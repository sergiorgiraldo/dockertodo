docker volume create data_volume
docker volume ls
docker container run -ti --mount type=volume,src=data_volume,dst=/opt/data alpine #change in opt/data, change the volume
docker container run -ti --mount type=volume,src=data_volume,dst=/opt/data debian #you see what was changed in alpine
docker container run -ti --mount type=volume,src=data_volume,dst=/opt/data alpine #you see what is changed in debian
