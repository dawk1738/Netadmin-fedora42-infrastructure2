# [cite_start]Installs the DHCP server daemon [cite: 104]
sudo dnf install dhcp-server

# [cite_start]Configures the DHCP service to start at boot [cite: 105]
sudo systemctl enable dhcpd

# [cite_start]Opens the configuration file for editing [cite: 103]
sudo nano /etc/dhcp/dhcpd.conf
