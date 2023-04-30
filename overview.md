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

* What is Config Sync and Why? 
* How it Works
* How to Setup on both GKE and non-GKE clusters

---

# Introduction
* Maintaining a consistent set of configurations and policies across environments can become a challenge especially as companies grow in size. 
* The need for a way to manage these consistency across clusters/environments becomes apparent.
![bg contain right:30%](https://files.codingninjas.in/article_images/anthos-config-management-3-1659783610.jpg)

---
# What is Config Sync? 
Config sync is an "open source" tool by google that allows you:
* Manage and sync configurations/policies to your Kubernetes clusters.
* Source: Any git repository (github, bitbucket, sourcerepos), OCI images and helm charts
* Single or multiple clusters
* Based on gitops principles
* YAML or JSON configs

---
# Architecture Overview


![bg 50%](https://cloud.google.com/static/anthos-config-management/docs/img/acm-overview.svg)

---
## Offerings: 
* OSS Config Sync (open source)
* GKE/Anthos Config SYNC (managed)


---

# How It Works
Some components of config sync:
* `Root Sync`: Custom Resource objects that manage cluster wide resources.
* `Repo Sync`: Custom Resource objects that manage namespaced resources
* `Resource Groups`: Validates configs and tracks resources managed by config sync.
* `Reconciler`: Manages root sync and repo sync objects by watching for changes and reconciling.

---

# How to Setup Config Sync
If you are using a GKE cluster, then you can simply opt in for google's managed config sync. 

### GKE Clusters
* Enable it on the UI
* Enable it using Terraform

### Non GKE Clusters
* Install Manually

---

## Demo
- UI
- Using Terraform 
- Manual