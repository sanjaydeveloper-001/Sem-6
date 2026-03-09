Below are **two 20-mark answers** based on the content from your uploaded PDF. I structured them like an **exam answer (introduction + explanation + diagram + points)** so you can write directly in the exam.

---

# 1. Explain the Architecture of Hadoop Ecosystem (20 Marks)

## Introduction

Apache Hadoop is an **open-source framework** used for storing and processing large volumes of data in a distributed computing environment. It allows large datasets to be processed across **clusters of commodity hardware** using parallel processing. The Hadoop ecosystem consists of several tools and technologies that work together to **store, manage, and analyze big data efficiently**. 

The core components of the Hadoop ecosystem are:

* HDFS (Hadoop Distributed File System)
* YARN (Yet Another Resource Negotiator)
* MapReduce
* Hadoop Common

These components are supported by several other tools like Hive, Pig, HBase, Spark, Mahout, ZooKeeper, and Oozie. 

---

## Architecture of Hadoop Ecosystem

```
                +------------------+
                |    Applications  |
                | (Analytics, ML)  |
                +---------+--------+
                          |
        +-----------------+-----------------+
        |                                   |
   +----+----+                         +----+----+
   |  Hive   |                         |   Pig   |
   +----+----+                         +----+----+
        |                                   |
        +-----------+--------------+--------+
                    |              |
                +---+--------------+---+
                |     MapReduce        |
                +---+--------------+---+
                    |              |
                +---+--------------+---+
                |        YARN          |
                +---+--------------+---+
                    |              |
              +-----+--------------+-----+
              |        HDFS (Storage)    |
              +--------------------------+
```

---

## Components of Hadoop Ecosystem

### 1. Hadoop Distributed File System (HDFS)

* HDFS is the **storage layer** of Hadoop.
* It stores huge datasets across multiple machines in a cluster.
* Files are divided into **blocks** and distributed across **DataNodes**.
* It provides **fault tolerance through data replication**. 

Functions:

* Distributed storage
* Fault tolerance
* High throughput access

---

### 2. YARN (Yet Another Resource Negotiator)

YARN manages **resources in the Hadoop cluster**.

Main Components:

* **Resource Manager** – allocates cluster resources.
* **Node Manager** – manages resources on individual nodes.
* **Application Manager** – coordinates execution of applications. 

Functions:

* Resource allocation
* Job scheduling
* Cluster management

---

### 3. MapReduce

MapReduce is the **data processing framework** in Hadoop.

It processes data using two functions:

**Map Function**

* Filters and sorts data
* Produces key-value pairs

**Reduce Function**

* Aggregates and summarizes the mapped data. 

Advantages:

* Parallel processing
* Fault tolerance
* Scalability

---

### 4. Hadoop Common

Hadoop Common contains **libraries and utilities** required by other Hadoop modules.

Functions:

* Java libraries
* Configuration files
* Support services for Hadoop components.

---

## Supporting Tools in Hadoop Ecosystem

### Hive

* Data warehouse infrastructure.
* Uses **Hive Query Language (HQL)** similar to SQL. 

### Pig

* High-level scripting platform for analyzing large datasets.
* Uses **Pig Latin language**.

### HBase

* NoSQL database that runs on top of HDFS.
* Used for **real-time data access**.

### Spark

* Fast in-memory data processing engine.
* Used for real-time analytics and machine learning.

### Mahout

* Machine learning library for Hadoop.

### ZooKeeper

* Manages coordination and synchronization in Hadoop clusters.

### Oozie

* Job scheduling system for Hadoop workflows. 

---

## Advantages of Hadoop Ecosystem

* Scalable storage and processing
* Fault tolerance
* Cost-effective (uses commodity hardware)
* Parallel processing
* Handles structured and unstructured data

---

## Conclusion

The Hadoop ecosystem provides a **complete platform for big data storage, processing, and analysis**. Its components such as HDFS, YARN, and MapReduce work together with various tools like Hive, Pig, and Spark to efficiently handle large datasets in distributed environments.

---
