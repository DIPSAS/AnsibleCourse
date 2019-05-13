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

## Clone the project

Make sure [git is installed](https://git-scm.com/download/) and clone the project:

```shell
git clone https://github.com/DIPSAS/AnsibleCourse.git
```

Navigate to the folder `AnsibleCourse/src`, this will be the working directory.

## Editor

It is highly recommended to use an editor with _tree view_ (showing file and folder structure) feature when working with Ansible codebases.

Recommendations are (pick one):

* [VSCode](https://code.visualstudio.com/) with [Ansible](https://marketplace.visualstudio.com/items?itemName=vscoss.vscode-ansible) plugin.
* [Atom](https://atom.io/) with [language-ansible](https://atom.io/packages/language-ansible) and [file-icons](https://atom.io/packages/file-icons) plugins.

## Alternative installation with Vagrant

A prebuilt Virtual Machine can be used with [Vagrant](https://www.vagrantup.com/) and the `Vagrantfile` in the repo.

Clone the project and:

```shell
vagrant up

# Let Vagrant download the VM image and provision it with Ansible
vagrant ssh

cd /vagrant/
```
