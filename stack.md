# Languages

nep.work's exisitng codebase mainly uses:

- Java 8+
- Scala (in Play modules only)

Custom scripts for specific use cases and house-keeping tasks are written in:

- Python
- Kotlin (only used within Gradle tasks)
- Groovy (will be removed or moved to Gradle/kotlin)

nep.work frontends, which are recent to nep.work use:

- Typescript 3+
- HTML5/CSS3

# Frontend stack

nep.work frontends use:

- Ionic
- Nativescript (IoT and resource intensive applications only)
- Angular/Vue
- RxJS
- SASS

The frontend build process, which is independent of the core nep.work sbt+gradle based build process, generates web, Android, iOS and desktop applications (via Electron) in case of Ionic. At the time of writing, Nativescript generates Android and iOS applications only.

# Mockups and PoC APIs

Proof-of-concept APIs and RAD-prototypes are made using
- Blade
- OpenAPI 3+ (used for code generation in prototypes and for documentation in matured projects)
- Vue/HTML5/CSS3 (Multipage Setup using dev CDNs)
- Blockstack (to skip setting up custom blockchain)
- Adobe XD/Balsamiq (for designing and wireframing)

_______________________________________________________________________________________________________________________

# nep.work core Frameworks

nep.work core's main features, adapted from cosys kernel, is being ported away from it's legacy codebase written entirely in Spring to Play 2+. It uses:

- Play 2+, in-built Akka and sbt support
- Spring Data JPA & Ignite
- Hibernate
- ElasticSearch and Logstash
- Spring Data Redis (read only, only used in specific modules serving mostly static content)

nep.work core's additional features that are being separated from the core into various microservices use:

- Quarkus
- Micronaut
- Apache Camel

# Data & Persistence

nep.work's data handling & persistence is comprised of an in-memory data management layer, a traditional database layer and a pluggable blockchain layer. 

## In-Memory Layer

- Apache Ignite
- Redis

## Databases

- PostgreSQL
- MongoDB (swappable with Mongo-compliant document DBs)
- Druid
- HypergraphDB

## Blockchain

- Multichain (core, fully decentralized with basic multi-centralization support)
- OpenChain/Hyperledger Fabric (optional, adds enterprise support, multi-centered authorities and control policies)
