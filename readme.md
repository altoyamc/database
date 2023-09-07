sudo systemctl start docker
sudo docker pull mysql:latest
sudo docker run --name localdb -e MYSQL_ROOT_PASSWORD=password -p 3306:3306 -d mysql:latest
sudo docker ps
sudo docker exec -it localdb mysql -uroot -p
sudo docker stop localdb
sudo docker rm localdb