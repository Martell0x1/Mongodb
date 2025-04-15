<p align="center">
  <img src="https://img.shields.io/badge/MongoDB-Studying%20Repo-brightgreen?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB Study Badge" />
</p>

<h1 align="center">
  📚 MongoDB Journey
</h1>

<p align="center">
  <img src="https://www.vectorlogo.zone/logos/mongodb/mongodb-ar21.svg" alt="MongoDB Logo" width="60%" />
</p>

<p align="center">
  🚀 Your go-to guide for learning <strong>MongoDB</strong> – from zero to hero.
</p>

---

## 📌 About This Repo

This repository is dedicated to documenting my **MongoDB learning journey** – including notes, tutorials, cheat sheets, code snippets, and practice exercises.

Whether you're new to MongoDB or brushing up on NoSQL skills, this repo might help you too.

---

## 📖 Contents
- 📌 NoSql VS SQL Databases
- ✅ MongoDB Basics
- 🔗 CRUD Operations
- 📦 Schema Design
- 🧠 Aggregation Framework
- ⚙️ Indexing & Performance
- 🛡️ Security & Authentication
- 🌐 MongoDB with Node.js
- 🔄 Replication & Sharding (Basics)
- 🧪 Practice Problems & Mini Projects

---

## 🛠 Tech Stack

