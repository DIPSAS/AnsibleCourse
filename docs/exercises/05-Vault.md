# Exercise 05: Ansible Vault and encrypted secrets

## Roles with encrypted variables, variable scoping

1) Create a *role* named `LocalUsers` with with `defaults/main.yaml` and `tasks/main.yaml`.

2) In the `defaults/main.yaml`, create a *dictionary* variable called `users` with usernames and password properties. Use Ansible Vault to encrypt the password.

hint:

```shell
ansible-vault encrypt_string [my-text-string] --ask-vault-pass
```
hint 2: [link](https://stackoverflow.com/a/44241343/3793019)


3) Use `win_user` and  create some users and give them *remote desktop* permissions (use the usernames and passwords from the previous bullet) to create these.

hint: `groups: Remote Desktop Users`, [link](https://docs.ansible.com/ansible/latest/modules/win_user_module.html)

4) Log on to the server with one of the new users.

5) Override the `users` variable in `group_vars/windows.yaml` with new usernames and passwords.
