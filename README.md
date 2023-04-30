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
