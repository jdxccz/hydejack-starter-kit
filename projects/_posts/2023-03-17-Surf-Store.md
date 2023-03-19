---
layout: post
title: Surf Store
description: >
  This is a cloud-based multi-user synchronous storage system, which is divided into meta stores for storing versions and hashes and block stores for storing data. It built the Raft mechanism to ensure fault-tolerant meta store and the Chord mechanism to ensure scalable and distributed block store.
image:
  path: /assets/img/projects/surfstore.png
sitemap: false
hide_last_modified: true
---

Language: **Go**

## General

This is a distributed cloud-based synchronous database that has been implemented from scratch for the purpose of learning the principles of consistency and distributed storage, and is based on the Raft and Chord papers. The system includes both client and server components, with the server component consisting of two clusters: a meta store cluster and a block store cluster. 

The client component is responsible for synchronizing local folder changes and cloud folder changes. The meta store cluster, based on the Raft mechanism, reviews conflicts in multi-user file updates and stores file information. The Raft mechanism ensures stability of the service when more than half of the machines are working normally. The block store cluster, based on the Chord mechanism, distributes file data blocks, ensuring load balancing and correct acquisition of required data blocks for files.

## Client

The client component first reads the files and index of the specified folder, and creates an index if one does not exist. It then updates the local index based on the index and files. Next, it connects to the remote meta store cluster leader node and attempts to submit the modified file directory. It also merges cloud changes made by others and determines whether the file update is valid. After that, it connects to the remote block store cluster, finds the corresponding block store, and retrieves or submits data blocks as necessary. Finally, the new index is written back to the folder.

## BlockStore

The block store initially employs a DHT-based addressing mechanism to efficiently locate the storage node that corresponds to the hash of the data block within the cluster, achieving this in O(logn) time complexity. The block store also provides functionality for both submitting and retrieving data.

## MetaStore

The meta store provides a default address for the block store. Additionally, it offers a method to retrieve the cloud index for comparing differences between the local and cloud files. When updating cloud files, one must first submit the update to the cloud index at the meta store to ensure its validity. For example, updates need to be based on the latest cloud version, similar to the submission restrictions on GitHub. Finally, the meta store implements the Raft consensus algorithm, which ensures consistency and fault tolerance across different meta store nodes through leader election and heartbeat messages.

## GRPC

In addition, the communication between cluster nodes, as well as between clusters and clients, is implemented using the gRPC service. This ensures cross-platform compatibility among different operating systems. Furthermore, gRPC provides high-performance and efficient communication due to its use of protocol buffers and HTTP/2. The use of gRPC also simplifies the implementation of the communication layer and enables easy integration with other tools and frameworks.

## MISC

The initialization program includes the reading and parsing of parameters, as well as the launching of nodes or clusters. The monitoring program tracks the real-time status of the metastore cluster. These programs are essential components of the distributed cloud synchronization database system and are crucial for ensuring the system's stability and reliability.

## Source Code

If you want to know more details, you can check source code <a href="https://github.com/jdxccz/SurfStore">@here</a>.