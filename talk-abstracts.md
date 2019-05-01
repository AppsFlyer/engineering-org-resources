**AppsFlyer Engineering has expertise in many areas from data engineering & science, a diversity of programming languages, platform and cloud operations as well as, culture & psych talks. You can find the different abstracts below.**  

We are happy to be invited to speak in any forum - conference, meetup, community event - so be sure to reach out.  Follow us on Twitter: [@appsflyerdev](https://www.twitter.com/appsflyerdev) and our [AppsFlyer Engineering meetup group](https://meetup.com/appsflyer).

<hr/>

### [Big Data Talks](#big-data)
<hr/>

<details><summary><strong>From Theory to Practice: Segmenting Big Data with Probabilistic Data Structures</strong></summary>

#### Short Description
Building solutions around large data sets with near real time response time is no easy feat. This requires the practical application of computer science theory to do so with minimal latency and while remaining fresh and precise.


#### Long Description
As software organizations are required to handle increasing volumes of data, probabilistic data structures and algorithms have been put to use more widely in order to find approximative solutions to problems that would be computationally prohibitive otherwise. 

At AppsFlyer, we ingest a daily 80+ billion events sent by our users, which come into our system without any schema or predefined structure. When we set out to build a new data segmentation product, which allows our users to segment these billions of events according to any logical criteria they wish to specify, we were tasked with the challenge of offering them interactive estimated unique counts of their segments in near real time.

This posed an interesting challenge from both computer science and engineering perspectives, things we needed to consider: 

- Which data structure is most appropriate? 
- Which data model would allow us to compose any number of criteria when event schemas are unknown in advance and ever changing? 
- How do you implement aggregations such as group-by over probabilistic data? 
- What database should we pick to allow for fast and scalable access to our data structures? 
- How do you do this reliably, precisely and with high freshness?
 
This talk will discuss how we built a system which allowed us to solve this problem over massive data sets with technologies such as Kafka, Spark, HBase and Theta Sketches, and all this with a Clojure backend for improved concurrency and throughput.

Speakers: [Ronen Cohen](/speaker-profiles.md#ronen-cohen)
<p>pe: Full-length Presentation</p>

<hr/>
</details>

<details><summary><strong>Journey to Real-Time Analytics in Extreme Growth</strong></summary>

#### Short Description

At AppsFlyer we have been finding ourselves the victims of our own success, with our data continuously growing, alongside the capabilities we want to enable for our clients to make better marketing decisions. This talk will dive into the evolution of our data management choices to support the changing needs of the business.

#### Long Description
At AppsFlyer we have been finding ourselves the victims of our own success, with our data continuously growing, alongside the capabilities we want to enable for our clients to make better marketing decisions. These, of course, eventually impact the technology we choose to make this all possible. This talk will dive into the evolution of our data management choices to support the changing needs of the business.

Powering more than 130 thousand mobile apps around the globe, AppsFlyer receives more than 70 billion requests a day, and as a result have a diversity of teams requiring real time performance for different use cases, whether real time attribution, monitoring, big data or web analytics. Each team has built their own technology stack to deliver on its needs. This talk will dive into the many different databases we use in-house – from Aerospike to Druid, Neo4J, Redis, to Clickhouse and even those we chose to eventually phase out. It will dive into the performance considerations for each, and the use cases we leverage each different database for, and why it’s the ideal DB for the job.

This talk will dive into our journey of how to choose the right solution for the job to implement real-time aggregation alongside batch processing over Apache Spark, and additional big data needs with Hadoop. Being able to evolve our architecture enabled us to solve recurring pains as well as aggregate 10X amounts of data with much faster response times, keep up with product demands while delivering a cheaper solution from a production cost perspective.

Speakers: [Yulia Trakhtenberg](/speaker-profiles.md#yulia-trakhtenberg), [Morri Feldman](/speaker-profiles.md#morri-feldman), [Nir Rubinstein](/speaker-profiles.md#nir-rubinstein), [Reshef Mann](/speaker-profiles.md#reshef-mann), [Adi Belan](/speaker-profiles.md#adi-belan)
<p>Type: Full-Length Presentation
<hr/>

</details>

<details><summary><strong>Managing Your Kafka in an Explosive Growth Environment</strong></summary>

#### Short Description
Kafka, many times is just a piece of the stack that lives in production that often times no one wants to touch - because it just works. At AppsFlyer, Kafka sits at the core of our infrastructure that processes billions of events daily.

#### Long Description
Kafka, many times is just a piece of the stack that lives in production that often times no one wants to touch – because it just works. At AppsFlyer, Kafka sits at the core of our infrastructure that processes billions of events daily.

This talk will share how we built our microservices architecture with Kafka as its core piece to support 70B+ requests daily. With continuous growth we needed to “learn on the job” how to improve our Kafka architecture by moving to the producer owner cluster model, breaking up our massive monolith clusters to smaller more robust clusters, and migrating from an older version of Kafka with real-time production clients & data streams. The talk will outline best practices for leveraging Kafka’s in-memory capabilities & built-in partitioning, as well as some of the tweaks and stabilization mechanisms that enable real-time performance at web-scale, alongside processes for continuous upgrades and deployments with end-to-end automation, in an environment of constant traffic growth.

Speakers: [Alon Gavra](/speaker-profiles.md#alon-gavra)
<p>Type: Full-length Presentation</p>
<hr/>

</details>

<details><summary><strong>Tick Tock on the Clock - Hope the Data Don't Stop</strong></summary>

#### Short Description
Sometimes a small error can lead to catastrophic results. This will be a postmortem talk that will detail how we nearly lost massive amounts of data, and the work undertaken under fire to bring us back from the cliff's edge.


#### Long Description
This is a story of a race against time! So hang on to your seats…

During a customer migration to a new attribution system, a huge project for AppsFlyer Engineering in 2018, we found ourselves facing a potential data loss catastrophe. It all started with the primal sin of a premature optimization made where we set the incorrect data retention timeframe for a database holding 65 billion records.

When we discovered this, with only one week to respond before the data is permanently erased, we channeled our MacGyver skills and got to work. During this session I’ll describe the chain of events that brought us to the cliff’s edge, the steps we took around the clock to save our data, and how we managed to forestall any data loss for our clients.

Speakers: [Adi Belan](/speaker-profiles.md#adi-belan)
<p>Type: Post-mortem</p>
<hr/>

</details>

<details><summary><strong>Down the Big Data Infrastructure Rabbit Hole</strong></summary>

#### Talk Description

The AppsFlyer data-infrastructure group was established to tackle the growing technical debt around the daily batch data processing - ingesting nearly 90TB a day. One of the initial tasks was focusing on fixing inexplicable corruptions which led us down a rabbit hole full of anomalies with our Spark committer, Hadoop JARs alongside interaction with our AWS S3 buckets (storing petabytes of data). This talk is our war story filled with twists and turns, a first time talk given outside of the walls of AppsFlyer walls aimed at shedding some light on what is truly involved with building a robust, real time, big data operation at scale.

Speakers: [Zohar Stiro](/speaker-profiles.md#zohar-stiro)
<p>Type: Full-length Presentation</p>
<hr/>

</details>
  
<details><summary><strong>A GDPR Retrospective: Implementation by a Large-Scale Data Organization in Reality</strong></summary>

#### Short Description
GDPR was likely one of the biggest challenges in data management that occurred in 2018.  This talk will be a one year retrospective about how it was executed in reality at a large-scale data organization.

#### Long Description
The date May 25, 2018 was a fateful day for many companies that process & store client data - particularly across the EU. On this day GDPR went into effect - and no one really knew quite what its effects would be. This talk will take you through our company's journey to compliance - the indexers we used to append & delete client data, and a retrospective of how this affected our data processing operations. This will walk you through the design through implementation, as well as expectation vs. real demand. Eventually what we imagined would be requested by hundreds of clients at best ended up being requested by tens of thousands - and continues growing, and learning how to manage this new compliance demand alongside our day to day data engineering tasks & processes was no easy feat.

Speakers: [Zohar Stiro](/speaker-profiles.md#zohar-stiro), [Ronen Cohen](/speaker-profiles.md#ronen-cohen), [Morri Feldman](/speaker-profiles.md#morri-feldman)
<p>Type: Full-length Presentation</p>
<hr/>

</details>
 
  
<details><summary><strong>Dynamic HBase Coprocessors Using Clojure</strong></summary>

#### Abstract
HBase Coprocessors allow moving nearly arbitrary code execution from the client to the HBase Region Server. For some applications, coprocessors provide a number of major advantages. For instance, moving code from the client can often increase performance by limiting data transfer over the network, especially for aggregation type processing. Also by reducing client data processing, the hardware requirements of the client can lowered. However, programming coprocessors is challenging in several ways. The development cycle for coprocessor development is slow. To try out changes to a coprocessor on a cluster, the coprocessor must be compiled and then the HBase cluster must be restarted to reload the coprocessor. In addition, trying to load a coprocesor with certain defects can crash the HBase cluster.

I will present a generic coprocessor that is able to execute arbitrary Clojure code as a solution to some of the difficulties surrounding coprocessor development. The generic Clojure coprocessor accepts queries that bring their own aggregation instructions in the form of Clojure code. The Clojure code on each query will then be dynamically compiled and executed on the cluster by the generic Clojure coprocessor. Changing specific aggregation code now simply requires rewriting the Clojure code and sending a new query, making for a much faster development cycle than with traditional coprocessor development. To allow the Clojure code to depend on external dependencies -- for instance a JSON parsing library -- the generic Clojure coprocessor also allows for loading "static" dependencies from jar files. In addition to being more dynamic, coprocessor development safety is also increased, because the most dangerous steps, loading and initializing a coprocessor, are only done once rather than each time the aggregation logic is changed. The code for the generic Clojure coprocessor along with full examples will be provided as open source on GitHub.

Speakers: [Morri Feldman](/speaker-profiles.md#morri-feldman)
<p>Type: Full-length Presentation</p>

<hr/>

</details>


<details><summary><strong>Salting Spark for Scale</strong></summary>

#### Abstract
One of the major issues that Spark batch jobs have to contend with at AppsFlyer is that our data is inherently skewed.  For instance a couple of apps account for the vast majority of our traffic.  Data skew wreaks havoc on naively written data jobs by making them perform and scale very poorly as the amount of data they need to process increases.  Recently one of our central data aggregations -- the process that prepares data for the overview dashboard -- stopped working and we had essentially reached the limit where we could no longer devote more Ram to the process to help it.  Using a technique called "Salting" to overcome the data skew that was killing this job we were able to get the job working again and make the entire process much more scalable.  I'll go over Salting in depth to explain how it works and how we are starting to use it here at AppsFlyer.
  
Speakers: [Morri Feldman](/speaker-profiles.md#morri-feldman)
<p>Type: Full-length Presentation</p>

</details>
<br/>
    
### [Programming Talks](#programming)
<hr/>
<br/>


#### Clojure & Functional Programming
<hr/>

<details><summary><strong>How I Supercharged Learning Clojure through Gamification</strong></summary>

#### Short Description
Gamification can be an excellent way to reduce the barrier of entry & quickly learn new programming languages. This talk will dive into how through a simple game you can master new syntaxes by applying concepts from languages you know & leveraging shared libraries to ramp up your coding skills.

#### Long Description
Mastering a new programming language can seem like a daunting task. As a person who has had to learn a number of new programming languages in a short amount of time, I’ve found gamification to be an excellent way to learn how to port knowledge from one language to another. This talk will dive into how through a simple game - I went through a journey of learning to code, and then was able to gain hands-on experience in a diversity of languages multiple times, when learning new languages. By applying concepts I formerly learned for Java to learn how to code in Clojure, and specifically by finding the similarities such as libraries, classes and types across languages, and then rebuilding this simple game in the new language, I quickly learned how to apply knowledge gained in other programming languages to the new language I was looking to learn. This talk will demonstrate how you can create a pet app that can teach you to too!

Speakers: [Mey Beisaron](/speaker-profiles.md#mey-beisaron)
<p>Type: Full-length Presentation</p>
<hr/>

</details>


<details><summary><strong>Channels and Macros in Core.Async</strong></summary>

#### Short Description
How to best leverage Clojure’s core.async library for good concurrency and utilization of modern multicore processors without suffering from “callback hell”.


#### Long Description
Clojure’s core.async library implements Tony Hoare’s concurrent programming model Communicating Sequential Processes — CSP. CSP is probably best known from its implementation in the Go programming. In the CSP programming model, independent processes communicate synchronously across channels. The runtime is then responsible for shifting work on and off of worker threads as needed. Such a programming model allows for achieving good concurrency and utilization of modern multicore processors without getting trapped in “callback hell.” Clojure core async provides the two pieces required to program in the CSP style — channels and the equivalent of Go’s goroutines. The channels facilitate interprocess communication and the goroutines transform sequential code to run concurrently. Surprisingly the goroutine in Clojure is implemented not as a core language feature but as a macro — the “go” macro — that rewrites any provided code into a state machine which can park rather than block a CPU thread when there is no work to do. We will examine core.async’s channels and its “go” macro in some detail as well as look at some real-world examples of using core.async channels with and without the “go” macro.


Speakers: [Morri Feldman](/speaker-profiles.md#morri-feldman)
<p>Type: Full-length Presentation</p>
<hr/>

</details>

<details><summary><strong>Clojure Fundamentals Workshop - From Zero to Hero</strong></summary>

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

Speakers: [Ronen Cohen](/speaker-profiles.md#ronen-cohen), [Ido Barkan](/speaker-profiles.md#ido-barkan), [Morri Feldman](/speaker-profiles.md#morri-feldman)
<p>Type: Workshop (90 Minutes - 8 Hours)</p>
<hr/>

</details>

<details><summary><strong>Advanced Patterns in Asynchronous Programming</strong></summary>

#### Talk Description
This talk will cover some advanced compositional patterns with Scala Futures, in order to build and use higher level abstractions when dealing with async code.

Using Futures as a basic building block for concurrent, async code has become pervasive in the past few years and for a good reason. However, when moving from the traditional synchronous code to the async one, a set of patterns that were obvious to implement before now seem to be more challenging. The aim of this talk is to show few examples of these patterns implemented with Scala futures in an async and non blocking manner. We will present the usage pattern and the implementation in order to show the principles of properly handling async code.

In the talk we will use Scala code but the principles are universal and apply to other languages and future implementations. 

Speakers: [Michael Arenzon](/speaker-profiles.md#michael-arenzon), [Asy Ronen](/speaker-profiles.md#asy-ronen)
<p>Type: Full-length Presentation</p>
<hr/>
</details>


<details><summary><strong>Functional Programming Fundamentals Workshop</strong></summary>

#### Talk Description
This workshop aims to be the entry point for developers into the world of functional programming. We'll talk about various functional programming paradigms such as:
- Referential Transparency
- Immutability
- Higher Order Functions and more

Examples and hands on training will be via the Clojure programming language. After learning about the fundamentals of FP concepts (and getting our hands "dirty" with some Clojure code), we will progress to modeling and building a simple web app. We'll start small and show how FP principles lend themselves to our solution. Depending on how much time there is for workshops this can be very short intro or a much longer fundamentals course.

 

Speakers: [Ronen Cohen](/speaker-profiles.md#ronen-cohen), [Morri Feldman](/speaker-profiles.md#morri-feldman), [Nir Rubinstein](/speaker-profiles.md#nir-rubinstein), [Ido Barkan](/speaker-profiles.md#ido-barkan)
<p>Type: Workshop (90 Minutes to Full Day)</p>
<hr/>
</details>


<details><summary>When Choosing the Wrong Thread Causes Complete Chaos</summary>

#### Talk Description
When you process billions of requests a day concurrency & multi-threading is critical for performance. As heavy users of Aerospike & Clojure as our primary backend language, we needed to write a clj library for Aerospike as there wasn't anything readily available. As part of its functionality we thought it would be useful for the library to encode and decode DB values to work with the diversity of serialization methods we use across our DBs (JSON, gzip, protobuf, etc). However, we had a bit of an oversight in making the library non-blocking, and an even bigger mistake of having the wrong thread do the decoding. All this created an extremely slow performance on high load of our production clients. We will dive into how we handled the issue rapidly in real time & the lessons learned.

Speakers: [Ido Barkan](/speaker-profiles.md#ido-barkan)
<p>Type: Full-length Presentation, Post-Mortem</p>
</details>


<br/>

#### Uncategorized (by Language)
<hr/>


<details><summary><strong>Programming IS(!) Philosophy</strong></summary>

#### Talk Description
What is it about philosophy that, even today, makes people sit and debate about seemingly "nothing"? How can these vague notions and abstractions have any relevance in today's world of hard facts and cold logic? In my talk, I'll try and show how philosophy, with emphasis of linguistic philosophy, relates closely to what we do in our everyday lives as programmers. How simple things like programming language selection and trying to define a bug or name a service, are all issues that carry a much more significant meaning and context than we usually give them - I'll try, for the duration of this session, to give a glimpse behind the curtain of some of our (mis)conceptions about our world of software engineering.

The talk outline would be as follows:
1. General background about me, my education and how I found myself at the high-tech world 
2. Core concepts of linguistic philosophy and their relation to programming 
3. Intro to Witgenstein and the 7 value propositions of his tractatus 
4. How the 7 value propositions translate into programming 
5. Choosing a programming language based on all the principles above - more than a simple “low level vs. high level” or “OO vs Functional”
 

Speakers: [Nir Rubinstein](/speaker-profiles.md#nir-rubinstein)
<p>Type: Full-length Presentation</p>
<hr/>
</details>



<details><summary><strong>What Has Non-Blocking I/O Done for me Lately?</strong></summary>

#### Talk Description
Non-blocking IO is an often misunderstood piece of programming. This talk will dive into what non-blocking IO actually is, how it works, and how to increase your throughput by a few orders of magnitude. We will review the C10K problem, and why we can't just add more threads? I will also speak about when it's worth the extra complexity price, and how can you get there relatively easily once you make the choice to do so.

Speakers: [Eran Harel](/speaker-profiles.md#eran-harel)
<p>Type: Full-length Presentation</p>
<hr/>
</details>


<br/>

#### Golang
<hr/>


<details><summary><strong>Go-Sundheit - FTW! Async Health Check Library for Golang</strong></summary>

#### Short Description

We recently open sourced an in-house library Go-Sundheit, to provide support for defining service health for golang services - this enables gophers to register async health checks for dependencies and the service itself - a pretty nifty tool in a dynamic CI/CD environment based on golang.

#### Long Description

At AppsFlyer we face the same issues that many other fast growing companies have to deal with - we have a considerably large operation, where we practice continuous delivery, and we’d like our deployments and runtime to be as safe as possible (mostly, so we can sleep well at night). This normally means that you’d like to know as soon as possible that your deployment has gone bad, or that a resource that your service depends on is now in bad shape.  

Enter Go-Sundheit. We recently started making the migration from Clojure to Go for some of our mission critical services, and in order to be able to have a more holistic view on the performance of our apps we needed to implement some health monitoring capabilities  This talk will present the open source library Go-Sundheit, a library built to provide support for defining service health for golang services. This allows you to register async health checks for your dependencies and the service itself, and provides a health endpoint that exposes their status. This session we will dive into some of the primary use cases where this is useful, and present a short demo for how to get started.


Speaker: [Eran Harel](/speaker-profiles.md#eran-harel)
<p>Type: Full-length Presentation</p>

</details>

<details><summary><strong>Migrating a Mission Critical Service to Go</strong></summary>

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


Speakers: [Asy Ronen](/speaker-profiles.md#asy-ronen), [Yuri Kalinin](/speaker-profiles.md#yuri-kalinin)
<p>Type: Full-length Presentation</p>
<hr/>
</details>


<details><summary><strong>Building a Service Metrics & Monitoring Stack for Go</strong></summary>

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


Speakers: [Asy Ronen](/speaker-profiles.md#asy-ronen), [Yuri Kalinin](/speaker-profiles.md#yuri-kalinin)
<p>Type: Full-length Presentation</p>
<hr/>
</details>

<details><summary><strong>A Journey from Python to Go</strong></summary>

#### Abstract

I love Python. It has been my go-to language for the past five years. But the growth in the popularity and maturity of Go, alongside the strong user base, made me think about how I can add it into my tool set.

In this talk, I'm going to tell you about my journey from Python to Go, and provide you with some tips and expose you to some of the resources that helped me succeed on this journey and live to tell the tale.  I will dive into some of the main differences, and how to minimize the learning curve, as well as some of the excellent libraries and tools that enabled me to ramp up my Go coding skills pretty quickly & painlessly.

Speaker: [Elad Leev](/speaker-profiles.md#elad-leev)
<p>Type: Full-length Presentation</p>

<hr/>
</details>

<br/>

#### Frontend
<hr/>


<details><summary><strong>API Gateways - This Time from the Client Side</strong></summary>

#### Abstract

API gateways are a common practice - usually the "public face" of your internal system & are served via one or more backend services.

Besides providing a uniform API, they also facilitate a standard way of authentication, permissions, versioning & much more.
What if we could gain some of those benefits when we build our web applications? 

What if we could compose our app from multiple agnostic parts, each with its different underlying technology & version, thus, enforcing a global authentication flow without rebuilding the whole system?

This talk will show you how we took the core concepts of an API gateway & applied them as the base architecture for our web apps, & scaled to 30+ apps in production while sharing libraries of various versions, managing a global state, routing & more.

Speakers: [Shimi Bar](/speaker-profiles.md#shimi-bar), [Liron Cohen](/speaker-profiles.md#liron-cohen)
<p>Type: Full-length Presentation</p>

<hr/>
</details>
 

<details><summary><strong>A Modular SDK in A Fragmented Landscape</strong></summary>

#### Abstract

Web SDKs need to provide a host of capabilities & are a contradiction in terms - on the one hand, they need to be "fully baked" & "closed" in order to provide a uniform API. On the other hand, they need to be flexible in order to support future development & a wide range of clients.

While this can be achieved by "baking" a custom SDK per client - this is not very scalable (nor practically applicable with a business in exponential growth). In order to be able to deliver on the promise of modularity, we wanted to enable users to decide which capabilities they want to enable, without having to define this in advance.  This talk will dive into the development methodology we used in-house to support this, & eventually, how we serve multiple SDKs in a uniform manner to a diversity of clients.

Speakers: [Shimi Bar](/speaker-profiles.md#shimi-bar), [Liron Cohen](/speaker-profiles.md#liron-cohen)
<p>Type: Full-length presentation</p>
<hr/>
</details>

<details><summary><strong>Micro-frontends: Is it a Silver Bullet?</strong></summary>

#### Short Description
Micro-frontends - is it just a hyped out buzzword or do they live up to their promise? This talk will cover how we architected our micro-frontends solution, the challenges we encountered, how we overcame them - and answer the ultimate question, are micro-frontends worth the hype?

#### Long Description
Micro-Frontends are gaining a lot of traction these days as the “silver bullet” solution to the former monolith project architecture, essentially the frontend variation on microservices. If you’re not familiar with micro-frontends, and how to implement them in your environment, you might find yourself asking “am i missing out on something important?” or “what does this even mean?”

In this talk, I will walk you through our journey where we found ourselves accumulating independent monolithic frontend stacks - and had to find a better way to manage and maintain these stacks in a hyper-growth environment. We will present how we migrated to this loosely-coupled architecture of independent projects and eventually were able to grow to 25+ micro-frontend projects that helped us optimize our development and achieve our goals more rapidly, the challenges we encountered that made our lives miserable - and how we overcame them, and finally will try to answer the ultimate question “are micro-frontends really a silver bullet?

Speakers: [Shimi Bar](/speaker-profiles.md#shimi-bar), [Liron Cohen](/speaker-profiles.md#liron-cohen)
<p>Type: Full-length Presentation</p>
<hr/>
</details>


<br/>

#### Mobile
<hr/>

<details><summary><strong>How a Seemingly Small Issue Can Make your Users Zombies</strong></summary>

#### Talk Description
Our SDK is used by more than 130K+ applications, and is what delivers all of our incoming traffic from the different platforms being used.  Recently, we encountered a critical issue, that prevented any incoming traffic from Android devices to AppsFlyer.

As part of our anti-fraud solution, we use the Dexguard algorithm to prevent reverse engineering, where the large majority of our 130K apps use the same tool. However, due to the issue, some source files in the SDK were corrupted on the client-side, breaking the backbone of the SDK, basically shutting down the outgoing mobile SDK traffic to AppsFlyer.  This talk will dive into the timeline of the incident, decisions we took in real time to mitigate the incident & the lessons we learned that we think can help others in a similar situation.


Speakers: [Maxim Shoustin](#)
<p>Type: Full-length Presentation, Post-Mortem</p>
<hr/>
</details>

<br/>

### [Culture Talks](#culture)
<hr/>


<details><summary><strong>How we Built a High Performing Engineering Organization by Hard Resetting our Hiring & Onboarding Processes</strong></summary>

#### Short Description
One of the long-standing anomalies in the tech industry is the focus on engineering products, but less so on engineering organizational culture.  Building great products, and hiring excellent engineers is a by-product of culture that needs to be constantly improved and evaluated.

#### Long Description
Have you ever found yourself struggling to build an engineering organization that is quality-driven with consistently great results?  When we analyzed why we didn't feel our organization was performing at the level we had anticipated, we reverse engineered this to fundamental issues with our culture.  Once we started working on this it had a ripple effect to our hiring process & then our onboarding process as well.  This talk will dive into how we refactored our hiring & onboarding to set up new hires for success from day one. This ultimately delivered a well-oiled high performing engineering organization through a practically applicable methodology that is easily replicable. This not only enabled us to improve the quality of our hires, but also retain excellent talent in the long-term.

Speakers: [Gilad Katz](/speaker-profiles.md#gilad-katz)
<p>Type: Full-length Presentation</p>
<hr/>
</details>

<details><summary><strong>How We Went All-In on Reducing Technical Debt - And Lived to Tell the Tale</strong></summary>

#### Short Description
A common modus operandi in many companies is "if it ain't broke - don't fix it" - this talk will demonstrate how to change this mindset to create higher performing engineering organizations.

#### Long Description
Imagine the technical debt of a startup in exponential growth for six consecutive years (growing from five engineers to 160 over this period, and from 10M daily events to over 70B). During this time, and up to the last 2 years the team focused on product expansion with a “if it ain't broke don’t fix it” attitude, resulting in inherent bugs, system instability & more than 80% of our team focused on maintenance. This will be a tale of how we went all-in on reducing technical debt by allocating more than 70% of the team for 1.5 years to reduce debt. I will share how we rewrote our core engine - at a time of extreme growth, while virtually putting on hold the rollout of any new features - a brave move in a competitive market. After two years into the process we managed to reduce the maintenance effort, number & severity of production issues - with the upside of increasing our velocity significantly. This was all made possible by instilling a culture of craftsmanship that was part of the re-engineering process, that has only been strengthen through this process.


<p>Speakers: [Gilad Katz](/speaker-profiles.md#gilad-katz)</p>
<p>Type: Full-length Presentation</p>
<hr/>
</details>

<details><summary><strong>Artificial Insanity: How to Keep Calm and Combat Imposter Syndrome</strong></summary>

#### Talk Description
We've all suffered from imposter syndrome from time to time.  But it turns out imposter syndrome has some really clear patterns, and there are actually a few simple tips and tricks to start appreciating ourselves more.  This talk will provide some tools to help you keep calm and focus on your small successes  that eventually translate to big successes - similar to Kaizen.  And that all this starts with allowing ourselves to be human first and foremost.

Speakers: [Sharone Zitzman](/speaker-profiles.md#sharone-zitzman)
Type: Ignite / Lightning Talk (5-10 Minutes) or Full-Length
<hr/>
</details>
<br/>

### [Cloud and Platform Engineering Talks](#cloud)
<hr/>
<br/>

<details><summary><strong>Baptism By Fire - Why Production Failures Make you a Better Developer</strong></summary>

#### Short Description
Taking end-to-end ownership of your production code, enables you to understand the operational aspects even the best code encounters - and will contribute to improved coding practices.

#### Long Description
As developers, we are constantly focused on writing elegant and cutting edge code, however, meaningful code eventually lives 99% of its life in production, and becomes “someone else’s problem”. As with all code, issues are bound to arise and someone will have to deal with them (probably at 3 AM after a pagerduty call). At AppsFlyer all developers are expected to own their code end-to-end, to create a greater sense of commitment to its quality, and enable more rapid turnaround on debugging issues. Three years of being on the on-call rotation for mission critical services at AppsFlyer have taught me some hard lessons, but made me a better developer along the way. In this session I’ll dive into best practices for how to approach production issues as developers, some of the lessons I’ve learned about a developer managing production code, and how this ultimately makes us (much) better coders.

Speakers: [Adi Belan](/speaker-profiles.md#adi-belan)
Type: Full-length Presentation
<hr/>
</details>
  
<details><summary><strong>Hacks of Kindness in the Turbulent Cloud</strong></summary>

#### Short Description
Efficiently managing large fleets on the cloud from the networking to security & even cost management often takes years to cultivate expertise in, and optimize.  

#### Long Description
Efficiently managing large fleets on the cloud from the networking to security & even cost management often takes years to cultivate expertise in, and optimize.  This is especially true when leveraging opportunistic cloud capabilities such as spot instances at scale, which in itself requires intelligent & reliable auto-scaling for a large-scale production operation - which in our case means serving more than 80B+ requests daily, while ingesting more than 90TB a day. This talk will provide you with some effective hacks of the trade that we learned in real time & through years of optimizations, to help survive the turbulent & continuously evolving cloud world, including: 

- Serving 80B requests on one endpoint with multiple ELBs
-  Whitelisting many IPs for your customers without compromising security
-  Managing spot instances like a champ
- Bypassing DHCP options set
- Balancing subnet IP allocation
- Doing it right: Bind & Route53
- Controlling co-location in a cluster
- Balancing traffic out with multiple NAT gateways
- Connecting to multiple regions via one VPN
- Tags & Cost management

Speakers: [Ariel Moskovich](/speaker-profiles.md#ariel-moskovich)
<p>Type: Full-length Presentation</p>
<hr/>
</details>


<details><summary><strong>Googlies, Grubbers, Lollies! How cricket helped us improve our throughput by 200%</strong></summary>

#### Short Description
Overnight the traffic to our postback sender service suddenly increased by 50% because of one of our client's apps.  This will be a story of how we learned to handle these spikes in real time, and even improved throughput and performance in the long run.

#### Long Description
I never imagined I’d know who Indian cricket star Rohit Sharma is, but then traffic to our real-time HTTP request sender service suddenly increased from 20 to 40 million events per minute. The reason? An app streaming the first game of the Indian cricket season. While growth is a good thing, we found ourselves unprepared for this sudden spike & needed to scramble. Initially we just threw money at the problem, but this wasn't sustainable. My talk will describe how we found low-cost, programmatic and architectural solutions to this problem and how we prepared ourselves to handle massive spikes like these on top of our existing 70 billion events per day. I'll explain our process of profiling, performance enhancement techniques, and some important lessons learned along the way.

Speakers: [Ethan Pransky](/speaker-profiles.md#ethan-pransky)
Type: Full-length Presentation, Post-Mortem
<hr/>
</details>



<details><summary><strong>Improving Developer Velocity & Autonomy with Deploy & Destroy Testing Environments</strong></summary>

#### Short Description
On demand testing environments fundamentally changed the quality & velocity of how we ship code - and you can too!

#### Long Description
One of the critical factors for development velocity is software correctness. Our ability to develop and ship new features fast is bound by our ability to validate several aspects of the change: 
* Does the feature meet the requirements? 
* How does the feature affect existing code, and how can it affect the production environment? With continuous codebase growth and new features being added, naturally our productivity decreases, and our need to improve the guarantees for quality and correctness increase.

In this talk, I’ll focus on testing environments: why developers need a self-service platform to create a full functioning environment on-demand, how such environments should be managed, and how can one restore part of the lost velocity. I’ll cover an internal system we use at AppsFlyer called ‘Namespaces’ that addresses the issue with the help of Mesos / Marathon, Docker, Traefik, and Consul.

Speakers: [Michael Arenzon](/speaker-profiles.md#michael-arenzon)
Type: Full-length Presentation
[Recording](#)
<hr/>
</details>


<details><summary><strong>Migration from BitBucket to GitLab</strong></summary>

#### Talk Description
AppsFlyer migrated its entire git operation, with production clients from BitBucket to Gitlab.  This talk will dive into what was involved with the migration process - from building the architecture through selecting the tooling and eventually how we built our very own self-serve API abstraction over the GitLab API.  Some of the points the talk will review:
• The migration process - from Mercurial to Git, how to move all projects, how to get developer buy-in and the lessons learned during the process
• Architecture - How we built it, the challenges we faced, how we built our DR solution, alongside the distributed backup  
• Building monitoring for the environment
• Self-service, tooling & and some pro tips and tricks for working with Gitlab
While this will be a talk about our Gitlab implementation, it will also provide key takeways for making such a migration in a large-scale engineering organization.


Speakers: [Elad Leev](/speaker-profiles.md#elad-leev)
<p>Type: Full-length Presentation</p>
<hr/>
</details>


<details><summary><strong>Graphite Infrastructure & Scaling Out Metric Flows </strong></summary>

#### Talk Description
Graphite is the de-facto standard for metrics storage and visualization, which allows every developer to get a fast and clear view of application performance, connections with other parts of the stack, and troubleshoot it easily. 

But if you do not cook it right, it could be slow and frustrating. In this talk we will share our methods for metrics processing, we will look under the Graphite hood and will concentrate on high load & multi-region Graphite stack setup within AWS. We will take a look at all the ways that metrics are passed from the application to a point on the graph.

We will speak about the main problems with the Graphite stack that many teams struggle with, when it comes to scale, our processes for dealing with these challenges, and making the most of the data.  


Speakers: [Vladimir Mevzos](#)
Type: Full-length Presentation
</details>


  
<!--
<details><summary>...</summary> -->

<!-- #### Short Description -->

<!-- #### Long Description -->


<!-- Speakers: [#](#)
Type: Full-length Presentation
</details>
<p>  -->
