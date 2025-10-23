Command,Description
sudo dnf install @base-x,Installs the core X server packages and dependencies.
sudo dnf install @xfce-desktop,Installs the full Xfce desktop environment group.
sudo systemctl enable xdm.service,Enables the XDM login manager to start at boot.
sudo systemctl set-default graphical.target,Switches the default boot mode from text (multi-user) to GUI (graphical).
sudo reboot,Applies the changes and starts the server into the new graphical login screen (XDM).
sudo systemctl isolate graphical.target,Temporarily switches to GUI mode.


Command,Description
sudo dnf update,Ensures latest software updates and security patches.
sudo passwd root,Set a strong password for the most powerful user.
sudo useradd -m username,Create a new user for daily tasks.
sudo passwd username,Set a password for the new user.
sudo dnf install httpd,Example command to install additional software packages.

Command,Description
nmcli connection show or ip addr show,Commands to view current network interfaces.
sudo nano /etc/sysconfig/network-scripts/ifcfg-eth0,Use text editor to set parameters like IP address.
sudo systemctl restart NetworkManager,Restarts the service to apply changes.
sudo systemctl enable firewalld,Configures the firewall to start on boot.
sudo firewall-cmd --permanent --zone=public --add-service=ssh,Permanently allows SSH traffic.
sudo firewall-cmd --reload,Makes the changes active.


Command,Description
sudo dnf install nano,Installs the easy-to-use editor.
sudo dnf install dhcp-server,Installs the DHCP server daemon.
sudo nano /etc/dhcp/dhcpd.conf,Opens the configuration file for DHCP.
sudo systemctl enable dhcpd,Configures service to start at boot.

Command,Description
sudo dnf install nfs-utils,Installs NFS server utilities.
sudo mkdir /shared,Creates the shared directory.
sudo nano /etc/exports,Opens exports file to configure NFS shares.
sudo systemctl start nfs-server.service,Starts NFS server.
sudo systemctl enable nfs-server.service,Enables NFS at boot.
sudo chmod -R 755 /shared,Sets proper permissions on the shared directory.
sudo systemctl restart nfs-server,Restarts NFS server to apply changes.

Command,Description
sudo firewall-cmd --permanent --zone=public --add-service=nfs,Opens NFS service ports.
sudo firewall-cmd --permanent --zone=public --add-service=mountd,Allows mountd through firewall.
sudo firewall-cmd --permanent --zone=public --add-service=rpc-bind,Allows rpcbind service through firewall.
sudo firewall-cmd --reload,Reloads firewall settings.

III. Samba Configuration (File and Printer Sharing)
sudo dnf install cups,Installs printing service (CUPS).
sudo systemctl start cups,Starts CUPS service.
sudo systemctl enable cups,Enables CUPS at boot.
sudo useradd dawkins,Create a Samba system user.
sudo smbpasswd -a dawkins,Add user to Samba database and set password.
sudo mkdir -p /srv/samba/share,Create the samba share directory.
sudo cp /etc/samba/smb.conf /etc/samba/smb.conf.bak,Backup the original configuration file.
sudo nano /etc/samba/smb.conf,Open to configure the main file.
sudo systemctl start smb,Starts the Samba service.
sudo systemctl enable smb,Enables Samba to start on boot.
sudo systemctl restart smb.service,Restarts Samba service to apply cha
