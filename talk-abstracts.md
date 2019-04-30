## AppsFlyer Engineering has expertise on a diversity of topics, find the 



### [Big Data Talks](#big-data)

<details><summary>From Theory to Practice: Segmenting Big Data with Probabilistic Data Structures</summary>
...
</details>

<details><summary>Journey to Real Time Analytics in Extreme Growth</summary>
<p>

#### Short Description

At AppsFlyer we have been finding ourselves the victims of our own success, with our data continuously growing, alongside the capabilities we want to enable for our clients to make better marketing decisions. This talk will dive into the evolution of our data management choices to support the changing needs of the business.

#### Abstract
At AppsFlyer we have been finding ourselves the victims of our own success, with our data continuously growing, alongside the capabilities we want to enable for our clients to make better marketing decisions. These, of course, eventually impact the technology we choose to make this all possible. This talk will dive into the evolution of our data management choices to support the changing needs of the business.

Powering more than 130 thousand mobile apps around the globe, AppsFlyer receives more than 70 billion requests a day, and as a result have a diversity of teams requiring real time performance for different use cases, whether real time attribution, monitoring, big data or web analytics. Each team has built their own technology stack to deliver on its needs. This talk will dive into the many different databases we use in-house – from Aerospike to Druid, Neo4J, Redis, to Clickhouse and even those we chose to eventually phase out. It will dive into the performance considerations for each, and the use cases we leverage each different database for, and why it’s the ideal DB for the job.

This talk will dive into our journey of how to choose the right solution for the job to implement real-time aggregation alongside batch processing over Apache Spark, and additional big data needs with Hadoop. Being able to evolve our architecture enabled us to solve recurring pains as well as aggregate 10X amounts of data with much faster response times, keep up with product demands while delivering a cheaper solution from a production cost perspective.

Speakers: [Yulia Trakhtenberg](#), [Morri Feldman](#), [Nir Rubinstein](#), [Reshef Mann](#), [Adi Belan](#)

</details>
</p>

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
<details><summary>1</summary>
...
</details>

<p>

#### Frontend
<details><summary>1</summary>
...
</details>

<p>
  




### [Culture Talks](#culture)

<details><summary>1</summary>
...
</details>

<p>

### [Cloud & Platform Engineering Talks](#cloud)

<details><summary>1</summary>
...
</details>

<p>
