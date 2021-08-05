# neo4j
Neo4j Tutorial  
### How to Install Docker on your macOS Machine.
- [x] Installation
- [x] [Docker_download](https://download.docker.com/mac/beta/Docker.dmg)
- [x] Double-click the DMG file, and drag-and-drop Docker into your Applications folder.
- [x] You need to authorize the installation with your system password.
- [x] Double-click Docker.app to start Docker.
- [x] The whale in your status bar indicates Docker is running and accessible.
- [x] Docker presents some information on completing common tasks and links to the documentation.
- [x] You can access settings and other options from the whale in the status bar. a. Select About Docker to make sure you have the latest version.

### Run Docker app & wait for a while to ready docker app
> when ready docker app open terminal & run docker command
```bash 
docker run -d -p 80:80 docker/getting-started
```
![docker run command](https://user-images.githubusercontent.com/77927449/128215485-fffbd083-b377-4b27-83f1-8f1643624c64.png)

## Now Start Neo4j pulling
- [x] [Neo4j_docker](https://hub.docker.com/_/neo4j)
![ne04j_docker_pull](https://user-images.githubusercontent.com/77927449/128216121-8842407e-57d0-405d-ab60-b9c768142191.png)

> run this command on terminal
```bash
docker pull neo4j --platform linux/amd64
```
![neo4j pull command](https://user-images.githubusercontent.com/77927449/128215550-d08862cb-da66-42b1-87f4-a43d1253dd71.png)

> check on docker app images tab

![dockerapp_images](https://user-images.githubusercontent.com/77927449/128216860-998ec266-4704-4c8a-ab3a-77f2a16b9852.png)

![docker_image](https://user-images.githubusercontent.com/77927449/128217360-eb9809f9-9760-4f6f-a0e9-3724815da717.png)

### Now run `neo4j` image porcess by terminal with define `port` & login `ID PASSWORD`

```bash
docker run --platform linux/amd64 -p7474:7474 -p7687:7687 -d --env NEO4J_AUTH=neo4j/test neo4j:latest
```
![neo4j image run](https://user-images.githubusercontent.com/77927449/128220664-6368764e-7f33-4576-8314-d86c2d140ac2.png)

#### now your neo4j ready for run on your define port number.
```bash
localhost:7474
```
![neo4j run by port](https://user-images.githubusercontent.com/77927449/128221622-ac800daa-c52b-4c71-99ea-cba03b14b64c.png)
# Congratulation!
#### Now put your ID & Password what we define -
```bash
ID - neo4j
Pass- test
```
##### Login done
![neo4j_login](https://user-images.githubusercontent.com/77927449/128222347-1641f229-ab1d-4578-affd-1469d2fbdd11.png)

> Command Play come -

![command_play_ready](https://user-images.githubusercontent.com/77927449/128223737-156cabe0-da0f-4615-a5c8-0de0c0644701.png)

### Okey LET'S started - `Neo4j` is a `Graph` Database, which language usage is called `Cypher` (Cypher Query Language).
>Cypher’s syntax provides a visual and logical way to match patterns of nodes and relationships in the graph. It is a declarative, SQL-inspired language for describing visual patterns in graphs using ASCII-Art syntax. It allows us to state what we want to select, insert, update, or delete from our graph data without a description of exactly how to do it. Through Cypher, users can construct expressive and efficient queries to handle needed create, read, update, and delete functionality.

### Command -
* MATCH command 
> `MATCH` command which like a query to find me anything matches the quiteria thay i have. 
```bash
MATCH (n) RETURN (n)
```
#### MATCH `(n)` <b>means<b> `n` is node & RETURN `(n)` - return node
  
  ![MATCH_n](https://user-images.githubusercontent.com/77927449/128233093-521a93da-5be3-43f0-a74f-aa62c799b2d1.png)
> no record found & no node found.

### Now we create a node by Command-
  ```bash
  CREATE (n)
  ```
  ![create a node](https://user-images.githubusercontent.com/77927449/128234038-3463c624-103b-450f-bcf5-58144e738c3d.png)
  
> again type the match command to see node
  ```bash
MATCH (n) RETURN (n)
```
> see here created a node by showing graphiclly

  ![node create](https://user-images.githubusercontent.com/77927449/128234384-63d2c12f-b449-4eb2-aac3-fbc9986d6ed8.png)
> you can see, we did not create a relationship here and did not name the node.
  
### How to delete?
  > delete command is -
```bash
MATCH (n) DELETE (n)
```
![node delete](https://user-images.githubusercontent.com/77927449/128235532-f9539000-e44b-4797-9ee6-a9668ce3ab76.png)

  ### How to added a `Person` with color on node-
  ```bash
  CREATE (n:Person{name:'Master-Academy', favoritecolor:'green'})
  ```
  ![create person](https://user-images.githubusercontent.com/77927449/128397965-b6e4d0ab-65f8-47d6-b883-bc233040ad30.png)

  
####  If we need a delete a person -
  ```bash
  MATCH (n:Person {name: 'UNKNOWN'})
DELETE n
```
  
  
