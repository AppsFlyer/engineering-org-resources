
Quick Links: [Home](https://github.com/AppsFlyer/engineering-org-resources), [Speaker Bios](/speaker-profiles.md)

**AppsFlyer Engineering has expertise in many areas from data engineering & science, a diversity of programming languages, platform and cloud operations as well as, culture & psych talks. You can find the different abstracts below.**  

We are happy to be invited to speak in any forum - conference, meetup, community event - so be sure to reach out.  Follow us on Twitter: [@appsflyerdev](https://www.twitter.com/appsflyerdev) and our [AppsFlyer Engineering meetup group](https://meetup.com/appsflyer).

<hr/>

### [Big Data Talks](#big-data)
<hr/>

<details><summary><strong>Applying Probabilistic Data Structures to Real Time Systems</strong></summary>

#### Short Description
Building solutions around large data sets with near real time response time is no easy feat. This requires the practical application of computer science theory to do so with minimal latency and while remaining fresh and precise.

#### Long Description
As software organizations are required to handle increasing volumes of data, probabilistic data structures and algorithms have been put to use more widely in order to find approximative solutions to problems that would be computationally prohibitive otherwise.

At AppsFlyer, we ingest a daily 80+ billion events sent by our users, which come into our system without any schema or predefined structure. When we set out to build a new data segmentation product, which allows our clients to segment their users based on these billions of events – according to any logical criteria they wish to specify – we were tasked with the daunting challenge of offering them a near real time interactive dashboard. An extremely large computational undertaking at minimal latency.

This posed an interesting challenge from both computer science and engineering perspectives, things we needed to consider:

* Which data structure is most appropriate?
* Which data model would allow us to compose any number of criteria when event schemas are unknown in advance and ever changing?
* How do you implement aggregations such as group-by over probabilistic data?
* What database should we pick to allow for fast and scalable access to our data structures?
* How do you do this reliably, high precision and freshness?

This talk will discuss how we built a system which allowed us to solve this problem over massive data sets with technologies such as Kafka, Spark, HBase and Theta Sketches.

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

<details><summary><strong>Managing Your Kafka in an Explosive Growth Environment (Var 1)</strong></summary>

#### Short Description
Kafka, many times is just a piece of the stack that lives in production that often times no one wants to touch - because it just works. At AppsFlyer, Kafka sits at the core of our infrastructure that processes billions of events daily.

#### Long Description
Kafka, many times is just a piece of the stack that lives in production that often times no one wants to touch – because it just works. At AppsFlyer, Kafka sits at the core of our infrastructure that processes billions of events daily.

This talk will share how we built our microservices architecture with Kafka as its core piece to support 70B+ requests daily. With continuous growth we needed to “learn on the job” how to improve our Kafka architecture by moving to the producer owner cluster model, breaking up our massive monolith clusters to smaller more robust clusters, and migrating from an older version of Kafka with real-time production clients & data streams. The talk will outline best practices for leveraging Kafka’s in-memory capabilities & built-in partitioning, as well as some of the tweaks and stabilization mechanisms that enable real-time performance at web-scale, alongside processes for continuous upgrades and deployments with end-to-end automation, in an environment of constant traffic growth.

Speakers: [Alon Gavra](/speaker-profiles.md#alon-gavra)
<p>Type: Full-length Presentation</p>
<hr/>

</details>


<details><summary><strong>So You've Inherited Kafka...Now What? (Var 2)</strong></summary>

#### Talk Description
Kafka, many times is just a piece of the stack that lives in production that often times no one wants to touch - because it just works. At AppsFlyer, a mobile attribution and analysis platform that generates a constant "storm" of 70B+ events (HTTP Requests) daily, Kafka sits at the core of our infrastructure.  

Recently I inherited the daunting task of managing our Kafka operation and discovered a lot of technical debt we needed to recover from if we wanted to be able sustain our next phase of growth.  This talk will dive into how to safely migrate from outdated versions, how to gain trust with developers to migrate their production services, how to manage and monitor the right metrics and build resiliency into the architecture, 
as well as how to plan for continued improvements through paradigms such as sleep-driven design, and much more.  

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

Speakers: [Morri Feldman](/speaker-profiles.md#morri-feldman), [Yulia Trakhtenberg](/speaker-profiles.md#yulia-trakhtenberg)
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

<details><summary><strong>Spark Optimization Models</strong></summary>

#### Abstract
While an extremely powerful technology, Spark many times requires a lot of trial and error to get the configurations & optimizations just right - especially at scale.  This talk will walk you through some of the challenges we encountered at AppsFlyer where we ingest 90TB / day and perform a diversity of data processing operations on this huge data set.  Some of the interesting optimizations we’ve employed include salting across multiple Spark clusters, and some of the anomalies we’ve encountered have been around areas of serialization and  certain map/reduce models.  This talk will dive into how we tackled each of these, and some of the outcomes.

  
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

<details><summary><strong>Unleash the Power of the REPL</strong></summary>

#### Description
Clojure provides some powerful tools out of the box for development and debugging. The best known that we all probably use is the REPL (Read Evaluate Print Loop) that enables developers a much easier way to interact with a running Clojure project and gives us more code clarity by making it possible to find the source of bugs much more quickly, and ultimately understand the code and flow better.  In this talk I will go back to the basics and dive into how to best leverage REPL a tool that every Clojure developer uses on a daily basis, with real code examples, and get the most out of leveraging the stack trace, as well as code inspection with prints & logs.  By better understanding the power of these tools, we will be able to drill down and isolate the issues so we can debug them via the REPL and solve them more quickly - and hone our Clojure skills.



Speakers: [Dana Borinski](/speaker-profiles.md#dana-borinski)
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

<details><summary><strong>Lessons in Building a System that Processes More than 80 Billion Events Daily
</strong></summary>

#### Talk Description
AppsFlyer’s mobile attribution and analysis platform is used by the biggest and most popular applications on Earth, generating a constant “storm” of 80B+ events (HTTP Requests) on their microservices, cloud based platform daily. In this talk, we will share the technological choices which include Clojure as our leading backend language - and the decisions to migrate from Python for improved multi-threading and concurrency.

The backend was to built to be a robust system based on a diversity of open source tooling such as: Kafka, RabbitMQ, Aerospike, Redis and a host of proprietary in-house developed tools and services that enable the testing and adoption of new data technologies, continuous deployment, and large-scale monitoring of the system - including open sourcing production libraries for interoperability with core technologies.

This talk will also dive into AppFlyer's real-time back-end architecture & functional programming philosophy, what it is like to be a developer at AppsFlyer, and overall attitude towards performance, redundancy and resiliency for processing 50 Million events/minute at an average latency of hundreds of milliseconds per event.

Speakers: [Nir Rubinstein](/speaker-profiles.md#nir-rubinstein), [Morri Feldman](/speaker-profiles.md#morri-feldman)
<p>Type: Full-length Presentation</p>
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


<details><summary><strong>When Choosing the Wrong Thread Causes Complete Chaos</strong></summary>

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


<details><summary><strong>Reactive Programming by Example</strong></summary>

#### Talk Description
The reactive manifesto is meant to guide you in building Responsive, Resilient, Elastic (scalable), and Message Driven systems.<br/>

But these are all bombastic words which are quite meaningless without a good context or good examples.<br/>

This talk will walk you through a story of improving a real life service, bringing it to perform well, and link the steps to the reactive manifesto cornerstones.<br/>
 

Speakers: [Eran Harel](/speaker-profiles.md#eran-harel)
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


Speakers: [Hadas Yaakobovich](/speaker-profiles.md#hadas-yaakobovich)
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

<details><summary><strong>go-grpc-channelz: a Go based UI for gRPC's channelz's implementation</strong></summary>

#### Short Description
gRPC is a modern, highly capable RPC system. But not without it’s complexities. go-grpc-channelz observe gRPC clients and servers and provides a prism into the current state of gRPC connections down to socket level events.

#### Long Description
[go-grpc-channelz](https://github.com/rantav/go-grpc-channelz) is my open source project in Go to provide better observability into gRPC’s current state of connections (channels).

gRPC is a robust and highly scalable RPC system. It abstracts actual socket connections through the channel abstraction. Channels represent load-balanced, possibly auto-discovered remote servers. Gaining visibility into the current state of gRPC channels is priceless. Think `netstat` for your gRPC server, but one which understands the full blown semantics of gRPC. Channelz is a gRPC spec that exposes the state of the above mentioned channels. go-grpc-channelz, written in go, is a pluggable UI layer which uses the channelz gRPC API to query and display the current state of gRPC connections. With three lines of code your gRPC service written in Go can gain useful observability.

In this session you’ll learn about some of the interesting design concepts of gRPC and how go-grpc-channelz can be used to expose some of its intrinsics.

Speaker: [Ran Tavory](/speaker-profiles.md#ran-tavory)
<p>Type: Full-length Presentation</p>
<hr/>
</details>

<details><summary><strong>go-archetype: effective project prototypes in your native language</strong></summary>

#### Short Description
go-archetype is sed on steroids. And a ton more. Create project prototypes in your natural language (Go/Java/C/etc), then your users interactively feed variables to generate new projects. No need to learn a template language and maintain a template codebase. Your Go/Java/C project is the template


#### Long Description
Architects? Tech leads? How many times have you looked at your codebase and thought “oh my, each new project is it’s own snowflake, I wish I had a useful template project we could all use”?

[go-archetype](https://github.com/rantav/go-archetype) is my open source project implemented in Golang providing a natural and language native flow to create project prototypes. With go-archetype you create a project archetype (aka blueprint) and a set of simple transformation, think `sed` on steroids.
Search and replace, use go text templates to synthesize user inputs, prompt users for input, conditional inclusion of files or parts of files…

Fast growing engineering organizations create new projects day in day out. How do you help developers maintain common project structure? How do you help developers scaffold an initial project structure? How do you help developers use useful default libraries, middlewares, configuration and settings out of the box?
With go-archetype it’s easy: You define a blueprint project, which is just a regular Go project, no extra templating language. And then a set of transformations, e.g. ask the user for their project name and replace here, here and here, ask the user for their project package and replace here and there, ask the user whether they want to use an HTTP router and include GorillaMux only if she answered “yes”.

go-archetype is written in go but in fact, can be used by blueprint authors for any language, be it JS, Java, C etc. It’s language agnostic. Example open source project using go-archetype: https://github.com/rantav/go-template

The motivation to creating go-archetype came after investing in several other templating frameworks and not finding what I want. Most other frameworks require you to write your blueprint project in a specialized language, be it react templates or other. But this approach is less than ideal since it forces you to maintain two versions of your blueprint, one in your natural language (e.g. Go) so that you can develop and test real actual code and make sure it compiles and passes tests, and another in a “shadow” template language, e.g. React or other templating language, for the sake of templating. go-archetype allows you to maintain just a single codebase and that is a big maintainability win!

Speaker: [Ran Tavory](/speaker-profiles.md#ran-tavory)
<p>Type: Full-length Presentation</p>
<hr/>
</details>
<br/>

#### Frontend & Fullstack
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

<details><summary><strong>The Power of Templates - How we Created a Clojure\React Symbiot in a Couple Minutes</strong></summary>

#### Description
In most engineering projects, the task of creating a new service often begins with the tedious objective of setting up the basics - adding configurations, creating the basic server files, initializing states and laying down the foundations for the innovation that will come on top. But what if we had a jump start advantage - set up everything in 1 minute, and instantly jump to the creativity step? Clojure Templates allows setting up a backend service in an instant. On the front-end side, Facebook's create-react-app allows you to do the same with React.js. Here I suggest a methodology for joining the power of Clojure with the magic of React.js by templating a configurable Clojure-React client\server architecture in less than a minute.


Speakers: [Dror Davidi](/speaker-profiles.md#dror-davidi)
<p>Type: Full-length Presentation</p>
<hr/>
</details>

<details><summary><strong>JavaScript Module System - What is it?</strong></summary>

### Short Description 

There’s always a lot of noise in JavaScript ecosystem around modules, but despite the hype, it’s not always apparent how to best leverage these. This talk is going to change that.


#### Long Description
JavaScript modules are now supported in all major browsers and soon in NodeJS 13, but are they really?

While they are supported in most of the major browsers, do we actually use them?

Why do we even need them and how were they brought about? And what did we do before modules existed?

In this talk, I’d like to demonstrate through common examples how we’ve seen & used modules before they had a name, best practices for how to use them today, and take a look at where the future will most likely take us.


Speakers: [Omer Herera](/speaker-profiles.md#omer-herera)
<p>Type: Full-length Presentation</p>
<hr/>
</details>


<details><summary><strong>The JavaScript Time Machine - Past, Present, to Infinity and Beyond</strong></summary>

### Short Description 

JavaScript has come a long way since being introduced in 1995, & so have we as engineers.

Come with me on this journey through time with JS & see how we have moved from using best practices adopted from other langs-to where JS took control all the way through the deployment & build processes today.

#### Long Description
JavaScript has come a long way since being introduced in 1995, and so have we as engineers. We’ve grown with JavaScript, and in this talk I’d like to demonstrate through common examples how we used to deploy and compile our JS once upon a time, using techniques that now will look weird, incorrect, like bad practices or even just funny.

Come with me on this journey through time with JavaScript, and see how we have moved from using best practices adopted from other languages, and techniques to compile JS to see how NodeJS/JavaScript ultimately took control all the way through the deployment and build processes for JavaScript today, and now we can’t live without these advancements.

Many times we forget that there is plenty to learn from history, and expertise takes decades to cultivate, and how the tools available in the community have evolved, learn why there are so popular, when to use them and when to avoid them, and what you can take from these years of learning with JavaScript to become better engineers in your day to day work.

Speakers: [Omer Herera](/speaker-profiles.md#omer-herera)
<p>Type: Full-length Presentation</p>
<hr/>
</details>

<details><summary><strong>Same Code, Faster Application</strong></summary>

### Short Description 
Complex React applications can affect performance and load time significantly. This talk will dive into how to optimize large and complex Javascript payloads and improve performance by orders of magnitude.

#### Long Description
A complicated React application usually consists of several components, utility methods, and third-party libraries. This can become especially complex, and can affect the user directly in the form of loading time, when shipping a large JavaScript payload (particularly on old devices and with weak network connections). In this talk, I will discuss ways to combat this complexity through a method called code splitting. I will start by explaining what code splitting actually is, and how we can use this method to split our payloads into multiple bundles with excellent tools such as React.Lazy and React.Suspense, and then ultimately only ship this to the user when they need it, improving load time significantly alongside other complexities that may arise from large payloads.

Speakers: [Roei Berkovich](/speaker-profiles.md#roei-berkovich)
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


Speakers: [Maxim Shoustin](/speaker-profiles.md#maxim-shoustin)
<p>Type: Full-length Presentation, Post-Mortem</p>
<hr/>
</details>

<details><summary><strong>Does scale matter?</strong></summary>

#### Short Description
This talk will dive into how to motivate and inspire our team together with developing high quality software for more than 130,000 apps?! 


#### Long Description
Today, the AppsFlyer SDK runs on more than 7 billion mobile devices. So what's actually involved with developing software for more than 130,000 apps?!
This talk will dive into what our day to day work looks like, and how we manage risks. Is it possible to write code without business-critical bugs in production? And for a matter of perspective - would three bugs in three years sound like a lot or a little? Does the system we're trying to build have fault tolerance?
I’m going to talk about how we motivate and inspire people, what challenges we face, the tools we use to achieve high-quality software, tips, and tricks.
How do we deal with stressful situations and how we stay cool through it all.



Speakers: [Maxim Shoustin](/speaker-profiles.md#maxim-shoustin)
<p>Type: Full-length Presentation (30-45 min)</p>
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


Speakers: [Gilad Katz](/speaker-profiles.md#gilad-katz)
<p>Type: Full-length Presentation</p>
<hr/>
</details>


<details><summary><strong>Scaling Your Engineering Organization: Get Serious with Training</strong></summary>

#### Talk Description
When you're a startup in hyper growth - sometimes one of the biggest challenges is actually onboarding new hires & quickly ramping them up on the tooling & stack. This becomes increasingly complex with a dynamic engineering organization that is not only built around agile delivery concepts with hundreds of thousands of real-time production users, but also a big data engineering organization that ingests more than 90TB of data daily. The need to support the product infrastructure around the clock, while ingesting & processing a constant stream of big data daily delivering real time access to complex segmented data, a diversity of data persistence & storage demands, as well as data models is a lot for a new hire to learn in a short amount of time. All this, alongside new programming languages & company culture. This talk will walk you through how we built a realistic training program that covers the diversity of in-house tooling & platforms - including Spark & Hadoop for big data operations, LTV databases alongside time series databases, S3, BigQuery and even the not very common choice of programming language - Clojure - to top it all off, with some Python, Golang & Scala. With the trial & error and continuous learning process we take from each training, we've managed to successfully onboard 10+ hires a month without compromising our engineering velocity nor platform robustness.

Speakers: [Morri Feldman](/speaker-profiles.md#morri-feldman), [Ronen Cohen](/speaker-profiles.md#ronen-cohen), [Nir Rubinstein](/speaker-profiles.md#nir-rubinstein)

<p>Type: Full-length Presentation</p>
<hr/>
</details>

<details><summary><strong>Artificial Insanity: How to Keep Calm and Combat Imposter Syndrome</strong></summary>

#### Talk Description
We've all suffered from imposter syndrome from time to time.  But it turns out imposter syndrome has some really clear patterns, and there are actually a few simple tips and tricks to start appreciating ourselves more.  This talk will provide some tools to help you keep calm and focus on your small successes  that eventually translate to big successes - similar to Kaizen.  And that all this starts with allowing ourselves to be human first and foremost.

Speakers: [Sharone Zitzman](/speaker-profiles.md#sharone-zitzman)
<p>Type: Ignite / Lightning Talk (5-10 Minutes) or Full-Length</p>
<hr/>
</details>

<details><summary><strong>How the Pillars of Community Map to the Pillars of High Performing Organizations</strong></summary>

#### Talk Description
The pillars of good community leadership are built around rallying people to a common purpose, building a meritiocracy so that the most masterful of contributions are those that prevail, and providing the value that people expect, or have the autonomy to move on from your community as well.  Leading teams to inspire them to have purpose, strive for mastery and do so autonomously essentially map to the same values.  This talk will dive into how you can build your company around core community values to build a high-performing organization, cultivate employee engagement and retention in the long term.

Speakers: [Sharone Zitzman](/speaker-profiles.md#sharone-zitzman)
<p>Type: Ignite / Lightning Talk (5-10 Minutes) or Full-Length</p>
<hr/>
</details>

<details><summary><strong>Game of Open Source: A Tale of Hype & Mire</strong></summary>

#### Talk Description
There is no question that the going is tough when it comes to open source projects. Building the excitement, community and hype is an undertaking unto itself - let's not talk about monetization. Often times, just as your project is starting to get off the ground and generate real business - newer and cooler disruptors enter the playing field - and it gets hard to keep the momentum going. This talk is going to give some real world insight on what's involved in really building a sustainable open source project, even when the hype is dwindling and the dust settles. This will be based upon lessons learned from leading the Cloud Native & OSS community in Israel, as well as the Cloudify community as my former day job.


Speakers: [Sharone Zitzman](/speaker-profiles.md#sharone-zitzman)
<p>Type: Ignite / Lightning Talk (5-10 Minutes) or Full-Length</p>
<hr/>
</details>

<br/>

### [Cloud, Platform and Security Engineering Talks](#cloud)
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
<p>Type: Full-length Presentation, Post-Mortem</p>
<hr/>
</details>

<details><summary><strong>Kafka Mirror Tester: Go and Kubernetes Powered Test Suite for Kafka Replication</strong></summary>

#### Short Description
Abstract: Inspired by the Jepsen series of database test suites I create kafka-mirror-tester, a cross Atlantic automated test suite for Kafka mirroring using Golang and Kubernetes. There, I said k8s, need I say more? 

#### Long Description
[kafka-mirror-tester](https://github.com/AppsFlyer/kafka-mirror-tester) is an automated test suite for kafka mirroring used at appsflyer to test the correctness and effectiveness of various kafka mirroring tools, namely [uReplicator](https://github.com/uber/uReplicator) and [Brooklin](https://github.com/linkedin/brooklin). kafka-mirror-tester automates the tasks of datacenter setup by creating two k8s clusters, one on each side of the Atlantic, then setting up kafka clusters at both sides, then setting up replication in between, running specialized Golang producers and consumers at both sides and then injecting faults to test durability. All done hands-free, completely automated. With lovely prometheus & grafana dashboards.

**Distributed systems. Are. Hard.** At AppsFlyer Kafka is the backbone and part of my team’s work on multiple datacenter deployment was making sure we are able to mirror (replicate) kafka messages across datacenters. This kind of things you want to test before reaching production and you want to be able to simulate failure scenarios such as broker down, replicator down, slow network etc under the neon light so that you’d know what to expect in reality. To achieve that in a completely reliable and repetitive manner and inspired by the [Jepsen](https://jepsen.io/) series of semi-automated database test suites I’ve set our to create our own automated kafka mirroring test suite, Kubernetest, Prometheus, Golang and more in my toolbelt. In this session you’ll learn about the interesting challenges of automating database and Kafka in particular tests, stressing out the system and making sure everything works correctly, and then tearing apart the system by injecting failure and observing the points where it breaks. This is fun!

Speakers: [Ran Tavory](/speaker-profiles.md#ran-tavory)
<p>Type: Full-length Presentation</p>
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
<p>Type: Full-length Presentation</p>
<p>[Recording](https://www.youtube.com/watch?v=sI_IrFTbWbo&t=248s)</p>
<hr/>
</details>


<details><summary><strong>Migration from BitBucket to GitLab</strong></summary>

#### Talk Description
AppsFlyer migrated its entire git operation, with production clients from BitBucket to Gitlab.  This talk will dive into what was involved with the migration process - from building the architecture through selecting the tooling and eventually how we built our very own self-serve API abstraction over the GitLab API.  Some of the points the talk will review:
* The migration process - from Mercurial to Git, how to move all projects, how to get developer buy-in and the lessons learned during the process
* Architecture - How we built it, the challenges we faced, how we built our DR solution, alongside the distributed backup  
* Building monitoring for the environment
* Self-service, tooling & and some pro tips and tricks for working with Gitlab

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


Speakers: [Vladimir Mevzos](/speaker-profiles.md#vladimir-mevzos)
<p>Type: Full-length Presentation</p>
</details>

<details><summary><strong>Building Guardrails through Partnerships with the Development Team </strong></summary>

#### Talk Description
Modern engineering groups want to work with the most nifty tech stacks, apply DevOps practices of agility and rapid deployment in the form of CI/CD and all this without compromising security.  But working with engineering teams is always a challenge, this talk will answer some of the most common questions we encounter in our field, such as: <br/>
Why is working with engineering teams always hard for security? How can we make the engineering team care about security without the headache? How do you build a strong relationship with engineering teams without compromising security and productivity? 

All of these questions actually have a pretty similar answer, however achieving this, is never a simple undertaking.  This talk will dive into all of this, including:
1. Presentation of the different engineering groups and how they work together
2. Main challenges
3. Past approach and the setbacks 
4. Learning to optimize and work together - introducing our new approach
5. Real world examples for how this is done in a real, big data, DevOps-centric organization
6. Future plans

This talk will provide real practical tools for how to do this in a modern engineering organization.


Speakers: [Guy Flechter](/speaker-profiles.md#guy-flechter)
<p>Type: Full-length Presentation</p>
</details>

<details><summary><strong>Free Your SSLF and the Resty Will Follow</strong></summary>

#### Short Talk Description
Branded URLs are easy to implement unless SSL is required.  We wanted to provide our customers with an easy solution that will work with our existing clicks solution, requiring minimum effort from them to implement, all while not changing our existing architecture and system.
This is how we used LetsEncrypt for easy, simple, scalable solution.

#### Long Talk Description
Our customers need branded URLs in order to maintain their brand equity, improved security practices, and increase click-through rates. In a world where becoming secure is mission-critical, HTTPS is a must.<br/>

However, there really is no out of the box solution for apply HTTPS at scale, so we found ourselves having to build our own solution.<br/>

In order to implement SSL for our customers, a complicated security process was required involving different groups within the organizations both on the client's side, and within our own company.<br/>

This talk will dive into how we solved this problem with Letsencrypt, Docker, Redis, Nginx, resty-Lua and and autossl module.


Speakers: [Dana Borinski](/speaker-profiles.md#dana-borinski)
<p>Type: Full-length Presentation</p>
</details>


<details><summary><strong>Hacking the Automotive Cloud</strong></summary>

#### Short Talk Description
Connected vehicles are the future of the automotive industry, however, the cloud environment for the automotive industry presents a dangerous attack surface with real-life consequences.

#### Long Talk Description
Connected vehicles are the future of the automotive industry, however, the cloud environment for the automotive industry presents a dangerous attack surface with real-life consequences.

In this talk I will share my experience of breaking into automotive cloud environments - from OSINT to post-exploitation activity. You will gain an understanding of the main interfaces used in the automotive cloud including supplier integrations and we will explore the differences between normal and automotive cloud environments.

This will be a technical presentation that will provide real life examples of: 
* From zero to hero – full backend control with examples
* Common fails which enable jumping between networks 
* Dangers of connected cars - taking control of a car from the cloud 
* How to break a production line
* Cloud credential leakage


Speakers: [Rotem Bar](/speaker-profiles.md#rotem-bar)
<p>Type: Full-length Presentation</p>
</details>


<!--
<details><summary>...</summary> -->

<!-- #### Short Description -->

<!-- #### Long Description -->


<!-- Speakers: [#](#)
Type: Full-length Presentation
</details>
<p>  -->
