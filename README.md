## Overview Design


![alt text](https://github.com/Fady-Refaat1/cn_nd_Udaconnect/blob/master/docs/architecture_design.png)


# Instruction to run the project 
<ol>
<li>In the main directory Run</li>

```
Vagrant up
```

```
vagrant ssh
```

</li>
<li>copy k3s configurations</li>

```
sudo cat /etc/rancher/k3s/k3s.yaml
```
and copy the file
<li>Go to ~/.kube/config and paste the file</li>
<li>Run 

```
kubectl apply -f deployment/
```
</li>
<li>run the script.sh that in all microservices folders to create and seed the database</li>
<li>OR do this  

```
kubectl exec -it <pod_NAME(If "person the name will person-postgresy5r5yruygjh for example")> -- bash
```

```
vi init_connection_db.sql
```

``` 
psql -U ct_admin -d connection -f init_connection_db.sql
```

</li>
<li>the project on port 

```
localhost:30000
```

</li>
</ol>
