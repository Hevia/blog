# Introduction 🧪
This post is a sort of informal literature review of scientific claim verification & generation. As of spring 2022, I am looking to start a graduate program. In preparation for that I am trying to narrow down my research interests to the general umbrella of scientific NLP. I'll be writing a series of posts outlining these tasks in the hope I can educate others & narrow down my research goals. 🤗

Scientific claim verification is a new NLP task introduced in (cite). The goal of the task is given a scientific claim & associated abstract(s). Identify whether or not the claim is supported or refuted by the abstract(s) and extract rationale sentences that justify the conclusion. 

From my understanding, one of the motivations behind this task is to aid researchers sift through scientific claims easily. This is as opposed to fact checking where the goal is to aid platforms & journalists in countering misinformation. Both of these tasks are similar in the sense they are determing whether an input claim is supported or refuted by a set of given source documents & models need to explain their rationale for their choices. In actuality you can likely also use models trained on scientific claims in efforts to combat misinformation. The reason for this distinction is to limit what the scope of the dataset is covering. 

Where these two tasks diverge is the nature of their inputs. For scientific claim verification, a valid claim is defined as: fluent, atomic, & decontextualized. What does this mean? Let's explore!

| Type      | Example |
| ----------- | ----------- |
| Atomic      | Dogs are mammals. |
| Not Atomic   | Dogs are mammals and have four legs. |  


| Type      | Example |
| ----------- | ----------- |
| Decontextualized      | Earthquakes happen because of the movement of tectonic plates. |
| Not Decontextualized   | As per the sentence previous, we know what causes earthquakes to happen. |  



# Verifying Scientific Claims ✅

# Generating Scientific Claims ✏️

# Directions for further research ⏭️

- Taking existing sentences and augmenting them into a valid claim. (T)
- Using retrival augmented transofmers (RAG, RETRO, WebGPT). I could see this being especially useful so you can get rid of the abstract as input requirement. Thus the model only needs the claim as input and is able to return 

If you work in this field & you're looking for collaborators please reach out :)

# References