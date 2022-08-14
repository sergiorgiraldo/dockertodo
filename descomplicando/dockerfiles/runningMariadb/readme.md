docker build -t mariadb .
docker run --name mariadb -e MYSQL_ROOT_PASSWORD=password -dp 3306:3306 mariadb