| Tool/Tech | Description |
|----------|-------------|
| ![MongoDB](https://img.shields.io/badge/-MongoDB-brightgreen?logo=mongodb&logoColor=white&style=flat) | NoSQL Document Database |
| ![Node.js](https://img.shields.io/badge/-Node.js-339933?logo=node.js&logoColor=white&style=flat) | Backend Runtime (used in some examples) |
| ![Mongoose](https://img.shields.io/badge/-Mongoose%20ODM-880000?style=flat&logoColor=white) | Elegant MongoDB Object Modeling for Node.js |
| ![VSCode](https://img.shields.io/badge/-VSCode-007ACC?logo=visual-studio-code&logoColor=white&style=flat) | My IDE |

---

## 📷 Gallery

<p align="center">
  <img src="https://user-images.githubusercontent.com/63813881/222934730-e9e0b350-261a-490e-9ad3-8f83cbd3a26f.png" alt="MongoDB Compass Example" width="70%" />
</p>

> Sample from MongoDB Compass – an intuitive GUI for interacting with your data.

---

## 🤓 Why MongoDB?

- 🔸 Flexible schema (perfect for fast development)
- 🔸 Great for JSON-style documents
- 🔸 Easy to scale horizontally
- 🔸 Powerful aggregation and indexing
- 🔸 Native support for geospatial data, full-text search, and more

---

## 🧠 Tips While Studying

- Don't memorize, **experiment**.
- Use **Compass** or **Atlas** for visualization.
- Try pairing MongoDB with **Node.js** for real-world context.
- Break down aggregation stages step-by-step.
- Practice writing queries by **thinking in documents**, not tables.

---

## 📁 Structure

- 🔸 ![NoSql vs SQL databases](#nosqlvssql)


---

## NoSql Vs Sql
- nosql = not only sql
- sql databases stores data in tables each table are related to other tables with a relationship
- nosql databases stores data in 4 different forms
	1- Documents
	2- Key-value 
	3- Wide-column
	4- Graph
- in the following content we will talk about each type in detailes

- ACID operations in sql

| Operation   | Description |
|-------------|-------------|
| Atomicity   | The database transaction must be compelety success or fail , Partial success is not allowd                 |
| Consistency | During the database transaction the RDBMS progress from one valid state to another (no valid data allowed) |
| Isolation   | Database transaction must occure in isolation from other transactions (a client who read must stull to client who write)
| Durability  | Data must be presist after a successful operation |

- BASE operations in nosql

| Operation   			| Description |
|-----------------------|-------------|
| Basically Available   |The system is guaranteed to be available for querying by all users (no isolation)              |
| Soft state 			|The value stored in the system may change becuase of the eventual consistency model            |
| Eventualy Consistent  |We may see older versions of data when applying new transactions (no isolation) like in hadoop |


- Types of data:
- Structuerd => a data thatha
- simi-Structured
- Un-Structured

| Data   		 | Description |
|----------------|-------------|
| Structuerd     |Data that has a formal structure like |
| simi-Structured|Data that is structure and un-structre in the same time (Facebook Posts , Emails) , JSON / XML         |
| Un-Structured  |Data that has no formal structure like  images , reports ..etc |

- NoSql databases are suitable for simi and un structured data
- Sql databases are suitable for structured data

- Important Notes

- NoSQl databases are used in buissiness scinarios when data doesn't have a specific schema
- thus nosql dbs are said to be growing horizontally , and sql are said to be growing vertically
- growing horizontally means adding new features to a database (if we have data and we don't know it's schema we can add featuers (columns in sql))
- growing vertically means that we know the schema of out data and we insert new instances / samples of data to it.
- hence NoSql dbs are used with huge data that has no formal schema and can be distibuted.
- NoSql dbs have less constraints on data (unlike sql which has many constraints) which cases some data inconsistencies but this increase the performance (the higher constraints on data the higher proccessing power it needs to apply this constraints).

- nosql dbs has no standarizations as it's opensource.
- nosql has limited query capabilities (we cannot write complex queries like in sql)

- CAP Theory
![img](https://imgs.search.brave.com/9lclC5GOxTPPBVdsCNXh8g0aSFUZwSSctxqQMfwDxUY/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly9tZWRp/YTIuZGV2LnRvL2R5/bmFtaWMvaW1hZ2Uv/d2lkdGg9ODAwLGhl/aWdodD0sZml0PXNj/YWxlLWRvd24sZ3Jh/dml0eT1hdXRvLGZv/cm1hdD1hdXRvL2h0/dHBzOi8vcmF3Lmdp/dGh1YnVzZXJjb250/ZW50LmNvbS9rYXQt/c3Rhci9ibG9nLWlt/YWdlcy9tYXN0ZXIv/Y2FwLXRoZW9yZW0u/MDAxLmpwZWc)

- based on CAP theory the choose between different DBMS depends on what we really need in our buisiness (pick tow)

- Nosql Data Types.
![img](https://imgs.search.brave.com/tInN9awQXc7ORQZphEtbDNtpuyXXP-Ev6ZmgeFhCCPA/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly93d3cu/YWx0ZXhzb2Z0LmNv/bS9zdGF0aWMvY29u/dGVudC1pbWFnZS8y/MDI0LzEyL2VmZTFi/M2ViLTU4MmEtNGQ3/Ny1hZDRlLTEwODk4/NDNjZTg5Ny5wbmc)

- Mangodb is document type nosql database

| **Aspect**                | **SQL Databases**                                                                 | **Document NoSQL Databases**                                                                 |
|---------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **Data Structure**        | Table-based, organized into rows and columns. Suitable for structured data.       | Document-based, using formats like JSON, BSON, XML, or YAML. Suitable for structured, semi-structured, and unstructured data. |
| **Schema**                | Fixed schema, predefined and must be adhered to. Ensures data integrity and consistency. | Flexible schema, dynamic and adaptable data structures. Suitable for evolving data requirements. |
| **Performance and Scalability** | Vertically scalable (upgrade hardware). Efficient for complex queries and transactions. | Horizontally scalable (add more servers). Better for large-scale data and fast read/write operations. |
| **Query Language**        | Use SQL (Structured Query Language) for querying and managing data.               | Use various query languages depending on the type of NoSQL database (e.g., MongoDB's query language, JSON, XML, YAML, binary schema). |
| **Use Cases**             | Transactional systems, banking, ERP systems, user-oriented applications with multiple join operations. | Content management systems, e-commerce, real-time applications, IoT, and big data. |
| **Examples**              | MySQL, PostgreSQL, Oracle, MS SQL Server.                                         | MongoDB, CouchDB, Amazon DocumentDB, ArangoDB. |
| **Data Model**            | Relational, with tables and relationships defined by foreign keys.                | Non-relational, with documents that can contain nested structures and arrays. |
| **Data Redundancy**       | Minimized through normalization.                                                 | Can occur to optimize performance, leading to potential data redundancy and consistency issues. |
| **Complexity in Joins**   | Support complex joins and transactions.                                           | Limited support for joins; often denormalized for performance. |
| **Learning Curve**        | Standardized SQL language, widely understood.                                     | May require learning new query languages and data modeling techniques. |
| **Data Integrity**        | Strong data integrity through constraints and transactions.                       | Data integrity can be managed but is less strict, relying more on application logic. |
| **Horizontal Scaling**    | Generally more difficult to scale horizontally.                                   | Designed for horizontal scaling, making it easier to handle large volumes of data. |
| **Vertical Scaling**      | Easier to scale vertically by upgrading hardware.                                 | Less common; horizontal scaling is more typical. |
| **Real-Time Applications**| Suitable for applications requiring complex transactions and joins.                | Optimized for fast read/write operations, ideal for real-time applications. |
| **Big Data**              | Can handle large datasets but may require sharding or partitioning.               | Designed to handle large datasets with ease, often used in big data applications. |

![img](https://i.imgur.com/Viqs3rL.png)
![img](https://i.imgur.com/aoZSZ7L.png)



---

## Mongodb Basics

- Mongodb database contains collections , each collection contains documents
- like RDBMS each database contains tables , each table contain rows

- the document is a JSON files , actually it's BSON files , each file is unified via `_id` it's like the primary key in the table
- but the `_id` (GUID) is created randomly using some kind of algorithms that it cannot be gussable

- Bson It is a computer data interchange format used mainly as a data storage and network transfer format in the MongoDB database.
• It is a binary form for representing simple data structures .
• BSON is faster to scan for specific fields than JSON.
• BSON adds some additional types such as a date data type and a byte-array (bindata) datatype.
• Client drivers serialize data to BSON, then transmit the data over the wire to the db.
• Data is stored on disk in BSON format. Thus, on a retrieval, the database does
 very little translation to send anobject out, allowing high efficiency.
• The client driver unserialized a received BSON object to its native language
 format.


## Mongodb Getting started

- mongodb is cross-platform DBMS , so it's available in numeros of platrofrms

### Windows
- For windows folks , head and download the [mongodb Community edition](https://www.mongodb.com/try/download/community)

- Create file to hold the data (Default: C:\data)

- Run your mongo server by navigating to your extracted(C:\Program Files\Mongodb) file > bin >
- Run: `mongod.exe –dbpath` mongod stands for “Mongo Daemon”. mongod is a background process used by MongoDB. The main
purpose of mongod is to manage all the MongoDB server tasks.
- Run your mongo shell
- Run: mongo.exe to run queries.
- Mongo shell is a command line shell that can interact with the client (for example, system administrators
and developers).

### Linux

- select your distro and hit download
- install the package with your package manager (dpkg for debian based distros for instance)
- `dpkg -i path_to_mongodb.deb`

```
# Start the MongoDB service
sudo systemctl start mongod

# Optional: Enable it to run on boot
sudo systemctl enable mongod

# Check the status
sudo systemctl status mongod
```

- to interact with mongo use `mongosh`

### Docker
- this is the way i perfer to deal with any new technology / software i learn espicially databases.
- now we have tow different ways the first one is download the server image and then finding any other software to interact with this server , the other one is download the image and interacting with the server itself via `mongosh`

- let's go for first option
- pull the image `docker pull mongo`
- or simply run the `docker run` command , it will download the image if it's not exists on your local machine
```
docker run -d \
--name mongo-server \
-e MONGO_INITDB_ROOT_USERNAME=mongoadmin \
-e MONGO_INITDB_ROOT_PASSWORD=LikeAndSubscribe \
-p 27017:27017 \
-v mongodemo:/data/db \
mongo:latest
```
- now this will make a container named mongo-server with some envrionment variables (username , password) to authenticate to the database server , then we forward the port from `docker_container_ip:27017` to `localhost/127.0.0.1:27017`

- the `-v` option is used to specify the storage of this container will be in the `/data/db` , this is recommended as when we delete the container the data inside of it will be removed as well ,so we keep that data persistant on our local machine.

- now if you `docker ps -a` you should see that mongo-server is up and running.
- now you can connect and interact with the server via different softwares (Studio 3T , NoSqlBooster , Robo 3T)
- if you a `cmd` guy you can download `mongosh` and connect to your db server
- for debian based linux :
```
curl -fsSL https://pgp.mongodb.com/server-6.0.asc | sudo gpg -o /usr/share/keyrings/mongodb-server-6.0.gpg --dearmor
echo "deb [ signed-by=/usr/share/keyrings/mongodb-server-6.0.gpg ] https://repo.mongodb.org/apt/ubuntu $(lsb_release -cs)/mongodb-org/6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list
sudo apt update
sudo apt install -y mongodb-mongosh

```

- connect using `mongosh "mongodb://<username>:<password>@localhost:27017"`

- if you a `GUI` guy you can use mongo extention in vscode

- hmm... things are little missy right?
- well , we can use `docker compose` to fire it up
```
version: '3.8'
services:
  mongo: 
    image: mongo:7.0
    environment:
      MONGO_INITDB_ROOT_USERNAME: mongadmin
      MONGO_INITDB_ROOT_PASSWORD: pass
    ports:
      - 27017:27017
    volumes:
      - mongodata:/data/db
volumes:
  mongodata:
    driver: local
```
- execute `docker compose up -d` in the same directory of the yaml file.

- please note:
- if you saw something like this error:
![img](https://i.imgur.com/EeHC82H.png)
- it means that your CPU is a little bit old and don't support AVX  instructions (idk wtf is this)
- you should use older version of mongodb like 4.4
```
services:
  mongo:
    image: mongo:4.4
    container_name: mongodb
    ports:
      - "27017:27017"
    volumes:
      - mongodata:/data/db
    environment:
      MONGO_INITDB_ROOT_USERNAME: mongadmin
      MONGO_INITDB_ROOT_PASSWORD: pass

volumes:
  mongodata:

```

- you can use the above build.

### Basic commands

- `show dbs` shows available databases.
- the `admin , config , local` databases are system databases.
- `db` shows your curretn database , default is `test`
- `use db` switch db (if exists) or create a new one if it doesn't exists (to see the new created database it must contain atleast one collection otherwise it will created in memory)

- `db.dropDatabase()` drops the database i'm currently use
- see more examples in the `Mongo Demo.txt` file (ITI)