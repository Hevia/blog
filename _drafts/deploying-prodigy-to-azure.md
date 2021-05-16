# Introduction


## Prodigy Docker Container
Here is a sample image that will spin up your Prodigy server when ran (this is the same one I use for deployments)

```docker
FROM python:stretch

ENV PYTHONUNBUFFERED 1
ENV PRODIGY_PORT=8000
ENV PRODIGY_LOGGING=verbose

COPY *linux_x86_64.whl /root # This is your prodigy wheel thats given to you
RUN pip install /root/prodigy*.whl
RUN python -m spacy download en_core_web_md # Download the version you need
RUN mkdir -p /root/.prodigy/ # store your config & settings here
COPY ProdigyLicenseKey.txt /root/.prodigy/
COPY prodigy.json /root/.prodigy/prodigy.json
COPY ./your_data.jsonl /root/
RUN pip install psycopg2

ENTRYPOINT prodigy textcat.manual your_dataset_task_name ./root/your_data.jsonl  --label your_labels_go_here
```



# What you need?
- Dockerfile (like the one above)
- Your database (deployed wherever it is)
- prodigy.json (this should be inside your )