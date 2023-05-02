---
marp: true
theme: default
title: Config sync 
description: An introduction to config sync and the gitops workflow
author: George Alonge
keywords: configsync, gke, gitops
---
# Config Sync 

![bg contain right:50%](https://files.codingninjas.in/article_images/anthos-config-management-3-1659783610.jpg)

Today we cover:

* Setup Open Source Config Sync

---

# Introduction
* Spin up a cluster: in this demo, i'm using a k3d cluster but any cluster should do
  ` k3d cluster create demo-cluster --servers 3`
  This creates a cluster with 3 nodes.

* Get the latest version of config sync from [here](https://github.com/GoogleContainerTools/kpt-config-sync/releases) 

* `export CS_VERSION=<Replace-with-version-from-config-sync-releases-page>`

* Download latest manifest file: [config-sync.yml]("https://github.com/GoogleContainerTools/kpt-config-sync/releases/download/${CS_VERSION}/config-sync-manifest.yaml") with `wget "https://github.com/GoogleContainerTools/kpt-config-sync/releases/download/${CS_VERSION}/config-sync-manifest.yaml"`

* Install on cluster:  `kubectl apply -f config-sync-manifest.yaml`
* Install root-sync for each repo: `kubectl apply -f root-sync.yaml`