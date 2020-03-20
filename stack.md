## Languages

nep.work's exisitng codebase mainly uses:

- Java 8+
- Scala (in Play modules only)

Custom scripts for specific use cases and house-keeping tasks are written in:

- Python
- Kotlin (only used within Gradle tasks)
- Groovy (will be removed or moved to Gradle/Kotlin)

nep.work frontends, which are recent to nep.work use:

- Typescript 3+
- HTML5/CSS3

## Frontend stack

nep.work frontends use:

- Ionic
- NativeScript (IoT and resource intensive applications only)
- Angular/Vue
- RxJS
- SASS

The frontend build process, which is independent of the core nep.work sbt+gradle based build process, generates web, Android, iOS and desktop applications (via Electron) in case of Ionic. At the time of writing, Nativescript generates Android and iOS applications only.

## Mockups and PoC APIs

Proof-of-concept APIs and RAD-prototypes are made using
- Blade (possibly FastAPI/Flask too in the future)
- OpenAPI 3+ (used for code generation in prototypes and for documentation in matured projects)
- Vue/HTML5/CSS3 (Multipage setup using dev CDNs)
- Blockstack (to skip setting up custom blockchain)
- Adobe XD/Balsamiq (for designing and wireframing)

_______________________________________________________________________________________________________________________

# nep.work core technologies

nep.work core's main features, adapted from cosys kernel, is being ported away from it's legacy codebase written entirely in Spring to Play 2+. It uses:

- Play 2+, in-built Akka and sbt support
- Spring Data JPA & Ignite
- Hibernate
- ElasticSearch and Logstash
- Spring Data Redis (read only, only used in specific modules serving mostly static content)

nep.work core's additional features that are being separated from the core into various microservices use:

- Quarkus (Netty, Vert.x, Kafka)
- Micronaut (Netty, Kafka)
- Apache Camel

## Data & Persistence

nep.work's data handling & persistence is comprised of an in-memory data management layer, a traditional database layer and a pluggable blockchain layer. 

### In-Memory Layer

- Apache Ignite
- Redis

### Databases

- PostgreSQL
- MongoDB (swappable with Mongo-compliant document DBs)
- Druid
- HypergraphDB

### Blockchain

- Multichain (core, fully decentralized with basic multi-centralization support)
- OpenChain/Hyperledger Fabric (optional, adds enterprise support, multi-centered authorities and control policies)

# AI & ML

nep.work currently does not have any support for AI/ML-specific features and APIs. In the future we will most likely be using the relevant (experimental) scripts and algorithms from cosys written using:

- Apache Spark MLib
- Grakn.AI
- Python (SciKit, TensorFlow, Keras)
- Julia (Flux, Spark.jl, SciKitLearn.jl, MLBase.jl, TensorFlow.jl)

______________________________________________________________________________________________________________________

N.B. We use GraalVM for running applications written in JavaScript, Python, Ruby, R, JVM-based languages like Java, Scala, Groovy, Kotlin, Clojure, and LLVM-based languages such as C and C++.
______________________________________________________________________________________________________________________
