---
published: true
title: A Short Introduction to Cassandra
layout: default
---

Cassandra is a database. It's a database of NoSQL family. It is developed at facebook and is now open-source.

These are the features that made Cassandra popular these days.

1. Cassandra is linearly scalable. That means you add a machine and it automatically increase performance with no further configuration.
2. Cassandra's write speeds are un-parellelled. Because writes are pushed into append-only log.
3. Cassandra's reads are distributed and fast (and reads won't get outdated data to client)

Cassandra has good support for analytics with Scala on top of Spark. So it became a hot cake in industry for large scale data which used to be stored in proprietary systems and used to be processed by ETL systems. Now you can have Cassandra and Spark cluster with Scala for real time analytics. It was very hard in the past even with Hadoop.

How does Cassandra work?

Cassandra nodes( machines with Cassandra installed)
