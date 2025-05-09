#infraservices
## Installation on Ubuntu Jammy
  1. `curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -`
  2. `curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor | sudo tee /etc/apt/keyrings/microsoft.gpg > /dev/null`
  3. `snap install curl`
  4. `curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor | sudo tee /etc/apt/keyrings/microsoft.gpg > /dev/null`
  5. `sudo add-apt-repository "$(curl https://packages.microsoft.com/config/ubuntu/22.04/mssql-server-2019.list)"`
  6. `sudo apt update`
  7. `sudo apt install -y mssql-server`
  8. `sudo systemctl status mysql`
  9. `sudo mysql_secure_installation`
  10. `sudo systemctl status mysql`
  11. `sudo systemctl start mysql`
  12. `sudo systemctl enable mysql`
  13. `sudo mysql -u root -p`