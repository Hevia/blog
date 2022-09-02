---
layout: post
description: A collection of things I learned and found worth sharing. Sometimes with sources!
categories: [TIL]
title: Today I Learned 📅
---

I stopped maintaining this list. Not because I still don't try to learn something new everyday, but the cost of keeping it up felt like a chore. Maybe I'll find a way to revitalize it in the future!

# June, 7th, 2012

- The Navajo goverment has its own presidental elections!
- Black on OLED screens is known to use less power because the LEDs that make up each pixel are off, whereas displaying white means the LEDs need to shine and consume power.
- Google found that on its devices that using blue used 25 percent more power than green or red
- In South Korea you are required by law to separate food scraps from your waste
  - That food waste is either turned into compost, biofuel, or other products
  - rotting food is a significant source of methane
  - It took 16 years from the laws inception in 1997 to finally achieve widespread adoption of 95%
  - The volume of food waste is still extremely high, which means 20-30% of the recycled byproduct goes unused
- Cloudflare's removal of the _cfduid cookie reports a net savings of 35k tons of CO2 per year because of Cloudflare's operating scale
- [Nonviolent protests are twice as likely to succeed as armed conflicts – and those engaging a threshold of 3.5% of the population have never failed to bring about change.](https://www.bbc.com/future/article/20190513-it-only-takes-35-of-people-to-change-the-world)
- Carbon emissions at data centers are determined by four variables: server utilization rate, choice of electrical grid, power usage effectiveness and overall power consumption
- Data Centers consumed 2% of electricity worldwide in 2019

# May 30th, 2021

- REE stands for Rare Earth Elements!
- China mines, processes, & exports about 70% of the worlds REEs
- You can use a heat pump connected to wastewater facilites to heat/cool homes & buildings
- The National Park Service is now changing its strategy from conserving the parks to preparing for how it will change as climate change worsens
- Fertilizers, from creation, to distribution account for almost 7% of GHG emissions worldwide in some models

# May 19th, 2021

- Kelp naturally accounts for ~5-10% of ocean carbon intake
- "Blue Carbon Storage" involves growing Kelp and sinking it to the seafloor to store carbon for nearly 1000 years
- Growing Sugar Kelp around Mussels helps improve the productivity of Mussels since Kelp can absord CO2 and reduce the local acidity levels
- Many marine plants evolved at a period in Earth's climate where CO2 was 2-3x higher then current levels, so that is why they thrive in high CO2 waters
- Some macroalgaes produce carrageenan which is used as an emsulifier in various food systems
- You can use livestock wastewater + algae to reuse water or grow algae farms
- Algae can be used to recycle metals from computer hardware (since certain algae species can absorb those metals)
- Algae can also be used to scrub microplastics from water using the same polysaccharides that help make carrageenan
- Algae can produce a wide range of food preservatives

# May 13th, 2021 🛴

- Service Workers operate on threads separate from main
- Service workers required HTTPS to be used
- ServiceWorkers + CacheStorage is what helps lead to such huge performance gains
- You can invalidate an old service worker cache by adopting a new name
- The cache used by service workers is separate from the browser cache
- iframes use their own browsing context which requires increased memory from the browser
- Service Workers are excuted in a ServiceWorkerGlobalScope context that have no access to DOM
- Service workers cannot be used when the user is in private browsing mode
- You have control over the cache lifetime for your site/service workers
- You can register service workers to listen for certain events (such as fetch) and whenever the client emits that event, the service workers will intercept the request & perform the work. You can then cache the result
- You can have the client install new service workers by also updating the associated cache version
- ServiceWorkers also enable push notifications & background sync APIs

# May 12th, 2021 🦼

## [Asynchronous Tasks with FastAPI and Celery](https://testdriven.io/blog/fastapi-and-celery/)

- Use Celery for tasks that perform heavy computation since FastAPI's Background tasks runs in the same event loop as your app's requests. Celery also has the benefit of being a managed task queue
- `celery worker` spins up a celery worker

# May 11th, 2021 🚁

- There are three methods corporations reduce GHG emissions
  - Direct abatement: direct elimination of GHGs within a company’s value chain
  - Neutralisation: removal of GHGs elsewhere to counterbalance own emission sources
  - Compensation: purchase of offsets to compensate GHG emissions
- Thermal Desalination : Heat up water to remove
- Reverse Osmosis : Filter water through a membrane (but can be an inefficient proess)
- Desalination plants account for up to 76 million tons of CO2 a year
- The salt water brine byproduct from desalination when pumped back into the ocean sinks to the bottom and can damage seafloor ecosystems 
- It is theorized that the leftover salt water brine can be used in manufacturing

## [Decoding the Weather Machine](https://www.pbs.org/wgbh/nova/video/decoding-the-weather-machine/)

- Infrared radiation is emitted by sources of heat 
- The composition of the atmosphere is what largely determines the temperature of Earth (we have known about this for almost 200+ years)
- John Tyndall discovered in 1859 that Carbon Dixoide traps heat 

## [Masters of the Pacific Coast: The Tribes of the American Northwest 2/2](https://youtu.be/RO2jRt8NqcY)

- There is a bit *too* much to write out, instead this 2 part documentary series is very much worth watching

# May 10th, 2021 🚦

- Inside of Cacti fluid are sugars called mucilage which can bind with contaiminants in water & help filter it. It was later developed into a powder which is used in many parts of the world to produce clean drinking water. Norma Alcantar is the scientists who discovered this after being told by her Grandmother how they would boil water with a cactus part a kids to help clean it.
- [Shaken Baby Syndrome](https://en.wikipedia.org/wiki/Shaken_baby_syndrome)
- In animal studies, a diet with 25% total calories coming from added sugars resulted in a 2-fold increase in total mortality rate
- Only use neutral oils when seasoning your cast iron (i.e: vegetabe, canola, sunflower, or shortening)
- 10 passes through coarse & 10 passes through fine are a good method to give your knives a quick sharp
- Don't clean your wetstone until AFTER you are sharpening all your knives, it helps with sharpening
- Use Bar Keepers Friend to clean your stainless steel pots & pan (use a glove & wash in the grain direction of the steel, which is normally in circles)
- Sharpen your knife with a wetstone 1-2 times a year
- A Solution of 1:1 water to white vinegar is a good regular cleaning of your board + a coat of food grade mineral oil

## The lost art of reading nature's signs by Tristan Gooley

- If you smell smoke in the air on a cold morning, the likely cause is a temperature inversion
- Temperature inversions increase the likelihood of fogs in the morning/evenings
- Rayleigh Scattering is responsible for making things that are further away appear lighter while making things close to you appear darker

## [Don't Talk to the Police](https://youtu.be/d-7o9xYp7eE)

- What you tell the police CANNOT be used to HELP you (Recall: Anything you say CAN and WILL be used AGAINST you)
- There are over 10,000 crimes on US Federal Code
- Even if you are guilty, do not talk to the police
- If you are innocent and only tell the truth, you will *always* give some information that will convict you. In some cases the police will even misrecall the testimony or not recall it fully

## [How Developers Can Create Personal Brands Through Online Presence](https://youtu.be/frWlMUv59kY)

- Good marketing is centered around establishing value for free first, before asking for money. 
- Bad marketing is when you try to sell the brand not the product
- Sales Safari is when you scout online communities for keywords, common painpoints, and ideas to help pitch or create your content
- 3 things you need to figure out when creating developer content
  - What are your goals?
  - Who is your audience (be very specific)? & What is your value proposition to them?
  - What culture are you adding to this space
- Personal Website
  - Maintain a personal website & link back to it on all your online profiles
  - On your contact page list the types of reasons you do/dont want to be contacted
- Online Profiles
  - Bio
    - Use the same bio + avatar on every active online profile
    - Use your bio to describe your value prop
    - Link any of the projects of yours you want people to check out
  - Github profile READMEs
    - Take advantage of them! They're useful!
    - Use pinned repos of the ones you want folks to check out
  - Pinned tweet
    - Think of it as the first result of a Google search query
    - People rarely scroll beyond a few tweets
    - You can make your pinned tweet the start of a thread

# May 7th, 2021 🚅

- Indingeous tribes in the PNW used aquacultures to harvest clams along the shores
- Indingeous tribes are theorized to have been in the PNW region for the past 10,000 years

# May 5th, 2021 🚂

- According to data collected by the HTTP Archive, videos, images, & JavaScript are the biggest network energy hogs.
- Online ads make up 10% of the internets carbon impact
- The "pull" design principle means dont load data until the user requests it, via interaction or navigation
- Default Effect is a psychological trick to encourage certain user behaviors. Often used nefariously but could be use to encourage better sustainable decisions.
- The 2011 SunShot initiative started by Obama's DOE helped bring down Solar costs to competitive levels in < 10 years and reached cheaper prices 3 years ahead of schedule
- Cruise lines register their companines in countries with loose labor laws. (source: Wendover Productions, The Insane Logistics of Shutting Down the cruise industry)
- CLUT stands for Color Look Up Tables.
- The Swedish scientist Svante Arrhenius first wrote about the link between carbon dioxide and global temperatures via the greenhouse effect in 1896.

## Ultimate GameBoy Talk

- GameBoy only uses 4 colors
- Original GameBoy only had 8KB of RAM!!
- Some games used MBCs(memory bank controllers) to play larger games on the GameBoy

## Python Concurrency: The Tricky Bits

- The Python GIL only allows one thread to run at any given time
- Because of the GIL, CPU bound tasks running on individual threads will slow each other down (theres a lot of blocking & resource starvation)
- Using threads does add additional speedups for I/O workloads
- You can simulate non-cpu bound task in Python using time.sleep()
- Python GIL will priotize CPU workloads over I/O workloads. This is unique to Python's GIL since OS's prefer shorter tasks
- A thread is always contained in a process, and each process contains one or more threads. Threads in the same process can share memory which means they can easily communicate and write to common data structures.
- Processes can generalize across CPU cores but threads can only run on a single core
- A common workaround to running code in Parallel in Python is to spawn several processes
- You can write C code that escapes the constraints of the GIL
- Processes have a bigger overhead compared to threads due to shared data/program state
- Procceses are not constrainted to run on a single CPU so you can execute CPU bound tasks in parallel on different cores
- Do not use threads for CPU workloads and do not use Processes for IO workloads. You will see decreased performance
- Reading/writing data to disk is not CPU work its IO work!
- Threads are more memory efficient then processes
- Pre-Emptive Multitasking is when the OS automately switches & interleaves thread events for you
- Cooperative Multitasking is when each thread announces when they want to switch. You can use coroutines to achieve this

# May 4th, 2021 🛺

- Endocrine Disruptors are chemicals that mimic the body's hormones which can fool our cells in acting in ways it was not supposed to
- Those endocrine disruptors which are found everywhere in our modern world could be causing the decline in sperm seen throughout much of the Western World
- About 350k deaths in America can be attributed to Air Pollution each year
