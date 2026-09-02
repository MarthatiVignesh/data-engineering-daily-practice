DAY 3 - BIG DATA FUNDAMENTALS, HDFS & LINUX
============================================

TOPIC
-----

Big Data Fundamentals, HDFS & Linux

THEORY TOPICS
-------------

1. Introduction to Big Data and why distributed systems
   - Monolithic systems
   - Distributed systems
   - Horizontal scalability
   - Fault tolerance

2. Hadoop Evolution
   - GFS
   - MapReduce
   - Hadoop 1.0
   - Hadoop 2.0
   - YARN
   - Hadoop ecosystem

3. HDFS Architecture
   - NameNode
   - DataNode
   - Blocks
   - Replication factor
   - HDFS read/write concepts

4. Fault Tolerance
   - Heartbeat
   - Single Point of Failure (SPOF)
   - NameNode High Availability
   - Active and Standby NameNodes
   - Quorum Journal Manager (QJM)
   - JournalNodes
   - Quorum


HANDS-ON EXERCISE
-----------------

Whiteboard exercise covering:

- Introduction to Big Data
- Why distributed systems are required
- Monolithic vs distributed systems
- Hadoop evolution
- GFS
- MapReduce
- Hadoop 1.0 vs Hadoop 2.0
- YARN
- Hadoop ecosystem


WORKED EXAMPLE
--------------

A MapReduce-style Word Count example was performed using
Linux commands.

Input:

big data
big data engineering
data engineering
big data

MAP OUTPUT:

big     1
data    1
big     1
data    1
engineering     1
data    1
engineering     1
big     1
data    1

SHUFFLE AND SORT OUTPUT:

big     1
big     1
big     1
data    1
data    1
data    1
data    1
engineering     1
engineering     1

REDUCE OUTPUT:

big     3
data    4
engineering     2


FILES
-----

theory/
- big-data-and-distributed-systems.txt
- hadoop-evolution.txt
- hdfs-architecture.txt
- fault-tolerance.txt

practice/
- whiteboard-exercise.txt
- mapreduce-input.txt
- worked-example.txt

outputs/
- map-output.txt
- shuffle-sort-output.txt
- reduce-output.txt


KEY LEARNING
------------

Big Data requires scalable and distributed systems.

HDFS provides distributed storage.

MapReduce provides a distributed processing model.

YARN separates resource management from processing in
Hadoop 2.0.

HDFS fault tolerance is supported by replication, heartbeats,
and NameNode High Availability.

The practical MapReduce workflow demonstrated:

INPUT
  |
  v
MAP
  |
  v
SHUFFLE AND SORT
  |
  v
REDUCE
  |
  v
FINAL RESULT


DAY 3 STATUS
------------

Theory: Completed
Hands-on: Completed
Worked Example: Completed
Actual Outputs: Saved
