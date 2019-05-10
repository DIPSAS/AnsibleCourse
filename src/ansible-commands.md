### Windows command
ansible windows_server -i inventory/servers.inventory -m win_ping

### Linux command
ansible zookeepers -i inventory/servers.inventory -m ping