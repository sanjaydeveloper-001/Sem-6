## Hadoop Distributed File System (HDFS)

**Hadoop Distributed File System** is the primary storage system of the **Apache Hadoop** ecosystem. It is designed to store **very large datasets across multiple machines** and provide **high-throughput access** to data. HDFS follows a **distributed architecture** where data is stored across many nodes in a cluster.

HDFS is designed based on the **master–slave architecture**, ensuring **fault tolerance, scalability, and reliability**.

---

# 1. Need for HDFS

Traditional file systems cannot efficiently handle **huge volumes of big data**. HDFS was developed to:

* Store **large files (GBs to TBs)**
* Handle **massive datasets across clusters**
* Provide **fault tolerance using replication**
* Allow **parallel data processing**

---

# 2. HDFS Architecture

HDFS consists of two main types of nodes:

1. **Master Node**
2. **Slave Nodes**

### Main Components

**1. NameNode (Master Node)**
The **NameNode** manages the entire HDFS file system.

Functions:

* Maintains **metadata** of files
* Stores **file directory structure**
* Tracks **block locations**
* Controls access to files

It does **not store actual data**, only metadata.

---

**2. DataNode (Slave Nodes)**
DataNodes are worker nodes that **store actual data blocks**.

Functions:

* Store data blocks
* Perform **read and write operations**
* Send **heartbeat signals** to NameNode
* Send **block reports**

A Hadoop cluster usually contains **multiple DataNodes**.

---

**3. Secondary NameNode**

The **Secondary NameNode** assists the NameNode.

Functions:

* Creates **checkpoints of metadata**
* Merges **Edit Logs with File System Image**
* Helps reduce the load on the NameNode

Note: It **does not replace the NameNode** during failure.

---

# 3. HDFS Storage Mechanism

When a file is stored in HDFS:

1. The file is **split into blocks** (default block size 128 MB).
2. Each block is stored across **multiple DataNodes**.
3. Each block is **replicated** (default replication factor = 3).
4. NameNode records the **location of each block**.

Example:

File → Split into Blocks → Distributed to DataNodes → Replicated

---

# 4. HDFS Architecture Diagram (Neat Diagram)

```
                 Client
                    |
                    v
                +---------+
                | NameNode|
                |(Metadata|
                | Manager)|
                +---------+
                    |
      ---------------------------------------
      |                |                   |
      v                v                   v
  +---------+      +---------+        +---------+
  |DataNode1|      |DataNode2|        |DataNode3|
  | Block A |      | Block B |        | Block C |
  | Block B |      | Block C |        | Block A |
  +---------+      +---------+        +---------+

          (Blocks replicated across nodes)
```

---

# 5. HDFS Read Operation

Steps for reading data:

1. Client requests file from **NameNode**.
2. NameNode returns **DataNode locations**.
3. Client reads data **directly from DataNodes**.
4. Data is transferred in **parallel blocks**.

This improves **speed and efficiency**.

---

# 6. HDFS Write Operation

Steps for writing data:

1. Client sends file request to **NameNode**.
2. NameNode provides **DataNode locations**.
3. File is **split into blocks**.
4. Blocks are stored and **replicated across DataNodes**.

---

# 7. Key Features of HDFS

### 1. Fault Tolerance

* Data replicated across nodes
* System continues even if a node fails

### 2. Scalability

* Nodes can be easily added to the cluster

### 3. High Throughput

* Suitable for **large data processing**

### 4. Data Locality

* Processing happens **near the data location**

### 5. Cost Effectiveness

* Uses **commodity hardware**

---

# 8. Advantages of HDFS

* Stores **massive amounts of data**
* Provides **high reliability**
* Supports **parallel processing**
* Easy **cluster expansion**
* Suitable for **Big Data applications**

---

# 9. Limitations of HDFS

* Not suitable for **small files**
* **Single point failure** if NameNode crashes (in older versions)
* Not ideal for **real-time processing**

---

# Conclusion

The **Hadoop Distributed File System (HDFS)** is a **fault-tolerant and scalable distributed storage system** designed for big data environments. By distributing data across multiple nodes and replicating blocks, HDFS ensures **high reliability, efficient storage, and fast access to large datasets**, making it a core component of the Hadoop ecosystem.

---

✅ If you want, I can also give:

* **A more professional exam diagram (the one teachers expect in university papers)**
* **Important 5–6 points to memorize for HDFS 20-mark answers**
* **Difference between HDFS and traditional file systems** (often asked in exams).
