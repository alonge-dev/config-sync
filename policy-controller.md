# Policy Controller 
Policy controller enforces cluster compliance using objects called constraints.
It is based on the open policy agent "Gatekeeper". 

## Constraints
* Constraints define what action is allowed or disallowed in your cluster. e.g. require labels on all namespaces, privilege mode escalation, etc

* Policy controller comes with a library of constraints ready for use - to help you maintain best practices for security in your cluster. 
  (If you require more policies, you can create a custom constraint template)

* Constraints can be applied directly to your clusters using the Kubernetes API or distributed on a set of clusters from a source of truth (using config sync)

## Policy Bundles
* Policy bundles allow you audit your clusters without writing any constraints yourself. 
  - requires [an anthos license](https://cloud.google.com/anthos-config-management/docs/concepts/policy-controller-bundles)
* Policy bundles help you meet industry standards, apply best practices etc.
* Policy bundles are applied in a dry run mode by default helping you see issues without blocking your workloads
* Policy bundles are created and maintained by google. you can view details about your coverage per bundle in the policy controller dashboard. 

Example - CIS Benchmark Bundle which covers:
* RBAC and service accounts
* Pod Security Policies
* Network policies and CNI
* Secrets management
* General policies

- [To learn more](https://cloud.google.com/anthos-config-management/docs/how-to/using-cis-k8s-benchmark)