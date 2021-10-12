# MongoDB


## Install
[Passo-a-passo da instalação.](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/#import-the-public-key-used-by-the-package-management-system)

> Add repository (ubuntu 20.04):

```bash
wget -qO - https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add -

echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list
```

> update and install:

```bash
sudo apt-get update
sudo apt-get install -y mongodb-org
sudo systemctl enable mongod
```

## Import dataset

```bash
mongorestore -d dbname dir/dbname/
```

## Configuração
**Habilitar pretty print**
```
echo DBQuery.prototype._prettyShell = true >> ~/.mongorc.js
```

**Mostrar** mais que 20 registros no find() do shell. Editar arquivo mongorc.js e adicionar:
```
DBQuery.shellBatchSize = 40
```


## mongo-hacker
Melhora da interface cli: https://github.com/TylerBrock/mongo-hacker

Install:
```
git clone https://github.com/TylerBrock/mongo-hacker
cd mongo-hacker
make install
cd ..
rm -rf mongo-hacker/
```
