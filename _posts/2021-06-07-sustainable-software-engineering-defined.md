---
layout: post
description: Curious about green software engineering? This post covers the common terms & how developers can take action against the climate crisis with just their day jobs. 
categories: [green software, sustainability, sse]
title: An introduction to Sustainable/Green Software Engineering
---

# Introduction 👋🏽

Sustainable Software Engineering (SSE or SSWE) is a relatively young sub-field of the discipline it hearlds from. As the climate crisis worsens, and as our world relies on technology more & more. It is important that we as engineers begin to consider the impact our software has on our planet.

While obvious ways of making your role more sustainable could be advocating for climate action at your workplace or joining a company that is working on solutions for the climate crisis, this post aims to cover some not so obvious ways you can bring sustainability to your role as a software engineer.

# Carbon Proxies 
Since it is often difficult to collect 100% accurate stats on the carbon footprint of your software. We can use other metrics to serve as a proxy that can link back to carbon emissions.

Here are a few examples of Carbon Proxies:

| Frontend & Client side     | Backend Services |
| ----------- | ----------- |
| Time to Interact (TTI). A shorter TTI implies better performing code    | Server Costs or Compute Units. Aim to have your code just as well on lower end hardware. |
| Page Size. Larger pages require more bandwidth   | Utilization. Running a server 24/7 uses more energy then going serverless or allocating loads dynamically |  

# Carbon Aware vs Carbon Efficient 

There are two terms often used to describe the role software plays in lowering emissions. These are not exclusive categories either.

- **Carbon Aware** : Software that can change its behavior based on the current carbon intensity of the grid it is using​

- **Carbon Efficient** : Efficient Software that can extract as much value as possible for carbon emitted​

Majority of the time you are designing your applications to be carbon efficient, but increasingly there is an interest in application that are *both* carbon aware & efficient. This post primarily covers ways to achieve the latter.

# So what can developers do? 👩🏽‍💻

This section will impart some common wisdom for those in various developer roles. I won't be covering things like volunteering, "contribute to open source, or joining a climate tech company. Just action items you can implement in your day job.

One of the more *important* activites you can do as a developer is to be an **advocate** for change in your workplace. Work with other employees to demand your company have an ambitious climate comittment & that it sticks to it.

One thing I will be omitting from this post is picking certain languages/technologies over others. Stick with what you are most productive in! But if you want to see how your choice of language could impact your carbon footprint. Check out [this post on language choice & desktop UI apps](https://devblogs.microsoft.com/sustainable-software/language-impact-on-ui-apps/)

If you think I missed something. Please feel free to contact me and let me know!

&nbsp;
## Web & App Development 🌐
Since this is the area I currently work in. I have a lot to say on the subject! So here is a nice listicle.

Some places you can measure the carbon footprint of your website:

- [Website Carbon](https://www.websitecarbon.com/)
- [Greenspector](http://mobile-efficiency-index.com/en/)

Here is a non-exhaustive short list of ways you can reduce the environmental burden of your software:

- Smaller JS bundles
- Optimize for [Core Web Vitals](https://web.dev/vitals/)
- Profile your applications to find weaknesses for optimization
- Batch I/O calls over dozens of smaller calls
- Lazy loading or virtualization
- Use system default fonts
- [Subset your fonts, load only the glyphs you need](https://www.afasterweb.com/2018/03/09/subsetting-fonts-with-glyphhanger/?utm_medium=email&utm_source=fershad)
- If your site requires CPU heavy loads from the client, consider using WASM for better performance
- Ensure your website has a dark theme option (darker pixels use less energy)
- Remove unnesscary cookies

&nbsp;
## AI / ML 🧠
The [carbon footprint of training AI](https://www.nature.com/articles/s42256-020-0219-9) is an increasingly well known problem. While there are arguments to be made that we need larger models first before we can create smaller ones. If you are an engineer in space, try using a smaller model on your task before going straight for the largest one. Does it achieve similar performance? Does the larger model truly provide additional utility or revenue gains? 

If you need to go with larger models, try to find infastructure powered completely by renewables. Most of the major cloud providers are already transitioning to renewable energy. You can search to see what regions run completely off of renewables. 

For researchers, tools like [ML CO2 Calculator](https://mlco2.github.io/impact/) can help you calculate the emissions from your model & generate LaTeX for you to include in your publication. The Python package [Code Carbon](https://codecarbon.io/) lets you track emissions of your model training with a few lines of code. 

If you want to see applications of AI in the climate space. Checkout Microsoft's [AI for Earth](https://www.microsoft.com/en-us/ai/ai-for-earth) program.

&nbsp;
## Cloud Computing, Operations & Security ⛅
As we defined carbon efficiency earlier. You always want your code to be as energy efficient as possible. Downtime or security vulnerabilities not only make your life as a developer more difficult, but also bring down how much value your code is using per unit energy consumed. 

Infastructure & system design decisions play a huge role here too! You can use [chaos engineering to lower carbon emissions of your system](https://devblogs.microsoft.com/sustainable-software/the-carbon-monkey/) or opt for [serverless functions to reduce compute consumption](https://devblogs.microsoft.com/sustainable-software/how-azure-com-uses-serverless-functions-for-consumption-based-utilization-and-reduced-always-on-electric-footprint/). Moving past efficiency and into smarter systems such as [Carbon-Aware Kubernetes](https://devblogs.microsoft.com/sustainable-software/carbon-aware-kubernetes/) or [moving compute intensive workloads to data centers using renewable energy](https://blog.google/inside-google/infrastructure/data-centers-work-harder-sun-shines-wind-blows/)

If some of the above steps are a bit too extra for your workload, [moving your infastructure over to containers alone can result in huge costs savings & increased CPU utilization](https://www.cncf.io/case-studies/nordstrom/), both of these follow the principles of using less energy + getting more value out of the energy you do use.

&nbsp;

# Online Communities 💬
Tons of amazing smart folks are also thinking about how software can help solve or mitigate the worse impacts of the climate crisis. Here are just a few communities where this awesome work is happening:

- [ClimateAction.tech](https://climateaction.tech/)
- [Work on Climate](https://workonclimate.org/)
- [Earthshot Labs](https://www.earthshot.eco/)
- [Climate Change AI](https://www.climatechange.ai/)
- [Important not Important](https://www.importantnotimportant.com/)

# Conclusion 🙋🏽‍♂️

Thanks for reading! I wrote this post so I can share with friends some of the few dozen ways they we have an **impact** on the climate crisis. Being a software engineer, we often wonder the real world value or impact our code can have beyond business value.

The end goal of sustainable software engineering isn't to establish a separate subdiscipline, but rather become part of what it means to be a software engineer.

Just as we consider performance, accessibility, testing, security, etc when writing our programs. We must now consider the impact our programs have on our environment. From the compute resources, to how it impacts the users on the other end.

# References 📝
- [Microsoft's Sustainable Software blog](https://devblogs.microsoft.com/sustainable-software/)
- [Principles of Green Software Engineering](https://principles.green/)
- [Green Software Foundation](https://greensoftware.foundation/)
- [How to Save a Planet](https://gimletmedia.com/shows/howtosaveaplanet)
- [Towards Sustainable Software Engineering](https://increment.com/containers/containers-for-sustainable-software-engineering/)
