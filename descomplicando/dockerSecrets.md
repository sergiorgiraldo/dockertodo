7659  echo -n "foobarbaz" | docker secret create srg -
 7660  docker secret ls
 7661  docker secret inspect srg
 7662  touch teste
 7663  vim teste
 7664  docker secret create srg-file ./teste
 7665  docker secret ls
 7666  docker secret inspect srg-file
 7667  docker secret rm srg
 7669  docker container
 7670  docker container ls
 7671  docker service create --name nginx -p 8080:80 --secret srg-file nginx
 7672  dk service ls
 7673  dk service inspect
 7674  dk service inspect nginx
 7676  dk service inspect nginx | grep secret
 7677  dk ps
 7678  dk exec -ti 98b9239c60e2 bash
 7679  dk secret inspect srg-file
 7680  echo -n "foobarbaz" | docker secret create srg -
 7681  dk service update --secret-add srg
 7682  dk service update --secret-add srg nginx
 7683  dk exec -ti 98b9239c60e2 bash
 7684  dk ps
 7685  dk exec -ti daf683 bash
