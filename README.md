# gitops-hub-and-spoke-template
TODO

## Initialize
This is the process for initializing the gitops loop between Red Hat OpenShift GitOps (ArgoCD) Applications and Red Hat Advanced Cluster Management for Kubernetes (Open Cluster Management) Policies for a target `hub1` cluster.

1. Deploy an unmodified Red Hat OpenShift Container Platform cluster
1. Log into cli of target hub cluster
1. Initialize the reconciliation loop
    ```sh
    ANSIBLE_STDOUT_CALLBACK=yaml ansible-playbook init-playbook.yaml
    ```

## Architecture
TODO

## Status
Current status of this repository

- [x] Initialization is tested as working against Red Hat OpenShift Container Platform cluster 4.16.12
- [ ] Update kuztomizations to point at git links rather then relative links to support structural promotions
- [ ] Document repo description / purpose
- [ ] Document repo architecture
- [ ] Implement sample "managed workload cluster"
