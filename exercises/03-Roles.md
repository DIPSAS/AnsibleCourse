## Roles, variables and iterators

1) Create a *role* for the windows update tasks from exercise 2 and change the playbook to use this role.

2) Create a new role called `IIS`. This role will install IIS features with the `win_feature` module.

3) Create a `defaults/main.yaml` file and add a _variable_ called IISFeatures containing the following features:

* `Web-Server`
* `Web-Common-Http`
* `Web-App-Dev`
* `Web-Net-Ext45`
* `Web-Asp-Net45`

hint: `yaml` lists are on the following format: 

```yaml

list:
    - item 1
    - item 2
```

4) Use `with_items:` to make `win_feature` install the list of IIS features.

5) Add the `IIS` role to the playbook and run.