# MongoDB Connector

Setup of mongodb database:

Follow the installation instructions from [mongodb](https://docs.mongodb.com/manual/administration/install-community/).

Start the mongodb by executing `sudo service mongod start`

Then, enter the mongodb shell by typing `mongo` in your command line.

Create a database for the project:

```console
use p2b2
```

Create a collection for the blocks to be saved in:

```console
db.createCollection("blocks")
```

**Note**: You won't be able to see the new p2b2 database before creating the collection, because the database is completely empty.

Now that you created the collection, you should be able to see the database using `show dbs` and the collection using `show collections`.

Create an index for the block number:
```console
db.records.createIndex({number:-1})
```