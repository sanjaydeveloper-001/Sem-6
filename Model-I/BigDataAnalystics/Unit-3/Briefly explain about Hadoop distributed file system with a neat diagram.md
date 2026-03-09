
# 2. Briefly Explain Hadoop Distributed File System (HDFS) with Neat Diagram (20 Marks)

## Introduction

Hadoop Distributed File System (HDFS) is the **primary storage component of Hadoop** designed to store large datasets across multiple machines. It is a **distributed and fault-tolerant file system** that runs on commodity hardware. HDFS stores data in blocks and distributes them across cluster nodes. 

---

## HDFS Architecture

HDFS follows a **Master–Slave architecture**.

Main components:

1. NameNode
2. DataNode
3. Secondary NameNode
4. HDFS Client
5. Block Storage

---

## Neat Diagram of HDFS Architecture

```
                    +-------------------+
                    |      Client       |
                    +---------+---------+
                              |
                              v
                     +--------+--------+
                     |      NameNode   |
                     |  (Master Node)  |
                     +--------+--------+
                              |
          ---------------------------------------------
          |                     |                      |
          v                     v                      v
    +-----------+        +-----------+          +-----------+
    | DataNode  |        | DataNode  |          | DataNode  |
    | (Block1)  |        | (Block2)  |          | (Block3)  |
    +-----------+        +-----------+          +-----------+
          |                     |                      |
      Replication           Replication            Replication
```

---

## Components of HDFS

### 1. NameNode (Master Node)

* Central server of HDFS.
* Maintains **metadata** such as:

  * File names
  * File permissions
  * Block locations
* Manages file system operations like:

  * Opening files
  * Closing files
  * Renaming files. 

---

### 2. DataNode (Worker Node)

* Stores the **actual data blocks**.
* Executes instructions given by NameNode.
* Performs:

  * Block creation
  * Block deletion
  * Block replication. 

---

### 3. Secondary NameNode

* Acts as a **helper for the NameNode**.
* Creates **checkpoints of metadata**.
* Merges EditLog and FsImage to prevent NameNode overload.

---

### 4. HDFS Client

* Interface between user applications and HDFS.
* Communicates with:

  * NameNode for metadata
  * DataNodes for reading/writing data.

---

### 5. Block Structure

* Files are divided into **blocks (default 128 MB)**.
* Blocks are stored across different DataNodes.
* Each block has **multiple replicas** (default replication factor = 3). 

---

## Working of HDFS

### File Storage Process

1. File is divided into blocks.
2. Blocks are stored across DataNodes.
3. Each block is replicated to ensure reliability.
4. NameNode maintains the metadata.

---

### Read Operation

1. Client requests file from NameNode.
2. NameNode provides block locations.
3. Client directly reads blocks from DataNodes.

---

### Write Operation

1. Client requests NameNode to write file.
2. NameNode allocates DataNodes.
3. Data is written to DataNodes and replicated.

---

## Features of HDFS

* Distributed storage
* Fault tolerance
* High scalability
* High throughput
* Data replication

---

## Advantages

* Reliable storage of large data
* Cost-effective infrastructure
* Parallel data processing
* High availability of data

---

## Limitations

* Not suitable for small files
* High latency access
* NameNode failure can affect the system

---

## Conclusion

HDFS is a **reliable and scalable distributed file system** designed for big data applications. Its master-slave architecture with NameNode and DataNodes ensures efficient storage, high availability, and fault tolerance for massive datasets.

---

✅ If you want, I can also give:

* **Shorter exam-friendly version (exactly 2–3 pages writing format)**
* **Better hand-draw diagram style you can copy in exam** (teachers like that).
