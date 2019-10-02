# SimpleMEANappwithMongoExpress

1. I consider that you already have Docker else can be downloaded from https://docs.docker.com/install/ (depending on your distribution). Also install docker-compose from https://docs.docker.com/compose/install/ after cloning the repository.

2. Run ```sudo npm update``` after installing npm from ```sudo apt-get install npm``` (for updating npm packages used in angular app) 

3. Mongo Express, Mongo and Nginx images will be pulled from Dockerhub. Run docker-compose.yml ```#sudo docker-compose.yml up -d``` from the directory where you have docker-compose.yml.

4. Once all the containers are up which can be checked from ```#sudo docker ps``` you can go to the defined ports in the local machine to access them.

## Ports can be accessed from terminal as long as they are http:
- Port ``4200`` for Angular    (can be accessed from `curl localhost:4200`)
- Port ``3000`` for Nodejs      (can be accessed from `curl localhost:3000`)
- Port ``8081`` for MongoExpress (UI based mongodb)    (can be accessed from `curl localhost:8081`)
- Localhost for Nginx   (can be accessed from `curl localhost`)

5. Execute ```#sudo docker exec -it "container id" bash``` to go to the shell of the container. Once in it,

```
#mongo (runs Mongodb environment).
#show dbs  (displays dbs).
#use database1  (create databse1)
*(write query)
#db.people.save({ firstname: "Nic", lastname: "Raboy" })
#db.people.save({ firstname: "Maria", lastname: "Raboy" })
#db.people.save({ firstname: "Joseph", lastname: "Martin" })
#db.people.save({ firstname: "Rick", lastname: "Dolhert" })
#db.people.save({ firstname: "Jon", lastname: "Doe" })
*(query for data)
#db.people.find({ firstname: "Nic" })
```

5. Displays the result of the query.
You can also check docker-compose logs from ``sudo docker-compose logs`` when it's running.
