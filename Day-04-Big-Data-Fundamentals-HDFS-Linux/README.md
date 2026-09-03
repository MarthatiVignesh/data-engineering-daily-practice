# Day 4 - Big Data Fundamentals, HDFS & Linux

## Topics Covered

### 1. Linux Fundamentals
- Linux file system
- ls
- touch
- mkdir
- rmdir
- cp
- mv
- rm
- Other core Linux commands

### 2. MapReduce
- What is MapReduce?
- Map stage
- Shuffle and Sort
- Reduce stage
- Word Count example
- MapReduce processing flow

### 3. HDFS CLI Hands-on
- Create HDFS files and folders
- Remove HDFS files and folders
- Copy files and folders
- Move files and folders
- Change replication factor
- View file metadata
- Check blocks and replication using fsck

## Linux Practice

Local practice directory:

practice/linux-filesystem/

Files created:
- file1.txt
- file2-renamed.txt

Commands practiced:
- mkdir
- touch
- ls
- cp
- mv
- rm
- rmdir

## MapReduce Practice

MapReduce Word Count was studied using the following flow:

Input
  |
  v
Map
  |
  v
Intermediate Key-Value Pairs
  |
  v
Shuffle and Sort
  |
  v
Reduce
  |
  v
Final Output

Example final word count:

big         2
data        3
engineering 1

## HDFS Practice

HDFS practice directory:

/user/sri/day4-practice

Operations performed:
1. Created HDFS directories.
2. Uploaded a local file to HDFS.
3. Listed HDFS files.
4. Read an HDFS file.
5. Created HDFS folders.
6. Copied files using hdfs dfs -cp.
7. Moved files using hdfs dfs -mv.
8. Removed files using hdfs dfs -rm.
9. Removed empty directories using hdfs dfs -rmdir.
10. Removed non-empty directories using hdfs dfs -rm -r.
11. Changed replication factor using hdfs dfs -setrep.
12. Checked blocks and locations using hdfs fsck.
13. Viewed metadata using hdfs dfs -stat and hdfs dfs -ls.

## Replication Observation

The replication factor was changed from 1 to 2.

Because the local Hadoop setup has only one DataNode, only one live physical replica was available.

Therefore, fsck reported:
- Target replicas: 2
- Live replicas: 1
- Missing blocks: 0
- Corrupt blocks: 0
- Under-replicated blocks: 1

This demonstrates the difference between the configured replication factor and the number of physical replicas that can actually exist with the available DataNodes.

## Output Files

- outputs/linux-filesystem-output.txt
- outputs/replication-fsck-output.txt
- outputs/metadata-output.txt

## Practice Files

- practice/linux-command-practice.txt
- practice/hdfs-cli-practice.txt
- practice/hdfs-test.txt

## Theory Files

- theory/mapreduce-concept.txt

## Key Learnings

- Linux provides commands for managing files and directories.
- MapReduce processes large datasets using Map, Shuffle and Sort, and Reduce stages.
- HDFS stores large files as blocks across DataNodes.
- The NameNode manages HDFS metadata.
- DataNodes store the actual data blocks.
- Replication provides fault tolerance.
- HDFS CLI commands can be used to manage files and directories.
- hdfs fsck can be used to inspect blocks and replication.
