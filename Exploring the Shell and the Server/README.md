## [Finding available options](https://www.mongodb.com/docs/manual/reference/program/mongod/)

```shell
mongod --help
```

## Setting dbpath and logpath

- Create new folders

```shell
cd /var/lib/mongodb
sudo mkdir db
sudo mkdir log
```

- Change the dbpath

```shell
sudo mongod --dbpath /var/lib/mongodb/db
```

- Change the logpath

```shell
sudo mongod --logpath /var/lib/mongodb/log/log.log
```

## Existing Configuration Options

```shell
mongosh
db.serverCmdLineOpts()
```

## [Configuration file](https://www.mongodb.com/docs/manual/reference/configuration-options/)

- Edit the configuration file

```shell
sudo vim /etc/mongod.conf
```

- Use another configuration file

```shell
sudo mongod -f mongod.conf
```

## [Shell Options and Help](https://www.mongodb.com/docs/mongodb-shell/reference/options/)

- Shell Options

```shell
mongosh --help
```

- Help

```shell
mongosh
help
```
