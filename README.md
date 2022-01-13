# j2e-project

## Installation

### First step
First, clone this repository and get into:
```bash
git clone https://github.com/JulesPierrat/j2e-project.git
cd j2e-project
```
Now you are in: 'REPOSITORYROOT/j2e-project'

### Install Client
First you will need a Php server like Apache2.
Start it:
```bash
sudo service apache2 start
```

Now you have to create a symbolic link beetween the apache2 root (/var/www/html) and our web client (REPOSITORYROOT/client/ProjetJ2E) :
```bash
ln -s REPOSITORYROOT/client/ProjetJ2E /var/www/html
```

Now you can access the client interface at:
http://localhost/ProjetJ2E

### DataBase PostgreSQL
