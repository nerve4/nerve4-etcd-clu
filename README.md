# nerve4-etcd-clu

An Ansible role that installs etcd base to Ubuntu. More info about bind: [link](https://etcd.io/)


## Requirements

Make sure, you made your vars file with valid path to custom template or you can use Default vars.

You need `ansible 2.13.7` to run this module

The Role also use `community.general collection` module. To install it, use: `ansible-galaxy collection install community.general`. 


## Tasks descriptions

- main.yml - Run the OS check and run the relevant playbook
- set-prerequisites.yml - Set prerequisites on the hosts
- temp-ssl-transition.yml - Setup ssl certs
- install-etcd-clu.yml - Deploy ETCD Services on the hosts


## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
- hosts: servergroup
  become: true
  become_user: lee

  vars_files:
    - vars/main.yml
    
  roles:
    - nerve4-etcd-clu
```


## Maintainer Information
Lee | 2023