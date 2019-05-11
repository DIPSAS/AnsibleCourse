# Exercise 06: Installation of DIPS Configuration Server

## DIPS Configuration Server

In this exercise the goal is to install DIPS Configuration Server on the Windows box and configure it to reach the Linux (Zookeeper) box in the same inventory.

1) Create a *role* named `DotnetFramework462` with a task that installs `Dotnet Framework 4.6.2`, a requirement for DIPS Configuration Server. Add the role to `Appserver.yaml`.

    hint: [Package URL](https://chocolatey.org/packages/dotnet4.6.2/4.6.01590.20190226). The package requires a reboot, so have `win_update` handy.

2) Update the role `ConfigurationServer` with `tasks/main.yaml` and write the *task* for installing the chocolatey package for DIPS Configuration Server, using the started variable set in `defaults/main.yaml`.

3) Write a *task* that verifies the health-endpoint for the installed DIPS Configuration Server.

4) Add the *role* `ConfigurationServer` to `Appserver.yaml`