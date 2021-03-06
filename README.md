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
First, you will need a postgresql server.
Start it:
```bash
sudo service postgresql start
```

Now you can create a new database and a new user for this project:
```bash
sudo -u postgres psql
```

```bash
create database test;
create user test with encrypted password 'test';
grant all privileges on database test to test;
exit;
```
The database is create.
Now we have to connect to postgres with test user (Password is test):
```bash
sudo -u postgres psql -d test -U test -W;
```
Add test information inside using this command:
```bash
\i 'REPOSITORYROOT/database/test.sql'
```

The database is set.

### Run server