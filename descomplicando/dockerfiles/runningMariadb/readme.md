docker build -t mariadb .
docker run --name mariadb -e MYSQL_ROOT_PASSWORD=password -dp 3306:3306 mariadb

---

You can enter the container with the following command (although you can also enter it from Docker Desktop etc.).
`docker exec -it mariadb bash`

Furthermore, you can execute SQL from the command line by going inside the container and executing the following.j

`root@4ec9744dff6e:/# mysql -u root -p`
