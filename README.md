
# CRUD Express API using docker and docker compose
This project is a tutorial for implementing CRUD operations using PostGres, express as well as docker and docker compose. 

The dependencies are as follows:
-docker V.27.2.0
-node v.20.11.1
-PostGres v.14.13

All others are managed by docker and docker containers but they use the following dependencies.
-node 20 image imported from docker hub 

For the tests you'll require the REST extension in VScode by Huachao Mao



## Deployment

To deploy this project go to the directory and

Start the docker containers using docker compose if newer docker version
```bash
  docker compose up
```
Else the below command for older versions of docker and docker compose
```bash
  docker-compose up
```
You can use whatever testing/API tool you want like postman, I've used REST VScode extension as mentioned in the description. In the test script run the GET /setup API request before everything else or you'll get server error as the db is not populated. 
```bash
GET http://localhost:13000/setup
```

After that you can use the GET methods for accessing all school records
```bash
GET http://localhost:13000
```

Below is the post method for populating the DB with records
```bash
POST http://localhost:13000
Content-Type: application/json

{
    "name": "John Doe",
    "location": "1227 madison ave"
}
```

__The server starts at 13000 even though the terminal might say it starts at 3000 that is because of the port mappings in dockerfile.__


