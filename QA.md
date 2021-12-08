1. Docker Swarm
   1. what are 2 modes of swarm (cluster and orchestration)
   2. what is swarm node (any machine with docker)
   3. what are node types (manager and worker)
   4. where does swarm configuration stays (in memory etcd)
   5. what is service from docker swarm perspective (containers wrapped with enhance features)
   6. what is the port to support secure client to swarm communication (2377/tcp)
   7. what is the port to support control plane gossip (7946/tcp and udp)
   8. what is the port to support VXLAN-based overlay network (4789/udp)
   9. what is --advertise-addr flag while initializing swarm being used for (publish endpoint)
   10. what is --listen-addr flag while initializing swarm being used for (accept traffic)
   11. what is the default port of advertisement (2379)
   12. what is the command to join a new worker to the swarm 
       1. get join token using - docker swarm join-token worker
       2. use the join token to join - docker swarm join --token <TOKEN> <MANAGER:2377>
   13. what is the command to join a new manager to the swarm
       1. get join token using - docker swarm join-token manager
       2. use the join token to join - docker swarm join --token <TOKEN> <MANAGER:2377> 
   14. what is the state of swarm managers (active-passive)
   15. what is the recommended number of managers (3/5)
   16. what is split brain problem (even number of managers lose right of owning the quorum if partitioned in exact half)
   17. what is locking of swarm (to avoid accidental access of old managers while they rejoin swarm, the swarm can be autolocked, so that the old manager has to pass unloack key before joining swarm)
   18. what is docker service (an unit managed by swarm)
   19. what is the way to initialize a service (docker service create --name --port --replicas <IMAGE_NAME>)
   20. what is the command to list all services (docker service ls)
   21. what is the command to see all the processes next to a service (docker service ps <SERVICE_NAME>)
   22. what is the command to see the state of service (docker service inspect <SERVICE_NAME>)
   23. what is the way to scale a specific service (docker service scale <SERVICE_NAME>=10)
   24. how to remove a service (docker service rm <SERVICE_NAME>)
   25. how to perform rolling update (docker service update --image <NEW_IMAGE> --update-parallelism 2 --update-delay 20s <SERVICE_NAME>)
   26. how to tail docker service log (docker service logs <SERVICE_NAME)
   27. 