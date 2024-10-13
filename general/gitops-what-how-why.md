---
icon: git
cover: >-
  https://images.unsplash.com/photo-1618401479427-c8ef9465fbe1?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwxfHxnaXR8ZW58MHx8fHwxNzI4ODU1NjY3fDA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# GitOps - What/How/Why ?

### What?

* **Evolution of Infrastructure as Code (IaC)**\
  GitOps builds upon the principles of IaC by leveraging Git as the source of truth for infrastructure and application management.
* **Git as the single source of truth**\
  All configurations and infrastructure states are stored in Git repositories, ensuring version control and transparency.
* **Primarily applied to Kubernetes-based infrastructure**\
  GitOps workflows are most common in environments where Kubernetes orchestrates workloads.
* **Introduction of the GitOps operator**\
  A key component introduced with GitOps is the "operator." Its role is to act as an intermediary between the pipeline and the orchestration system. The operator examines the state of the repository, initiates orchestration, and ensures continuous synchronization between the desired and actual states.

***

### Why?

* **Auditing**\
  Track and maintain a log of all modifications to infrastructure.
* **Scalability**\
  Simplify the process of deploying similar infrastructure using the DRY (Don't Repeat Yourself) principle, facilitating easy replication.

***

### How?

Depending on the orchestration system and the level of support you require, different operator solutions are available in the market.\
Here are three major factors to consider when selecting a GitOps operator:

1. **Free or Paid**\
   Evaluate whether an open-source or commercial solution aligns with your needs.
2. **Orchestration System Compatibility**\
   Ensure the tool supports your chosen orchestration platform (e.g., Kubernetes, Terraform).
3. **Popularity**\
   Consider how widely the tool is adopted and the availability of community support or documentation.

Additionally, other features provided by specific tools may also influence your decision, such as SSO, RBAC, and multi-tenancy support.

***

### Examples

| **Argo CD**           | Free & Paid          | Kubernetes                 | 17.7k |
| --------------------- | -------------------- | -------------------------- | ----- |
| **Flux CD**           | Free                 | Kubernetes                 | 8.8k  |
| **Codefresh**         | Paid (Based on Argo) | Kubernetes                 | N/A   |
| **Weave GitOps Core** | Free                 | Kubernetes                 | 540   |
| **Jenkins X**         | Free                 | Kubernetes                 | 4.2k  |
| **Atlantis**          | Free                 | Terraform (non-Kubernetes) | 6.5k  |

***

### My Choice

I chose **Argo CD** because:

* It is a well-known open-source project, meaning I can find extensive resources and community support if needed.
* It supports **Kubernetes** as the orchestration tool, which fits my use case perfectly.

Since I am using Argo CD for **learning purposes** in a home lab environment, I do not need advanced features or a complex setup.









