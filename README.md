### PS1
    PS1='\033[1;32m\u@\h\033[1;37m:\033[1;34m\w\033[1;37m$ '

### Logout users
    pkill -KILL -u {username}
  
### MySQL login fix
    UPDATE mysql.user SET plugin = 'mysql_native_password' WHERE user = 'root' AND plugin = 'unix_socket';

### Static IP
Go to **/etc/netplan/**
For example you might find there a default netplan configuration file called **01-netcfg.yaml** or **50-cloud-init.yaml** with a following content instructing the networkd deamon to configure your network interface via DHCP:

    network:
        ethernets:
            eth0:
                dhcp4: false
                addresses: [192.168.1.24/24]
                gateway4: 192.168.1.1
                nameservers:
                    addresses: [8.8.8.8,8.8.4.4]
                optional: true
        version: 2

**sudo netplan apply**

### quit screen
    screen -XS <name/id> quit
    
### Find folder name
    sudo find / -type d -name "<folder name>"
