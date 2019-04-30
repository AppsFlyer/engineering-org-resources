## AppsFlyer Engineering has expertise on a diversity of topics, find the different abstracts below.  

We are happy to be invited to speak in any forum - conference, meetup, community event - so be sure to reach out.  Follow us on Twitter: [@appsflyerdev](https://www.twitter.com/appsflyerdev) and our [AppsFlyer Engineering meetup group](https://meetup.com/appsflyer).

<hr/>

### [Big Data Talks](#big-data)
<hr/>

<details><summary>From Theory to Practice: Segmenting Big Data with Probabilistic Data Structures</summary>

#### Short Description
Building solutions around large data sets with near real time response time is no easy feat. This requires the practical application of computer science theory to do so with minimal latency and while remaining fresh and precise.


#### Long Description
As a company that ingests large amounts of data (more than 90TB/day), as part of our core functionality, AppsFlyer for ways to empower users to leverage their data by providing access to data sets for finer-grained analysis and segmentation to optimize targeting. Access to large data sets, especially raw data is often times an I/O intensive task, making it a slow and memory-straining task. Therefore, when setting out to provide such functionality, we were faced with a challenging engineering problem which also required us to apply theory from the field of Computer Science.

When we decided to launch a new service called audiences that would enable users near real time segmentation of relevant audiences based on different filters – we needed to examine how to provide data as reliably as possible with minimal latency. This talk will dive into how we built the solution taking into account how to provide the freshest most precise data, while persisted to easily accessible storage. This required qualifying the right probabilistic data structure, modeling the solution for rapid data access – through its schema and flow and leveraging the right tooling – including Spark, Hadoop and HBase, and the challenges involved with doing so with a jungle of unstructured massive data sets.

Speakers: [Ronen Cohen](#)
Type: Full-length Presentation
</details>

<details><summary>Journey to Real-Time Analytics in Extreme Growth</summary>

#### Short Description

At AppsFlyer we have been finding ourselves the victims of our own success, with our data continuously growing, alongside the capabilities we want to enable for our clients to make better marketing decisions. This talk will dive into the evolution of our data management choices to support the changing needs of the business.

#### Long Description
At AppsFlyer we have been finding ourselves the victims of our own success, with our data continuously growing, alongside the capabilities we want to enable for our clients to make better marketing decisions. These, of course, eventually impact the technology we choose to make this all possible. This talk will dive into the evolution of our data management choices to support the changing needs of the business.

Powering more than 130 thousand mobile apps around the globe, AppsFlyer receives more than 70 billion requests a day, and as a result have a diversity of teams requiring real time performance for different use cases, whether real time attribution, monitoring, big data or web analytics. Each team has built their own technology stack to deliver on its needs. This talk will dive into the many different databases we use in-house – from Aerospike to Druid, Neo4J, Redis, to Clickhouse and even those we chose to eventually phase out. It will dive into the performance considerations for each, and the use cases we leverage each different database for, and why it’s the ideal DB for the job.

This talk will dive into our journey of how to choose the right solution for the job to implement real-time aggregation alongside batch processing over Apache Spark, and additional big data needs with Hadoop. Being able to evolve our architecture enabled us to solve recurring pains as well as aggregate 10X amounts of data with much faster response times, keep up with product demands while delivering a cheaper solution from a production cost perspective.

Speakers: [Yulia Trakhtenberg](#), [Morri Feldman](#), [Nir Rubinstein](#), [Reshef Mann](#), [Adi Belan](#)

</details>

<details><summary>Managing Your Kafka in an Explosive Growth Environment</summary>

#### Short Description
Kafka, many times is just a piece of the stack that lives in production that often times no one wants to touch - because it just works. At AppsFlyer, Kafka sits at the core of our infrastructure that processes billions of events daily.

#### Long Description
Kafka, many times is just a piece of the stack that lives in production that often times no one wants to touch – because it just works. At AppsFlyer, Kafka sits at the core of our infrastructure that processes billions of events daily.

This talk will share how we built our microservices architecture with Kafka as its core piece to support 70B+ requests daily. With continuous growth we needed to “learn on the job” how to improve our Kafka architecture by moving to the producer owner cluster model, breaking up our massive monolith clusters to smaller more robust clusters, and migrating from an older version of Kafka with real-time production clients & data streams. The talk will outline best practices for leveraging Kafka’s in-memory capabilities & built-in partitioning, as well as some of the tweaks and stabilization mechanisms that enable real-time performance at web-scale, alongside processes for continuous upgrades and deployments with end-to-end automation, in an environment of constant traffic growth.

Speakers: [Alon Gavra](#)
Type: Full-length Presentation

</details>

<details><summary>Tick Tock on the Clock - Hope the Data Don't Stop</summary>

#### Short Description
Sometimes a small error can lead to catastrophic results. This will be a postmortem talk that will detail how we nearly lost massive amounts of data, and the work undertaken under fire to bring us back from the cliff's edge.


#### Long Description
This is a story of a race against time! So hang on to your seats…

During a customer migration to a new attribution system, a huge project for AppsFlyer Engineering in 2018, we found ourselves facing a potential data loss catastrophe. It all started with the primal sin of a premature optimization made where we set the incorrect data retention timeframe for a database holding 65 billion records.

When we discovered this, with only one week to respond before the data is permanently erased, we channeled our MacGyver skills and got to work. During this session I’ll describe the chain of events that brought us to the cliff’s edge, the steps we took around the clock to save our data, and how we managed to forestall any data loss for our clients.

Speakers: [Adi Belan](#)
Type: Post-mortem

</details>

<details><summary>Down the Big Data Infrastructure Rabbit Hole</summary>

#### Talk Description

The AppsFlyer data-infrastructure group was established to tackle the growing technical debt around the daily batch data processing - ingesting nearly 90TB a day. One of the initial tasks was focusing on fixing inexplicable corruptions which led us down a rabbit hole full of anomalies with our Spark committer, Hadoop JARs alongside interaction with our AWS S3 buckets (storing petabytes of data). This talk is our war story filled with twists and turns, a first time talk given outside of the walls of AppsFlyer walls aimed at shedding some light on what is truly involved with building a robust, real time, big data operation at scale.

Speakers: [Zohar Stiro](#)
Type: Full-length Presentation
</details>
  
<details><summary>A GDPR Retrospective: Implementation by a Large-Scale Data Organization in Reality</summary>

#### Short Description
GDPR was likely one of the biggest challenges in data management that occurred in 2018.  This talk will be a one year retrospective about how it was executed in reality at a large-scale data organization.

#### Long Description
The date May 25, 2018 was a fateful day for many companies that process & store client data - particularly across the EU. On this day GDPR went into effect - and no one really knew quite what its effects would be. This talk will take you through our company's journey to compliance - the indexers we used to append & delete client data, and a retrospective of how this affected our data processing operations. This will walk you through the design through implementation, as well as expectation vs. real demand. Eventually what we imagined would be requested by hundreds of clients at best ended up being requested by tens of thousands - and continues growing, and learning how to manage this new compliance demand alongside our day to day data engineering tasks & processes was no easy feat.

Speakers: [Zohar Stiro](#), [Ronen Cohen](#), [Morri Feldman](#)
Type: Full-length Presentation
</details>
 
  
<details><summary>Dynamic HBase Coprocessors Using Clojure</summary>

#### Abstract
HBase Coprocessors allow moving nearly arbitrary code execution from the client to the HBase Region Server. For some applications, coprocessors provide a number of major advantages. For instance, moving code from the client can often increase performance by limiting data transfer over the network, especially for aggregation type processing. Also by reducing client data processing, the hardware requirements of the client can lowered. However, programming coprocessors is challenging in several ways. The development cycle for coprocessor development is slow. To try out changes to a coprocessor on a cluster, the coprocessor must be compiled and then the HBase cluster must be restarted to reload the coprocessor. In addition, trying to load a coprocesor with certain defects can crash the HBase cluster.

I will present a generic coprocessor that is able to execute arbitrary Clojure code as a solution to some of the difficulties surrounding coprocessor development. The generic Clojure coprocessor accepts queries that bring their own aggregation instructions in the form of Clojure code. The Clojure code on each query will then be dynamically compiled and executed on the cluster by the generic Clojure coprocessor. Changing specific aggregation code now simply requires rewriting the Clojure code and sending a new query, making for a much faster development cycle than with traditional coprocessor development. To allow the Clojure code to depend on external dependencies -- for instance a JSON parsing library -- the generic Clojure coprocessor also allows for loading "static" dependencies from jar files. In addition to being more dynamic, coprocessor development safety is also increased, because the most dangerous steps, loading and initializing a coprocessor, are only done once rather than each time the aggregation logic is changed. The code for the generic Clojure coprocessor along with full examples will be provided as open source on GitHub.

Speakers: [Morri Feldman](#)

</details>


<details><summary>Salting Spark for Scale</summary>

#### Abstract
One of the major issues that Spark batch jobs have to contend with at AppsFlyer is that our data is inherently skewed.  For instance a couple of apps account for the vast majority of our traffic.  Data skew wreaks havoc on naively written data jobs by making them perform and scale very poorly as the amount of data they need to process increases.  Recently one of our central data aggregations -- the process that prepares data for the overview dashboard -- stopped working and we had essentially reached the limit where we could no longer devote more Ram to the process to help it.  Using a technique called "Salting" to overcome the data skew that was killing this job we were able to get the job working again and make the entire process much more scalable.  I'll go over Salting in depth to explain how it works and how we are starting to use it here at AppsFlyer.
  
Speakers: [Morri Feldman](#)

</details>

<p>
<br/>
  

  
<!--
<details><summary>...</summary> -->

<!-- #### Short Description -->

<!-- #### Long Description -->


<!-- Speakers: [#](#)
Type: Full-length Presentation
</details>
<p>  -->
  
### [Programming Talks](#programming)
<hr/>
<br/>


#### Clojure
<hr/>


<details><summary>How I Supercharged Learning Clojure through Gamification</summary>

#### Short Description
Gamification can be an excellent way to reduce the barrier of entry & quickly learn new programming languages. This talk will dive into how through a simple game you can master new syntaxes by applying concepts from languages you know & leveraging shared libraries to ramp up your coding skills.

#### Long Description
Mastering a new programming language can seem like a daunting task. As a person who has had to learn a number of new programming languages in a short amount of time, I’ve found gamification to be an excellent way to learn how to port knowledge from one language to another. This talk will dive into how through a simple game - I went through a journey of learning to code, and then was able to gain hands-on experience in a diversity of languages multiple times, when learning new languages. By applying concepts I formerly learned for Java to learn how to code in Clojure, and specifically by finding the similarities such as libraries, classes and types across languages, and then rebuilding this simple game in the new language, I quickly learned how to apply knowledge gained in other programming languages to the new language I was looking to learn. This talk will demonstrate how you can create a pet app that can teach you to too!

Speakers: [Mey Beisaron](#)
Type: Full-length Presentation
</details>



<details><summary>Clojure Fundamentals Workshop - From Zero to Hero</summary>

#### Short Description
The true value of Clojure is hard to appreciate without experiencing it. Come to this course to find out what makes Clojure so special and why it is attracting so many companies and programmers.

#### Long Description
Clojure is a modern functional Lisp that runs on the JVM. It is designed to allow programmers to write programs that tackle complex problems in as simple a way as possible, adding little unnecessary overhead (i.e. it was written to be very lean). The major features of Clojure work together synergistically to provide the ability to write simple programs. For instance, developing your program at the REPL gives you quick feedback and encourages a ground up introspective development style where you are inside your running program. Some of the features that we will cover here in this course include REPL driven development, Clojure’s opinionated concurrency model and access to the proven JVM ecosystem and infrastructure. The true value of Clojure is hard to appreciate without experiencing it.

Come to this course to find out what makes Clojure so special and why it is attracting so many companies and programmers.

This workshop is targeted to those new to both Clojure and / or functional programming. We will introduce Clojure and teach you how to use it effectively and idiomatically. Students will build a realistic, but simple HTTP-based service designed to introduce them to many of Clojure’s concepts and facilities.

Through a mixture of exposition and hands-on coding students will learn the following:

* Sequence model
* Immutability
* REPL-driven development
* Creating a project
* Data Oriented Programming
* Concurrency model
* Host interop
* Data specification using Clojure.spec
* CSP with core.async
* Macro system


**Agenda
Each is a 20 minute talk with 10 minutes of practice.**

#### Session 1
a. Basic Basics, addition subtraction, repl, editor
b. Map reduce filter – higher order functions
c. Namespaces, project organization, compilation?
- 30 Minute Break

#### Session 2
a. Setup a web app – ring middleware function composition
b. Immutability – both from hands-on, as well as theoretical persistent data structures
c. Atoms, start using them in web app immediately
- 30 Minute Break

#### Session 3
a. Routing / endpoints in web app. Starting / stopping threads
b. Core async to connect twitter read / processor threads
c. Finish the web app – resetting / getting histogram
- 30 Minute Break

* API for web app – 
* Start / stop reading from Twitter
* Get the current histogram
* Reset the histogram

Speakers: [Ronen Cohen](#), [Ido Barkan](#), [Morri Feldman](#)
Type: Workshop (90 Minutes - 8 Hours)
</details>
<p>


<br/>

#### Golang
<hr/>


<details><summary>Go-Sundheit - FTW! Async Health Check Library for Golang</summary>

#### Short Description

We recently open sourced an in-house library Go-Sundheit, to provide support for defining service health for golang services - this enables gophers to register async health checks for dependencies and the service itself - a pretty nifty tool in a dynamic CI/CD environment based on golang.

#### Long Description

At AppsFlyer we face the same issues that many other fast growing companies have to deal with - we have a considerably large operation, where we practice continuous delivery, and we’d like our deployments and runtime to be as safe as possible (mostly, so we can sleep well at night). This normally means that you’d like to know as soon as possible that your deployment has gone bad, or that a resource that your service depends on is now in bad shape.  

Enter Go-Sundheit. We recently started making the migration from Clojure to Go for some of our mission critical services, and in order to be able to have a more holistic view on the performance of our apps we needed to implement some health monitoring capabilities  This talk will present the open source library Go-Sundheit, a library built to provide support for defining service health for golang services. This allows you to register async health checks for your dependencies and the service itself, and provides a health endpoint that exposes their status. This session we will dive into some of the primary use cases where this is useful, and present a short demo for how to get started.


Speaker: [Eran Harel](#)

</details>

<p>

<details><summary>Migrating a Mission Critical Service to Go</summary>

#### Short Description
This talk will dive into how we rewrote one of our production services in Go, leveraging Golang’s natives proxy implementation and routines alongside its async capabilities for improved scale & throughput of web services, enabling exponentially improved performance.

#### Long Description
AppsFlyer, a leading mobile attribution & marketing analytics platform, processes nearly 70+ billion HTTP requests a day (approximately 50 million requests a minute), and is built using a microservices architecture. The entry point to the system that wraps all of the frontend services is a mission-critical (non-micro) service called the API Gateway. This essentially serves as a single point for routing traffic from customers to our backend services, simplifying authentication and authorization exponentially for our clients, but with the tradeoff of also potentially being a single point of failure.

Originally, this service was written in Clojure. As traffic grew - it became apparent that the code for the API gateway was too complex, and needed constant refactoring to enable the throughput required. Once the service became too unstable, we realized the we needed to rewrite the project completely - either in Clojure (just better), or explore other language options as well. This project decided to forego cognitive biases - and explore new language to rewrite the service to. After benchmarking, Go was selected and then went through a rigorous design phase, then rewrite, migration of production services, and benchmarking for improved performance. This talk will walk you through how to qualify a new language to introduce for mission critical production services, best practices for rewriting and migrating production services.

**Talk Outline:**
* Brief intro to describe technology stack & scenario 
* Previous architecture and need for rewrite 
* Benchmarking Clojure vs. other languages 
* Design, Implementation, Architecture 
* Migration + Benchmarking performance improvements 
* Q&A


Speakers: [Asy Ronen](#), [Yuri Kalinin](#)
Type: Full-length Presentation
</details>
<p>


<details><summary>Building a Service Metrics & Monitoring Stack for Go</summary>

#### Short Description
As a JVM-less language, this talk will dive into how we built a monitoring and metrics library for Go to be interoperable with additional in-house JVM libraries such as Clojure, Scala, and Javascript.

#### Long Description
AppsFlyer is largely a Clojure shop, that is a language that requires JVM to run a prerequisite. We recently decided to rewrite one of our mission-critical services in Go, to achieve better performance. While leveraging Go improved throughput, it is not a JVM based language, and in order to achieve out of the box services such as memory usage metrics, garbage collectors and more, for Go this needs to be written from scratch. This talk will dive into how we built a monitoring and metrics library for Go to be interoperable with JVM libraries such as Clojure, Scala, and Javascript to enable cross-language efficiency - and well as work with other parts of the stack including Redis & Kafka.

The talk will begin with outlining the difference between the two metrics stacks, out of the box support for each language and mapping the gaps for migration to Go. We will then dive into the challenges with interoperability between different languages in a production environment, as well as the challenges with writing language-specific libraries from scratch for production services - and will finish with a short demo of the AppsFlyer Go Metrics library, based on Grafana + Go (that will be open sourced once it is production-grade).

If time allows, we will also tell a short tale from the trenches about a bug that was discovered after rolling out the service to production of routines that would open (and not close), that caused a spike in requests, that would never have been discovered had we not written the new services along with the metrics libraries to properly monitor them, which eventually would have led to a massive production failure.

**Talk Outline:**
* Intro to technology stack - JVM vs. Go Metrics Stack
* Interoperability challenges between languages and environments
* Writing a Go-specific metrics stack to be interoperable with other JVM-based languages
* Short Demo (AppsFlyer Grafana Go Library - AF Go Metrics) 


Speakers: [Asy Ronen](#), [Yuri Kalinin](#)
Type: Full-length Presentation
</details>
<p>

<details><summary>From Theory to Practice: Segmenting Big Data with Probabilistic Data Structures</summary>

#### Short Description

#### Long Description


Speakers: [Adi Belan](#)
Type: Full-length Presentation
</details>

<details><summary>A Journey from Python to Go</summary>

#### Abstract

I love Python. It has been my go-to language for the past five years. But the growth in the popularity and maturity of Go, alongside the strong user base, made me think about how I can add it into my tool set.

In this talk, I'm going to tell you about my journey from Python to Go, and provide you with some tips and expose you to some of the resources that helped me succeed on this journey and live to tell the tale.  I will dive into some of the main differences, and how to minimize the learning curve, as well as some of the excellent libraries and tools that enabled me to ramp up my Go coding skills pretty quickly & painlessly.

Speaker: [Elad Leev](#)

</details>


<br/>

#### Frontend
<hr/>



<details><summary>API Gateways - This Time from the Client Side</summary>

#### Abstract

API gateways are a common practice - usually the "public face" of your internal system & are served via one or more backend services.

Besides providing a uniform API, they also facilitate a standard way of authentication, permissions, versioning & much more.
What if we could gain some of those benefits when we build our web applications? 

What if we could compose our app from multiple agnostic parts, each with its different underlying technology & version, thus, enforcing a global authentication flow without rebuilding the whole system?

This talk will show you how we took the core concepts of an API gateway & applied them as the base architecture for our web apps, & scaled to 30+ apps in production while sharing libraries of various versions, managing a global state, routing & more.

Speakers: [Shimi Bar](#), [Liron Cohen](#)
</details>
 

<details><summary>A Modular SDK in A Fragmented Landscape</summary>

#### Abstract

Web SDKs need to provide a host of capabilities & are a contradiction in terms - on the one hand, they need to be "fully baked" & "closed" in order to provide a uniform API. On the other hand, they need to be flexible in order to support future development & a wide range of clients.

While this can be achieved by "baking" a custom SDK per client - this is not very scalable (nor practically applicable with a business in exponential growth). In order to be able to deliver on the promise of modularity, we wanted to enable users to decide which capabilities they want to enable, without having to define this in advance.  This talk will dive into the development methodology we used in-house to support this, & eventually, how we serve multiple SDKs in a uniform manner to a diversity of clients.

Speakers: [Shimi Bar](#), [Liron Cohen](#)
</details>

<details><summary>Micro-frontends: Is it a Silver Bullet?</summary>

#### Short Description
Micro-frontends - is it just a hyped out buzzword or do they live up to their promise? This talk will cover how we architected our micro-frontends solution, the challenges we encountered, how we overcame them - and answer the ultimate question, are micro-frontends worth the hype?

#### Long Description
Micro-Frontends are gaining a lot of traction these days as the “silver bullet” solution to the former monolith project architecture, essentially the frontend variation on microservices. If you’re not familiar with micro-frontends, and how to implement them in your environment, you might find yourself asking “am i missing out on something important?” or “what does this even mean?”

In this talk, I will walk you through our journey where we found ourselves accumulating independent monolithic frontend stacks - and had to find a better way to manage and maintain these stacks in a hyper-growth environment. We will present how we migrated to this loosely-coupled architecture of independent projects and eventually were able to grow to 25+ micro-frontend projects that helped us optimize our development and achieve our goals more rapidly, the challenges we encountered that made our lives miserable - and how we overcame them, and finally will try to answer the ultimate question “are micro-frontends really a silver bullet?

Speakers: [Liron Cohen](#), [Shimi Bar](#)
Type: Full-length Presentation
</details>


<br/>

### [Culture Talks](#culture)
<hr/>


<details><summary>How we Hard Reset our Hiring & Onboarding Processes & Became High Performing Engineering Organization</summary>

#### Short Description
One of the long-standing anomalies in the tech industry is the focus on engineering products, but less so on engineering organizational culture.  Building great products, and hiring excellent engineers is a by-product of culture that needs to be constantly improved and evaluated.

#### Long Description
Have you ever found yourself struggling to build an engineering organization that is quality-driven with consistently great results?  When we analyzed why we didn't feel our organization was performing at the level we had anticipated, we reverse engineered this to fundamental issues with our culture.  Once we started working on this it had a ripple effect to our hiring process & then our onboarding process as well.  This talk will dive into how we refactored our hiring & onboarding to set up new hires for success from day one. This ultimately delivered a well-oiled high performing engineering organization through a practically applicable methodology that is easily replicable. This not only enabled us to improve the quality of our hires, but also retain excellent talent in the long-term.

Speakers: [Gilad Katz](#)
Type: Full-length Presentation
</details>

<details><summary>How We Went All-In on Reducing Technical Debt - And Lived to Tell the Tale</summary>

#### Short Description
A common modus operandi in many companies is "if it ain't broke - don't fix it" - this talk will demonstrate how to change this mindset to create higher performing engineering organizations.

#### Long Description
Imagine the technical debt of a startup in exponential growth for six consecutive years (growing from five engineers to 160 over this period, and from 10M daily events to over 70B). During this time, and up to the last 2 years the team focused on product expansion with a “if it ain't broke don’t fix it” attitude, resulting in inherent bugs, system instability & more than 80% of our team focused on maintenance. This will be a tale of how we went all-in on reducing technical debt by allocating more than 70% of the team for 1.5 years to reduce debt. I will share how we rewrote our core engine - at a time of extreme growth, while virtually putting on hold the rollout of any new features - a brave move in a competitive market. After two years into the process we managed to reduce the maintenance effort, number & severity of production issues - with the upside of increasing our velocity significantly. This was all made possible by instilling a culture of craftsmanship that was part of the re-engineering process, that has only been strengthen through this process.


Speakers: [Gilad Katz](#)
Type: Full-length Presentation
</details>

<details><summary>Artificial Insanity: How to Keep Calm and Combat Imposter Syndrome</summary>

#### Talk Description
We've all suffered from imposter syndrome from time to time.  But it turns out imposter syndrome has some really clear patterns, and there are actually a few simple tips and tricks to start appreciating ourselves more.  This talk will provide some tools to help you keep calm and focus on your small successes  that eventually translate to big successes - similar to Kaizen.  And that all this starts with allowing ourselves to be human first and foremost.

Speakers: [Sharone Zitzman](#)
Type: Ignite / Lightning Talk (5-10 Minutes) or Full-Length
</details>
<p>
<br/>


<details><summary>From Theory to Practice: Segmenting Big Data with Probabilistic Data Structures</summary>

#### Short Description

#### Long Description


Speakers: [Adi Belan](#)
Type: Full-length Presentation
</details>


<details><summary>From Theory to Practice: Segmenting Big Data with Probabilistic Data Structures</summary>

#### Short Description

#### Long Description


Speakers: [Adi Belan](#)
Type: Full-length Presentation
</details>
<p>


<br/>

### [Cloud & Platform Engineering Talks](#cloud)
<hr/>
<br/>

<details><summary>Baptism By Fire - Why Production Failures Make you a Better Developer</summary>

#### Short Description
Taking end-to-end ownership of your production code, enables you to understand the operational aspects even the best code encounters - and will contribute to improved coding practices.

#### Long Description
As developers, we are constantly focused on writing elegant and cutting edge code, however, meaningful code eventually lives 99% of its life in production, and becomes “someone else’s problem”. As with all code, issues are bound to arise and someone will have to deal with them (probably at 3 AM after a pagerduty call). At AppsFlyer all developers are expected to own their code end-to-end, to create a greater sense of commitment to its quality, and enable more rapid turnaround on debugging issues. Three years of being on the on-call rotation for mission critical services at AppsFlyer have taught me some hard lessons, but made me a better developer along the way. In this session I’ll dive into best practices for how to approach production issues as developers, some of the lessons I’ve learned about a developer managing production code, and how this ultimately makes us (much) better coders.

Speakers: [Adi Belan](#)
Type: Full-length Presentation

</details>
  
<details><summary>From Theory to Practice: Segmenting Big Data with Probabilistic Data Structures</summary>

#### Short Description

#### Long Description

Speakers: [Adi Belan](#)
Type: Full-length Presentation
</details>
