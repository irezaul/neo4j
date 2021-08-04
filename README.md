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
