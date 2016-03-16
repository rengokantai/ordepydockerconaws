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


    
