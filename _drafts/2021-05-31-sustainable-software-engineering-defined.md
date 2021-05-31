---
layout: post
description: Curious about green software engineering? This post covers the common terms & how developers can take action against the climate crisis with just their day jobs. 
categories: [green software, sustainability, sse]
title: An overview of Sustainable/Green Software Engineering
---

# Introduction 👋🏽
Sustainable Software Engineering (SSE or SSWE) is a relatively young sub-field of the discipline it hearlds from. As the climate crisis worsens, and as our world relies on technology more & more. It is important that we as engineers begin to consider the impact our software has on our planet. 

While obvious ways of making your role more sustainable could be advocating for climate action at your workplace or joining a company that is working on solutions for the climate crisis, this post aims to cover some not so obvious ways you can bring sustainability to your role as a software engineer. 

# Carbon Proxies 

# Carbon-Aware vs Carbon-Efficient 

# So what can developers do? 👩🏽‍💻
This section will impart some common wisdom for those in various developer roles. I won't be covering things like volunteering, "contribute to open source, or joining a climate tech company. Just action items you can implement in your day job.

One of the more *important* activites you can do as a developer is to be an **advocate** for change in your workplace. Work with other employees to demand your company have an ambitious climate comittment & that it sticks to it. How to Save a Planet has a great episode on how employees [made this happen at Amazon](https://gimletmedia.com/shows/howtosaveaplanet/kwhljz7/how-amazon-workers-got-serious-about)

One thing I will be omitting from this discussion is picking certain languages/technologies over others. Stick with what you are most productive in! But if you want to see how your choice of language could impact your carbon footprint. Check out [this post on language choice & desktop UI apps](https://devblogs.microsoft.com/sustainable-software/language-impact-on-ui-apps/)

If you think I missed something. Please feel free to contact me and let me know!

&nbsp;
## Web & App Development 🌐
Since this is the area I currently work in. I have a lot to say on the subject! One of the first improvements 

Some places you can measure the carbon footprint of your website:
- 

Here is a non-exhaustive short list of ways you can reduce the environmental burden of your software:
- Smaller JS bundles
- Lazy loading
- Use system default fonts
- 


&nbsp;
## AI / ML 🧠
The [carbon footprint of training AI](https://www.nature.com/articles/s42256-020-0219-9) is an increasingly well known problem. While there are arguments to be made that we need larger models first before we can create smaller ones. If you are an engineer in space, try using a smaller model on your task before going straight for the largest one. Does it achieve similar performance? Does the larger model truly provide additional utility or revenue gains? 

If you need to go with larger models, try to find infastructure powered completely by renewables. Most of the major cloud providers are already transitioning to renewable energy. You can search to see what regions run completely off of renewables. 

For researchers, tools like [ML CO2 Calculator](https://mlco2.github.io/impact/) can help you calculate the emissions from your model & generate LaTeX for you to include in your publication. 

If you want to see applications of AI in the climate space. Checkout Microsoft's [AI for Earth](https://www.microsoft.com/en-us/ai/ai-for-earth) program. 

&nbsp;
## Cloud Computing, Operations & Security ⛅
As we defined carbon efficiency earlier. You always want your code to be as energy efficient as possible. Downtime or security vulnerabilities not only make your life as a developer more difficult, but also bring down how much value your code is using per unit energy consumed. 

Infastructure & system design decisions play a huge role here too! You can use [chaos engineering to lower carbon emissions of your system](https://devblogs.microsoft.com/sustainable-software/the-carbon-monkey/) or opt for [serverless functions to reduce compute consumption](https://devblogs.microsoft.com/sustainable-software/how-azure-com-uses-serverless-functions-for-consumption-based-utilization-and-reduced-always-on-electric-footprint/). Moving past efficiency and into smarter systems such as [Carbon-Aware Kubernetes](https://devblogs.microsoft.com/sustainable-software/carbon-aware-kubernetes/) or [moving compute intensive workloads to data centers using renewable energy](https://blog.google/inside-google/infrastructure/data-centers-work-harder-sun-shines-wind-blows/)

&nbsp;
## Blockchain 🔗
I won't claim to be an expert on blockchain or cryptocurrencies, but it is obvious they are not going the way of the dodo. If you are a developer in this space, ensure your blockchain isn't wasting needless computation ala proof of work, and investigate alternative consensus algorithims such as proof of stake or proof of activity. If you are working on a cryptocurrency, ensure your currency provides utility besides just digital money. 

It is also important to consider the justice components of your application. Is your cryptocurrency solving a problem other technologies can't? Or are you just building something for the rich to get richer?

&nbsp;
## Quantum Computing 🧪
One of the coolest applications of Quantum computing is [Quantum-Inspired algorithims](https://docs.microsoft.com/en-us/azure/quantum/optimization-what-is-quantum-optimization) which are optimization algorithims that run on classicial hardware, but are far more performant. If your task requires optimization somewhere in the process, this class of algorithims could potentially provide a performance boost & improve the carbon efficiency of your application. 

Quantum Computing can also be applied with [optimizing conservation projects](https://cloudblogs.microsoft.com/quantum/2021/03/09/modernizing-conservation-planning-software-for-broader-global-impact/) or [tuning traffic signals to use the least amount of carbon](https://cloudblogs.microsoft.com/quantum/2020/08/04/jij-toyota-azure-quantum-reducing-carbon-emissions/)


# Online Communities 💬
Tons of amazing smart folks are also thinking about how software can help solve or mitigate the worse impacts of the climate crisis. Here are just a few communities where this awesome work is happening:

- [ClimateAction.tech](https://climateaction.tech/)
- [Work on Climate](https://workonclimate.org/)
- [Earthshot Labs](https://www.earthshot.eco/)
- [Climate Change AI](https://www.climatechange.ai/)
- [Important not Important](https://www.importantnotimportant.com/)

# Conclusion 🙋🏽‍♂️
Thanks for reading! Hopefully you see just how **much** a software engineer can do in their day job alone. The end goal of sustainable software engineering isn't to establish a separate subdiscipline, but rather become part of what it means to be a software engineer. Just as we consider performance, accessibility, testing, security, etc when writing our programs. We must now consider the impact our programs have on our environment. From the compute resources, to how it impacts the users on the other end. 

# References 📝
- [Microsoft's Sustainable Software blog](https://devblogs.microsoft.com/sustainable-software/)
- [Principles of Green Software Engineering](https://principles.green/)
- [Green Software Foundation](https://greensoftware.foundation/)
- [How to Save a Planet](https://gimletmedia.com/shows/howtosaveaplanet)
