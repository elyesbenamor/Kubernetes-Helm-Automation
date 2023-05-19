# # k8s-helm-automation

This is a project where you can blindly configure linux Vms to be part of a **kubernetes** cluster that has most of the configuration. 
Only run the playbooks explained below and you are done 

## Requirements
- 🦎 Minimum two Vms (ubuntu/debian) based.
-  🛜 Decent internet connection 

## One way to go
`setup-cluster.yml` is used to to handle al the requirements an being installed in order to have a proper cluster.

## Roles definitions
- `system-setup` : used to install 🐧 requirements.
-  `docker` : install docker 🐋
- `k8s-setup`: install ☸️ api resources and initialize the cluster
-  `helm` : install helm package


## Control Options

You can control packages version or networking setup. 
|Variable                          |Value                         |
|-------------------------------|-----------------------------|
|`kubernetes_version`            |'1.17'            |
|`kubernetes_pod_network`            |By default `flannel` is enabled    |
|`kubernetes_apt_release_channel`|`main` channel always|


## Usage
- invoke `ansible-playbook -i inventory system-setup` and get a coffee ˗ˏˋ☕ˎˊ˗
-  invoke `ansible-playbook -i inventory clean-k8s.yml` is to clean the setup in all kubernetes nodes.
