#### ordepydockerconaws

#####1 ECS concepts
```
{
  "family":"web",
  "containerDefinitions":[
  {
    "name":"sample-service",
    "image":"",
    "memory":500,
    "cpu":10,
    "essential":true,
    "portMappings":[{"containerPort":80,"hostPort":8080}],
    "environment":[{"name":"PORT","value":"8080"}]
    }
  ]
}
```
#####2
######1 review docker
```
sudo docker build tag rengokantai/name .
```
```
sudo docker run --rm --publish 8080:8080 --name containername rengokantai/name
```
open another shell
```
sudo docker stop containername
```
######2 create ECS
go to ECS, create a stack name = rengo  
create a EC2 instance, create a AMI role with ECS access, with public subnet, ADD following in "Advanced details"
```
#! /bin/bash
echo ECS_CLUSTER=rengokantai >> /etc/ecs/ecs.config
```
after log in EC2(using ec2-user as username)
```
sudo docker ps
```
######3

    
