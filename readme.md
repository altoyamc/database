## Setup docker
sudo systemctl start docker
sudo docker pull mysql:latest
sudo docker run --name localdb -e MYSQL_ROOT_PASSWORD=password -p 3306:3306 -d mysql:latest

## Check docker
sudo docker ps

## Run docker
sudo docker exec -it localdb mysql -uroot -p

## Close and delete docker
sudo docker stop localdb
sudo docker rm localdb

## Access details
Username: root
Password: password
Database Name: localdb
Port: 3306
Ip: 0.0.0.0