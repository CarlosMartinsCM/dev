# MySQL

## Install

Ubuntu:

```bash
sudo apt install mysql-server
# don't accept password policy
sudo mysql_secure_installation
```

Configurar senha root:
```bash
sudo mysql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '123456';
FLUSH PRIVILEGES;
```

## Importar arquivo

Verificar antes se o banco `dbname` existe. 

```bash
mysql -u root -p dbname < dataset.sql
```

## Alterar senha

Exemplo alterar senha root:

```bash
sudo mysql -u root -p
ALTER USER 'root'@'localhost' IDENTIFIED WITH caching_sha2_password by '123456';
exit
```

Por exemplo, se a senha é abc e deseja alterar para 123456:

```bash
mysqladmin -u root -p'abc' password '123456'
```


## Exportar database para arquivo

```bash
mysql -u username -p dbname > dumpfile.sql
```

```bash
mysqldump -u root -p dbname > dumpfile.sql
```


## Comandos

### Create database
```sql
CREATE DATABASE mydb DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;
```

### Truncate

```sql
SET FOREIGN_KEY_CHECKS = 0;
truncate tableName;
SET FOREIGN_KEY_CHECKS = 1;
```

## Ferramentas

### Workbench

Download: [mysql-apt-config_0.8.19-1_all.deb](https://dev.mysql.com/downloads/repo/apt/) (ou última versão)

```bash
sudo apt install ./mysql-apt-config_0.8.19-1_all.deb
```
Selecionar "Ok"

```bash
sudo apt update
```

```bash
sudo apt install mysql-workbench-community -y
```

```bash
mysql-workbench
```