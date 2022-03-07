# Ansible Assisted Installer Playbooks

This Playbook is for setting cluster into Day2 and setting UP PXE services and files.
giving `Assisted installer` URL and cluster 

> note: After transfomation the UI will no longer shows the current cluster

### **Requirements**
---
-  Ansible >= 2.9



### **How to Use**
---
clone the repo and install the needed requirements
if need you can set different branch in the `requirements.yaml`

```shell
ansible-galaxy install -f requirements.yaml
```

set the variable in the `playbook.yaml`
```yaml
    ARCH: arm
    URL: http://<URL>:<PORT>
    CLUSTER_ID: "< CLUSTER UUID >" 
```

next run the installation
```shell
ansible-playbook -i <host>, playbook.yaml 
```

you can check add optional configurations which listed in the role Documentation 

- [setup-pxe doc](https://github.com/eifrach/ansible-role-setup-pxe/blob/main/README.md)
- [iso-to-pxe](https://github.com/eifrach/ansible-role-download-iso-pxe/blob/main/README.md)


