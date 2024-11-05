# MySQL

## Linux (Ubuntu)
Update the package index
```bash
sudo apt update
```

Install MySQL
```bash
sudo apt install mysql-server -y
```

Check the status of MySQL
```bash
sudo systemctl status mysql 
# or 
sudo systemctl status mysql.sercive
```

If MySQL is not running, start the service
```bash
sudo systemctl start mysql
```

Access MySQL shell
```bash
sudo mysql
```

Show databases
```bash
show databases;
```

MySQL Secure Installation
```bash
sudo mysql_secure_installation
```

For the local installation, you can use the following settings, but if you are using a remote server in production you should type "yes":
```
Press y|Y for Yes, any other key for No: no

Remove anonymous users? (Press y|Y for Yes, any other key for No) : no

Disallow root login remotely? (Press y|Y for Yes, any other key for No) : no

Remove test database and access to it? (Press y|Y for Yes, any other key for No) : no

Reload privilege tables now? (Press y|Y for Yes, any other key for No) : no
```

Define root password
```bash
sudo mysql
```
```sql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'your_root_password';
```

Testing connection with new root password
```bash
mysql -u root -p
```
or
```bash 
sudo mysql -u root -p'your_root_password' # without space between -p and password
```

## MySQL Workbench
Install MySQL Workbench
```bash
sudo snap install mysql-workbench-community
```

## MySQL on Docker
Pull the MySQL image and create a container and set up the root password and port forwarding
```bash
docker run --name your-container-name-here -e MYSQL_ROOT_PASSWORD=your_root_password -p 3306:3306 -d mysql:8.0.39-debian
```

Stop container
```bash
docker stop your-container-name-here
```

Start container
```bash
docker stop your-container-name-here
```

Access MySQL container
```bash
docker exec -it your-container-name-here /bin/bash
```

Access MySQL shell
```bash
mysql -u root -p'your_root_password'
```
