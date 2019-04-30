# Ansible course material

![](https://cdn.svgporn.com/logos/ansible.svg)

## Prerequisites and installation

To be able to follow this course and do the exercises, Ansible need to be installed.
The Ansible controller machines needs to run on som sort of nix system, preferably Linux or MacOS.

For Windows 10, [installation via Linux Subsystem](https://docs.microsoft.com/en-us/windows/wsl/install-win10) is recommended.

Install Ansible and the required packages (Ubuntu based):

```shell
sudo apt-get update
sudo apt-get install software-properties-common -y
sudo apt-get install python-pip -y
sudo pip install 'pywinrm>=0.1.1'
sudo apt-get install --reinstall ca-certificates -y
sudo apt-add-repository ppa:ansible/ansible -y
sudo apt-get update
sudo apt-get install ansible -y
```

Verify with `ansible --version`.

>By using the official Ansible package repo, new versions of Ansible will be installed when running:
>```shell
>sudo apt-get update
>sudo apt-get upgrade
>```