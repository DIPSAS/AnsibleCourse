## Inventory - Windows

1) Add your Windows server to `inventory/servers.inventory` and update `[windows:vars]` with connection details, like username, connection method etc.

2) Use the `win_ping` module to verify that a connection can be made to the server.

hint: `ansible [host_group_name_in_inventory_file] -i inventory/servers.inventory -m win_ping`

## Inventory - Linux

1) add your Linux server to `inventory/servers.inventory` and update `[linux:vars]` with connection details, like username, connection method etc.

2) Generate SSH keypair on the Ansible controller machine.

3) Transfer the SSH public-key to the Linux machine.

4) Use the `ping` module to verify that a connection can be made to the server.

hint: `ansible [host_group_name_in_inventory_file] -i inventory/servers.inventory -m ping`