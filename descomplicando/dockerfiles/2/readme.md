docker build -t foo .
docker run --name myapache -d -p 80:80 foo
docker exec -ti hashDoContainer bash
