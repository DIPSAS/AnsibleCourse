# Exercise 06: Installation of DIPS Configuration Server

## DIPS Configuration Server

In this exercise the goal is to provision the Linux server with the `Zookeeper` playbook, and install DIPS Configuration Server on the Windows box.

1) Run the playbook `Zookeeper.yaml` to install Apache Zookeeper component on the Linux server. Zookeeper is used as distributed filesystem for DIPS Configuration Server.

2) Create a *role* named `DotnetFramework462` with a task that installs `Dotnet Framework 4.6.2`, a requirement for DIPS Configuration Server. Add the role to `Appserver.yaml`.

    hint: [Package URL](https://chocolatey.org/packages/dotnet4.6.2/4.6.01590.20190226). The package requires a reboot, so have `win_update` handy.

3) Update the role `ConfigurationServer` with `tasks/main.yaml` and write the *task* for installing the chocolatey package for DIPS Configuration Server, using the started variable set in `defaults/main.yaml`.

4) Write a *task* that verifies the health-endpoint for the installed DIPS Configuration Server.

5) Add the *role* `ConfigurationServer` to `Appserver.yaml`