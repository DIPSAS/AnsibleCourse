# Exercise 04: Templates, handlers and files

## Roles with  templates and handlers

1) Add the `Stratos` *role* to the playbook. Update the *role* with a *task* for copying `log4net.config` to the install-location of Stratos (variable `stratosInstallfolder`).

hint: [win_template](https://docs.ansible.com/ansible/latest/modules/win_template_module.html)

2) In the `defaults/main.yaml`, create a variable `logLevel` with the value `info` and introduce this variable in `templates/log4net.config` => `<level value="Debug" />` (replace `Debug` with this variable).

3) Create a *handler* that restarts the `Stratos` service if:
    
* A new version of Stratos is installed
* The `log4net.config` file changes.

hint: [win_service](https://docs.ansible.com/ansible/latest/modules/win_service_module.html)

4) Run the playbook, observe the handler restarting the service and verify it from `http://server-name:1337/api/chocoPackages`.

5) Bonus exercise: Use `win_uri` to verify HTTP 200 from the service after installation.
