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
## Basic SQL commands
* Create a database
	* `CREATE DATABASE testdb;`
* Use a database
	* `USE testdb;`
* Create a table
```mysql
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100)
);
```
* Insert data
	* `INSERT INTO users (name, email) VALUES ('Hardik', 'hardikarekar@gmail.com');`
* Select data
	* `SELECT * FROM users;`
* Update data
	* `UPDATE users SET name = 'Bittu' WHERE id = 1;`
* Delete data
	* `DELETE FROM users WHERE id = 1;`
* Exit MySQL
	* `EXIT;`
* List all databases
	* `SHOW databases;`
* List all tables in current DB
	* `SHOW tables;`
* See table schema
	* `DESCRIBE users;`
