# vue
vue.js document

# how to setup docker for db
1. run below command on docker installed terminal 
docker container run  -p 3306:3306 \
                      -e MYSQL_ROOT_PASSWORD=root \
                      -v ~/mariadb:/var/lib/mysql \
                      --name mariadb_container mariadb:10.1.40
-> first line : port forawrding 3306 for mariadb
-> second line : set environmental variable for mariadb password
-> third line : sync volume host and container -> datas on container are volatile data
-> forth line : set containe name and image version

2. connect to container and create database and tables
docker exec -it mariadb_container /bin/bash
mysql -p \ root
run components on /vuw/DB/tb_create
