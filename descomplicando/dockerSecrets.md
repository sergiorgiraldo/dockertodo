 echo -n "foobarbaz" | docker secret create srg -
 docker secret ls
 docker secret inspect srg
 touch teste
 vim teste
 docker secret create srg-file ./teste
 docker secret ls
 docker secret inspect srg-file
 docker secret rm srg
 docker container
 docker container ls
 docker service create --name nginx -p 8080:80 --secret srg-file nginx
 dk service ls
 dk service inspect
 dk service inspect nginx
 dk service inspect nginx | grep secret
 dk ps
 dk exec -ti 98b9239c60e2 bash #secrets are stored at /run/secrets/
 dk secret inspect srg-file
 echo -n "foobarbaz" | docker secret create srg -
 dk service update --secret-add srg
 dk service update --secret-add srg nginx
 dk exec -ti 98b9239c60e2 bash
 dk ps
 dk exec -ti daf683 bash
