docker volume create data_volume
docker volume ls
docker container run -ti --mount type=volume,src=data_volume,dst=/opt/data alpine #change in opt/data, change the volume
docker container run -ti --mount type=volume,src=data_volume,dst=/opt/data debian #you see what was changed in alpine
docker container run -ti --mount type=volume,src=data_volume,dst=/opt/data alpine #you see what is changed in debian
---------------
compose
---------------
version: "3.2"
services:
  web:
    image: nginx:alpine
    ports:
      - "80:80"
    volumes:
      - type: volume
        source: mydata
        target: /data
        volume:
          nocopy: true
      - type: bind
        source: ./static
        target: /opt/app/static

networks:
  webnet:

volumes:
  mydata:
