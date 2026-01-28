## ArgoCD
Argo CD is referred to as a "GitOps CD" tool because it uses Git repositories as the single source of truth to define the desired application state and automates the process of matching that state to a live Kubernetes cluster.   
It is specifically designed to implement the GitOps methodology for Continuous Delivery (CD). 

Here is why it fits the definition:
- Git as Single Source of Truth: Argo CD tracks changes to applications defined in Git (YAML, Helm, Kustomize).
- Pull-Based Model: Instead of a CI system pushing changes, Argo CD runs inside Kubernetes, actively pulling configuration from Git to deploy applications, which enhances security.
- Drift Detection and Self-Healing: It constantly compares the live state in the cluster with the desired state in Git. If someone makes manual changes to the cluster (drift), Argo CD can automatically fix it to match the Git repository.
- Declarative Approach: It enforces a GitOps workflow where infrastructure and applications are defined declaratively, providing auditability and easy rollbacks. 
- Argo CD bridges the gap between Git and Kubernetes, making it a foundational tool for implementing GitOps. 
