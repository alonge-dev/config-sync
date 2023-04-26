# Config Sync 

Today we cover:

* What is Config Sync? 
* How it Works
* How to Setup on both GKE and non-GKE clusters


# What is config sync? 
Config Sync is an open source tool from Google that enables you to manage and sync the configuration of your Kubernetes clusters from a Git repository. 

- Works for single clusters, multi-tenant clusters and multi-cluster deployments
- Based on gitops principles
- YAML or JSON configs

## Offerings: 
- OSS Config Sync (open source)
- GKE/Anthos Config SYNC (managed)


# How It Works
The main components of config sync:
1. `Config Sync Operator`: Watches git and applies changes to cluster.
2. `Config Management`: Manages config sync components e.g. repo url, branch, auth settings etc.
3. `Config Validator`: Validates configs before applying them to cluster (optional)


# How to Setup Config Sync
If you are using a GKE cluster, then you can simply opt in for google's managed config sync. 

### GKE Clusters
- Enable it on the UI
- Enable it using Terraform

### Non GKE Clusters
- Install Manually

## Demo
- UI
- Using Terraform 
- Manual