
Pods :

$ kubectl get pods 
NAME                                     READY   STATUS             RESTARTS   AGE
amir-node-redis                          1/1     Running            0          69m
amir-node-redis-6d54874477-7psvg         1/1     Running            0          12s
amir-node-redis-6d54874477-cqv5t         1/1     Running            0          12s
amir-node-redis-6d54874477-gx5ch         1/1     Running            0          12s
amir-node-redis-6d54874477-j5qhd         1/1     Running            0          12s
amir-redis-77b64d4668-pdz2z              1/1     Running            0          7m17s
amir-redis-pod                           1/1     Running            0          104m

$ kubectl logs amir-node-redis-6d54874477-7psvg
redis connected to redis://amir-redis-service:6379
listening at http://localhost:5000

services : 

amir-node-redis             
amir-redis-service 

$ kubectl get services
NAME                        TYPE           CLUSTER-IP     EXTERNAL-IP      PORT(S)          AGE
amir-node-redis-service     LoadBalancer   10.3.36.31     141.95.163.57    5000:32152/TCP   9m37s
amir-redis-service          LoadBalancer   10.3.15.159    141.95.163.35    6379:

dans le navigateur :
141.95.163.57:5000
It is working, good job
