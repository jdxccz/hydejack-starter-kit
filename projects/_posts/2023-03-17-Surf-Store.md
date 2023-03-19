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

This is a distributed cloud-based synchronous database that has been implemented from scratch for the purpose of learning the principles of consistency and distributed storage, and is based on the Raft and Chord papers. The system includes both client and server components, with the server component consisting of two clusters: a meta store cluster and a block store cluster. The client component is responsible for synchronizing local folder changes and cloud folder changes. The meta store cluster, based on the Raft mechanism, reviews conflicts in multi-user file updates and stores file information. The Raft mechanism ensures stability of the service when more than half of the machines are working normally. The block store cluster, based on the Chord mechanism, distributes file data blocks, ensuring load balancing and correct acquisition of required data blocks for files.

## Client


## BlockStore


## MetaStore

## MISC