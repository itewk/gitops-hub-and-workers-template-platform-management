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

## Accessability
Information about accessability.

### Colors
An attempt has been made where color is used in console customizations to be color blind safe based on [Paul Tol's Notes: Colour schemes and templates: Sequential Colour Schemes: Figure 18a](https://personal.sron.nl/~pault/#sec:sequential).

* management: #A80003 / #FFFFFF
* production: #F6790B / #000000
* test: #E7B503 / #000000
* development: #BBE453 / #000000
* sandbox: #C6F7D6 / #000000
* info: #888888 / #000000

## Testing
Kustomize build test
```sh
ANSIBLE_STDOUT_CALLBACK=yaml ansible-playbook tests/test-all-kustomization-builds-playbook.yaml
```

## Status
Current status of this repository

- [x] Initialization is tested as working against Red Hat OpenShift Container Platform cluster 4.16.12
- [x] Gitops-ify adding managed clusters to RHACM
- [x] Implement sample "managed workload cluster"
- [ ] Update kuztomizations to point at git links rather then relative links to support structural promotions
- [ ] Document repo description / purpose
- [ ] Document repo architecture
