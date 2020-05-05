#traefik in docker swarm mode

```
docker network create --driver=overlay traefik-public
docker network inspect traefik-public
docker stack deploy traefik -c traefik.yml
docker logs traefik_reverse-proxy.1.4kqr10ndvs9bty4mane47okng --tail 10
docker stack deploy njs -c  njs.yml
docker stack ps njs 
docker service scale njs_helloworld=5
```


http://<IP>:8080/dashboard
