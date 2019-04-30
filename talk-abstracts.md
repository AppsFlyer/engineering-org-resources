## AppsFlyer Engineering has expertise on a diversity of topics, find the 



### [Big Data Talks](#big-data)

<details><summary>From Theory to Practice: Segmenting Big Data with Probabilistic Data Structures</summary>

#### Short Description
Building solutions around large data sets with near real time response time is no easy feat. This requires the practical application of computer science theory to do so with minimal latency and while remaining fresh and precise.


#### Long Description
As a company that ingests large amounts of data (more than 90TB/day), as part of our core functionality, AppsFlyer for ways to empower users to leverage their data by providing access to data sets for finer-grained analysis and segmentation to optimize targeting. Access to large data sets, especially raw data is often times an I/O intensive task, making it a slow and memory-straining task. Therefore, when setting out to provide such functionality, we were faced with a challenging engineering problem which also required us to apply theory from the field of Computer Science.

When we decided to launch a new service called audiences that would enable users near real time segmentation of relevant audiences based on different filters – we needed to examine how to provide data as reliably as possible with minimal latency. This talk will dive into how we built the solution taking into account how to provide the freshest most precise data, while persisted to easily accessible storage. This required qualifying the right probabilistic data structure, modeling the solution for rapid data access – through its schema and flow and leveraging the right tooling – including Spark, Hadoop and HBase, and the challenges involved with doing so with a jungle of unstructured massive data sets.

