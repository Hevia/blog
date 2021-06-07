---
layout: post
description: A quick guide on how to deploy the Prodigy data labeling tool to Azure Web Apps using Docker
categories: [python, nlp, prodigy, azure, postgresql, docker]
title: Deploying Prodigy to Azure using Docker
---
# Introduction 👋🏽
This is a quick guide on how to deploy Explosion's data annotation tool [Prodigy](https://prodi.gy/). This guide is meant as a reference & assumes you know how to use Docker, Azure, and you know how to deploy/provision a database. 

If you get stuck check out the [Prodigy docs](https://prodi.gy/docs) or post your question on [Prodigy's support forum](https://support.prodi.gy/).


## Prodigy Docker Container 🐳
Here is a sample image that will spin up your Prodigy server when ran (this is the same one I use for deployments)
```docker
FROM python:stretch

ENV PYTHONUNBUFFERED 1
ENV PRODIGY_PORT=8000 # This is important!!! Remember the port number for the Web App step
ENV PRODIGY_LOGGING=verbose # I found the verbose logs helpful for debugging problems 

COPY *linux_x86_64.whl /root # This is your prodigy wheel thats given to you
RUN pip install /root/prodigy*.whl 
RUN python -m spacy download en_core_web_md # Download the language embeddings you need
RUN mkdir -p /root/.prodigy/ # store your config & settings here
COPY ProdigyLicenseKey.txt /root/.prodigy/
COPY prodigy.json /root/.prodigy/prodigy.json # Your prodigy settings
COPY ./your_data.jsonl /root/ # Your data
RUN pip install psycopg2 # Install your database ORM/driver here + any additional installs. We're using postgreSQL 

# Put your prodigy task
ENTRYPOINT prodigy textcat.manual your_dataset_task_name ./root/your_data.jsonl  --label your_labels_go_here
```

## Prodigy.json 📚
Here is an example of how your prodigy.json might look like. I had problems with Azure Web Apps when not setting `"host": "0.0.0.0"`. Change db_settings to db of your choice, refer to Prodigy documentation for how to do so. 

```json
{
    "feed_overlap": true,
    "host": "0.0.0.0",
    "db": "postgresql",
    "db_settings": {
        "postgresql": {
            "host": "yourdatabase.postgres.database.azure.com",
            "dbname": "postgres",
            "user": "admin-user@database-name",
            "password": "thepassword"
        }
    }
}
```

# Deployment 🚀


## Prereqs ✅
- Dockerfile (like the one above)
- Your database (deployed wherever it is)
- prodigy.json (this should be inside your image)

## Database 📁
Make sure you have your database configured beforehand. With prodigy you can have *multiple* instances running pointing to the *same* database working off of *different* datasets. You don't need to spin up a new db with every image. Make sure your database accepts connections from the IP of your web app or the proper network permissions are in place. You will know your prodigy instance can connect to your database once you test it locally. 

## Docker 🐋
You want to build & test your prodigy image, then push it to your container registry. For this tutorial we're using Docker's public container registry. Might be best to use a private registery so nobody can pull your image and annotate your data 😅

1. Build your prodigy: `docker build -t <tag-name> .`

2. Test it locally: `docker run -p 8000:8000 <tag-name>`

3. Push it to your container registry: `docker push <tag-name>`

## Azure Web Apps ⛅
Navigate to the resource group you want to use.

1. Follow Add -> Marketplace -> Web App.

2. On the Web App Creation Page under the **Instance Details** panel:
    - Select `Docker Container` for Publish
    - Select `Linux` for OS

3. Configure everything else on this page for your needs.

4. On the Web App Docker page, configure it to pull from your Docker image. Make sure you don't have any accidental spaces or misspellings (which has happened plenty of times to myself!)

5. Configure any other pages you need, but it is now good to hit `Review + create`

6. Head over to your provisioned Web App resource

7. On the left side column panel. Navigate to Settings -> Configuration -> Application Settings

8. Add a new application setting

9. **IMPORTANT!** Name it `WEBSITES_PORT` and set the value to be the same port number as the `PRODIGY_PORT` in your Dockerfile. So for in our example `WEBSITES_PORT` would be set to `8000`. If you forget to set this application setting, I have found prodigy not to work/load. 

10. Save & restart your Web App

After some time, depending on the size of your container. You should be able to navigate to your URL & start annotating!