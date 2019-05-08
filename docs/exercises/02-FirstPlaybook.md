# Exercise 02: Playbook and simple tasks

## My first Playbook

1) Create a file called `Appserver.yaml`.

2) Add a *task* for running Windows Update with the `win_update` module, targeting the `windows` hostgroup. Note: we only want _security updates_ installed.

hint: [win_update module](https://docs.ansible.com/ansible/latest/modules/win_updates_module.html)

3) Add a new *task* to the playbook for rebooting the server with the `win_reboot` module _only if the installed windows update required it_.

4) Run the playbook against the inventory file.

hint:

```shell
ansible-playbook -i [path/to/file.inventory] Appserver.yaml --verbose
```