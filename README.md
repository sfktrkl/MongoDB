## MongoDB

### Installation [Linux](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/)

- Import the public key used by the package management system

```shell
sudo apt-get install gnupg
curl -fsSL https://pgp.mongodb.com/server-6.0.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-6.0.gpg \
   --dearmor
```

- Create a list file for MongoDB

```shell
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-6.0.gpg ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list
```

- Reload local package database

```shell
sudo apt-get update
```

- Install the MongoDB packages

```shell
sudo apt-get install -y mongodb-org
```

### Running

- Start MongoDB

```shell
sudo systemctl start mongod
```

- Verify that MongoDB has started successfully

```shell
sudo systemctl status mongod
```

- Stop MongoDB

```shell
sudo systemctl stop mongod
```

- Restart MongoDB

```shell
sudo systemctl restart mongod
```

- Begin using MongoDB

```shell
mongosh
```

### Time to Get Started

- To see existing databases

```shell
show dbs
```

- Create and connect to a new database

```shell
use shop
```

- Create a collection on the fly and insert

```shell
db.products.insertOne({ "name": "A Book", "price": 12.99 })
db.products.insertOne({ "name": "A T-Shirt", "price": 22.99, "description": "High quality T-Shirt" })
db.products.insertOne({ "name": "A Computer", "price": 1122.99, "description": "High quality Computer", "details": { "cpu": "Intel", "memory": 32 } })
```

- Look at the data

```shell
db.products.find().pretty()
```

### Install python

```bash
sudo apt-get install python3
sudo apt-get install python3-pip        # Install pip
sudo apt-get install python3-autopep8   # Install autopep8
```

### Install Jupyter Notebook

- Install

```shell
pip install jupyterlab
pip install notebook
```

- Run the jupyter notebook

```shell
jupyter notebook
```

### Install pymongo

```shell
pip install pymongo
```
