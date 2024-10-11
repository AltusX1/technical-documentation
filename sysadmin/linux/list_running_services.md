**How to find list of running services in linux server ?**

There are several ways to find a list of running services on a Linux server:

Using the `systemctl` command:

This is the most common method for modern Linux distributions using systemd as the init system:

 ``` bash
sudo systemctl list-units --type=service
```

This command will list all active services, including their state (running, inactive, failed, etc.).

Using the `ps` command:

The ps command is a more general tool for listing processes. To see running services, you can filter by the SERVICE column:

 ``` bash
ps aux | grep SERVICE
```

Replace `SERVICE` with the actual name of the service you're looking for.

Using the `service` command:

This command is specific to the SysV init system, which is still used on some older Linux distributions:

 ``` bash
service --status-all
```

This will list all running services and their status.

Using the `chkconfig` command:

This command is also used on older Linux distributions with SysV init:

 ``` bash
chkconfig --list
```

This will list all services and their startup states (on, off, or default).