Speakers: [Ronen Cohen](#)
Type: Full-length Presentation
</details>
<p>

<details><summary>Journey to Real-Time Analytics in Extreme Growth</summary>

#### Short Description

At AppsFlyer we have been finding ourselves the victims of our own success, with our data continuously growing, alongside the capabilities we want to enable for our clients to make better marketing decisions. This talk will dive into the evolution of our data management choices to support the changing needs of the business.

#### Long Description
At AppsFlyer we have been finding ourselves the victims of our own success, with our data continuously growing, alongside the capabilities we want to enable for our clients to make better marketing decisions. These, of course, eventually impact the technology we choose to make this all possible. This talk will dive into the evolution of our data management choices to support the changing needs of the business.

Powering more than 130 thousand mobile apps around the globe, AppsFlyer receives more than 70 billion requests a day, and as a result have a diversity of teams requiring real time performance for different use cases, whether real time attribution, monitoring, big data or web analytics. Each team has built their own technology stack to deliver on its needs. This talk will dive into the many different databases we use in-house – from Aerospike to Druid, Neo4J, Redis, to Clickhouse and even those we chose to eventually phase out. It will dive into the performance considerations for each, and the use cases we leverage each different database for, and why it’s the ideal DB for the job.

This talk will dive into our journey of how to choose the right solution for the job to implement real-time aggregation alongside batch processing over Apache Spark, and additional big data needs with Hadoop. Being able to evolve our architecture enabled us to solve recurring pains as well as aggregate 10X amounts of data with much faster response times, keep up with product demands while delivering a cheaper solution from a production cost perspective.

Speakers: [Yulia Trakhtenberg](#), [Morri Feldman](#), [Nir Rubinstein](#), [Reshef Mann](#), [Adi Belan](#)

</details>
</p>

<details><summary>Managing Your Kafka in an Explosive Growth Environment</summary>

#### Short Description
Kafka, many times is just a piece of the stack that lives in production that often times no one wants to touch - because it just works. At AppsFlyer, Kafka sits at the core of our infrastructure that processes billions of events daily.

#### Long Description
Kafka, many times is just a piece of the stack that lives in production that often times no one wants to touch – because it just works. At AppsFlyer, Kafka sits at the core of our infrastructure that processes billions of events daily.

This talk will share how we built our microservices architecture with Kafka as its core piece to support 70B+ requests daily. With continuous growth we needed to “learn on the job” how to improve our Kafka architecture by moving to the producer owner cluster model, breaking up our massive monolith clusters to smaller more robust clusters, and migrating from an older version of Kafka with real-time production clients & data streams. The talk will outline best practices for leveraging Kafka’s in-memory capabilities & built-in partitioning, as well as some of the tweaks and stabilization mechanisms that enable real-time performance at web-scale, alongside processes for continuous upgrades and deployments with end-to-end automation, in an environment of constant traffic growth.

Speakers: [Alon Gavra](#)
Type: Full-length Presentation

</details>

<p>
  
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

<details><summary>From Theory to Practice: Segmenting Big Data with Probabilistic Data Structures</summary>

#### Short Description

#### Long Description


Speakers: [Adi Belan](#)
Type: Full-length Presentation
</details>
<p>
  
<details><summary>From Theory to Practice: Segmenting Big Data with Probabilistic Data Structures</summary>

#### Short Description

#### Long Description


Speakers: [Adi Belan](#)
Type: Full-length Presentation
</details>
<p>
  
  
<details><summary>From Theory to Practice: Segmenting Big Data with Probabilistic Data Structures</summary>

#### Short Description

#### Long Description


Speakers: [Adi Belan](#)
Type: Full-length Presentation
</details>
<p>
  
  

  
  
  
  
  
<details><summary>Dynamic HBase Coprocessors Using Clojure</summary>

#### Abstract
HBase Coprocessors allow moving nearly arbitrary code execution from the client to the HBase Region Server. For some applications, coprocessors provide a number of major advantages. For instance, moving code from the client can often increase performance by limiting data transfer over the network, especially for aggregation type processing. Also by reducing client data processing, the hardware requirements of the client can lowered. However, programming coprocessors is challenging in several ways. The development cycle for coprocessor development is slow. To try out changes to a coprocessor on a cluster, the coprocessor must be compiled and then the HBase cluster must be restarted to reload the coprocessor. In addition, trying to load a coprocesor with certain defects can crash the HBase cluster.

I will present a generic coprocessor that is able to execute arbitrary Clojure code as a solution to some of the difficulties surrounding coprocessor development. The generic Clojure coprocessor accepts queries that bring their own aggregation instructions in the form of Clojure code. The Clojure code on each query will then be dynamically compiled and executed on the cluster by the generic Clojure coprocessor. Changing specific aggregation code now simply requires rewriting the Clojure code and sending a new query, making for a much faster development cycle than with traditional coprocessor development. To allow the Clojure code to depend on external dependencies -- for instance a JSON parsing library -- the generic Clojure coprocessor also allows for loading "static" dependencies from jar files. In addition to being more dynamic, coprocessor development safety is also increased, because the most dangerous steps, loading and initializing a coprocessor, are only done once rather than each time the aggregation logic is changed. The code for the generic Clojure coprocessor along with full examples will be provided as open source on GitHub.

Speakers: [Morri Feldman](#)

</details>

<p>

<details><summary>Salting Spark for Scale</summary>

#### Abstract
One of the major issues that Spark batch jobs have to contend with at AppsFlyer is that our data is inherently skewed.  For instance a couple of apps account for the vast majority of our traffic.  Data skew wreaks havoc on naively written data jobs by making them perform and scale very poorly as the amount of data they need to process increases.  Recently one of our central data aggregations -- the process that prepares data for the overview dashboard -- stopped working and we had essentially reached the limit where we could no longer devote more Ram to the process to help it.  Using a technique called "Salting" to overcome the data skew that was killing this job we were able to get the job working again and make the entire process much more scalable.  I'll go over Salting in depth to explain how it works and how we are starting to use it here at AppsFlyer.
  
Speakers: [Morri Feldman](#)

</details>

<p>
  
### [Programming Talks](#programming)

#### Clojure
<details><summary>1</summary>
...
</details>

<p>

#### Golang
<details><summary>Go-Sundheit - FTW! Async Health Check Library for Golang</summary>

#### Short Description

We recently open sourced an in-house library Go-Sundheit, to provide support for defining service health for golang services - this enables gophers to register async health checks for dependencies and the service itself - a pretty nifty tool in a dynamic CI/CD environment based on golang.

#### Long Description

At AppsFlyer we face the same issues that many other fast growing companies have to deal with - we have a considerably large operation, where we practice continuous delivery, and we’d like our deployments and runtime to be as safe as possible (mostly, so we can sleep well at night). This normally means that you’d like to know as soon as possible that your deployment has gone bad, or that a resource that your service depends on is now in bad shape.  

Enter Go-Sundheit. We recently started making the migration from Clojure to Go for some of our mission critical services, and in order to be able to have a more holistic view on the performance of our apps we needed to implement some health monitoring capabilities  This talk will present the open source library Go-Sundheit, a library built to provide support for defining service health for golang services. This allows you to register async health checks for your dependencies and the service itself, and provides a health endpoint that exposes their status. This session we will dive into some of the primary use cases where this is useful, and present a short demo for how to get started.


Speaker: [Eran Harel](#)

</details>

<p>



<details><summary>A Journey from Python to Go</summary>

#### Abstract

I love Python. It has been my go-to language for the past five years. But the growth in the popularity and maturity of Go, alongside the strong user base, made me think about how I can add it into my tool set.

In this talk, I'm going to tell you about my journey from Python to Go, and provide you with some tips and expose you to some of the resources that helped me succeed on this journey and live to tell the tale.  I will dive into some of the main differences, and how to minimize the learning curve, as well as some of the excellent libraries and tools that enabled me to ramp up my Go coding skills pretty quickly & painlessly.

Speaker: [Elad Leev](#)

</details>

<p>

#### Frontend
<details><summary>API Gateways - This Time from the Client Side</summary>

#### Abstract

API gateways are a common practice - usually the "public face" of your internal system & are served via one or more backend services.

Besides providing a uniform API, they also facilitate a standard way of authentication, permissions, versioning & much more.
What if we could gain some of those benefits when we build our web applications? 

What if we could compose our app from multiple agnostic parts, each with its different underlying technology & version, thus, enforcing a global authentication flow without rebuilding the whole system?

This talk will show you how we took the core concepts of an API gateway & applied them as the base architecture for our web apps, & scaled to 30+ apps in production while sharing libraries of various versions, managing a global state, routing & more.

Speakers: [Shimi Bar](#), [Liron Cohen](#)
</details>

<p>
  

<details><summary>A Modular SDK in A Fragmented Landscape</summary>

#### Abstract

Web SDKs need to provide a host of capabilities & are a contradiction in terms - on the one hand, they need to be "fully baked" & "closed" in order to provide a uniform API. On the other hand, they need to be flexible in order to support future development & a wide range of clients.

While this can be achieved by "baking" a custom SDK per client - this is not very scalable (nor practically applicable with a business in exponential growth). In order to be able to deliver on the promise of modularity, we wanted to enable users to decide which capabilities they want to enable, without having to define this in advance.  This talk will dive into the development methodology we used in-house to support this, & eventually, how we serve multiple SDKs in a uniform manner to a diversity of clients.

Speakers: [Shimi Bar](#), [Liron Cohen](#)
</details>

<p>
  



### [Culture Talks](#culture)

<details><summary>1</summary>
...
</details>

<p>

### [Cloud & Platform Engineering Talks](#cloud)

<details><summary>Baptism By Fire - Why Production Failures Make you a Better Developer</summary>

#### Short Description
Taking end-to-end ownership of your production code, enables you to understand the operational aspects even the best code encounters - and will contribute to improved coding practices.

#### Long Description
As developers, we are constantly focused on writing elegant and cutting edge code, however, meaningful code eventually lives 99% of its life in production, and becomes “someone else’s problem”. As with all code, issues are bound to arise and someone will have to deal with them (probably at 3 AM after a pagerduty call). At AppsFlyer all developers are expected to own their code end-to-end, to create a greater sense of commitment to its quality, and enable more rapid turnaround on debugging issues. Three years of being on the on-call rotation for mission critical services at AppsFlyer have taught me some hard lessons, but made me a better developer along the way. In this session I’ll dive into best practices for how to approach production issues as developers, some of the lessons I’ve learned about a developer managing production code, and how this ultimately makes us (much) better coders.

Speakers: [Adi Belan](#)
Type: Full-length Presentation

</details>

<p>
  
<details><summary>From Theory to Practice: Segmenting Big Data with Probabilistic Data Structures</summary>

#### Short Description

#### Long Description


Speakers: [Adi Belan](#)
Type: Full-length Presentation
</details>
<p>

<details><summary>Journey to Real Time Analytics in Extreme Growth</summary>
<p>
