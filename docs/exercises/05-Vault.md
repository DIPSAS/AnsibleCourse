# Exercise 05: Ansible Vault and encrypted secrets

## Roles with  encrypted variables, variable scoping

1) Create a *role* named `LocalUsers` with with `defaults/main.yaml` and `tasks/main.yaml`.

2) In the `defaults/main.yaml`, create a *dictionary* variable called `users` with usernames and password properties. Use Ansible Vault to encrypt the password.

hint:

```shell
ansible-vault encrypt_string [my-text-string] --ask-vault-pass
```
hint 2: [link](https://stackoverflow.com/a/44241343/3793019)


3) Use `win_user` and `win_user_right` create some users and give them *remote desktop* permissions (use the usernames and passwords from the previous bullet) to create these.

4) Override the `users` variable in `group_vars/windows.yaml` with new usernames and passwords.
