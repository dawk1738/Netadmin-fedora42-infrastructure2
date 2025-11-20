# [cite_start]Configures the firewall to start on boot [cite: 101]
sudo systemctl enable firewalld

# [cite_start]Permanently allows SSH traffic in the public zone [cite: 101]
sudo firewall-cmd --permanent --zone=public --add-service=ssh

# [cite_start]Makes the changes active without rebooting [cite: 102]
sudo firewall-cmd --reload
