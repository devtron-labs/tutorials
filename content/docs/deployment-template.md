# Deployment Configurations

![Deployment Template](/dep-temp.PNG "Deployment Template")

## Container

```html
ContainerPort:
    name: app
    port: 8080
    servicePort: 80
```

Key |Description
----|----
`name` | name of the container
`port` | port for the container
`servicePort` | service port for the container


## Liveness Probe

```html
LivenessProbe:
  Path: ""
  port: 8080
  initialDelaySeconds: 20
  periodSeconds: 10
  successThreshold: 1
  timeoutSeconds: 5
  failureThreshold: 3
```


Liveness probe is required to check whether the given container is working and responding to requests or not. Certain specifications can be provided to check the condition for checking the liveliness of a given container.



Key | Description
-----|-----
`Path`  |It define the path where the liveness needs to be checked.
`failureThreshold` |It defines the maximum number of failures that are acceptable before a given container is not considered as live.
`initialDelaySeconds` |It defines the time to wait before a given container is checked for liveliness.
`periodSeconds` |It defines the time to check a given container for liveness.
`successThreshold` |It defines the number of successes required before a given container is said to fulfil the liveness probe.
`timeoutSeconds` |It defines the time for checking timeout.





## Readiness Probe

```html
ReadinessProbe:
  Path: ""
  port: 8080
  initialDelaySeconds: 20
  periodSeconds: 10
  successThreshold: 1
  timeoutSeconds: 5
  failureThreshold: 3
```



Readiness defines whether a given container is ready or not.

Key  |Description
---|---
`Path`                |It define the path where the rediness needs to be checked.
`failureThreshold`    |It defines the maximum number of failures that are acceptable before a given container is not considered as ready.
`initialDelaySeconds` |It defines the time to wait before a given container is checked for readiness.
`periodSeconds`	      |It defines the time to check a given container for readiness.
`successThreshold`    |It defines the number of successes required before a given container is said to fulfil the rediness probe.
`timeoutSeconds`      |It defines the time for checking timeout.
## Autoscaling 

```html
autoscaling:
  enabled: false
  MinReplicas: 1
  MaxReplicas: 2
  TargetCPUUtilizationPercentage: 90
  TargetMemoryUtilizationPercentage: 80
```



Autoscaling is a feature provided by kubernetes for automatically scaling up or scaling down a container.<br />

Key   |Description
-------|--------
`MaxReplicas`			    	|Maximum number of replicas allowed for scaling.
`MinReplicas`			    	|Minimum number of replicas allowed for scaling.
`TargetCPUUtilizationPercentage`    	|The target CPU utilization that is expected for a container.
`TargetMemoryUtilizationPercentage`	 |The target memory utilization that is expected for a container.
`enabled`			    	|to enable autoscaling or don't enable it.


## Image

```html
image:
  pullPolicy: IfNotPresent
 
```
Image is used to access images in kubernetes, pullpolicy is used to define the instances calling the image, here the image is pulled when the image is not present,it can also be set as "Always". 
## Ingress

```html
ingress:
  enabled: false
  annotations: {}
  path: ""
  host: ""
  tls: []
```


Ingress is used in kubernetes to provide an interface between the users and the various contents of the container and proxy ports, it also provides load balancing as well as SSL.
Here enabled is used to enable or disable  given ingress.

Key |Description
----|----
`enabled` | Enable or disable ingress
`annotations`|  To configure some options depending on the Ingress controller
`path`| Path name
`host` | Host name
`tls` | It contains security details


 
 ## Ingress Internal
 
```html
ingressInternal:
  enabled: false
  annotations: {}
  path: ""
  host: ""
  tls: []
```

It provides definition for the internal ingress.

Key |Description
----|----
`enabled` | Enable or disable ingress
`annotations`|  To configure some options depending on the Ingress controller
`path`| Path name
`host` | Host name
`tls` | It contains security details


 
## Resources

```html
resources:
  limits:
    cpu: '1'
    memory: 200Mi
  requests:
    cpu: '0.10'
    memory: 100Mi
```

Resources are required to set CPU and memory usage.
### Limits

Limits make sure a container never goes above a certain value. The container is only allowed to go up to the limit, and then it is restricted.<br />

  ### Requests
 
 Requests are what the container is guaranteed to get.


## Service

```html
  service:
    type: ClusterIP
    annotations: {}
```


Service is an abstraction which defines a logical set of Pods and a policy by which to access them.


ClusterIP-This default type exposes the service on a cluster-internal IP. You can reach the service only from within the cluster.


## Volumes

```html
 volumes: []
```

It is required when some values need to be read from or written to an external disk.


## Volume Mounts

```html
volumeMounts: []

```

It is used to provide mounts to the volume


## Affinity 

```html
Spec:
  Affinity:
    Key:
    Values:
```

Spec is used to define the desire state of the given container.
Inter-pod affinity allow you to constrain which nodes your pod is eligible to be scheduled based on labels on pods.


## Tolerations

```html
tolerations:
  key: "key"
  operator: "Equal"
  value: "value"
  effect: "NoSchedule"

```

A given pod can access the given node and avoid the given taint only if the given pod satisfies a given taint.


## Arguments

```html
args:
  enabled: false
  value: []
```

This is used to give arguments to command 


## Command

```html
command:
  enabled: false
  value: []
```

It contains the commands for the server.

Key     | Description
-------|--------
`enabled`  |To enable or disable the command.
`value` |It contains the commands.


## Prometheus

``` html
  prometheus:
    release: monitoring
```

It is a kubernetes monitoring tool and the name of the file to be monitored as monitoring in the given case.It describes the state of the prometheus.


## Grace Period

```html
GracePeriod: 30
```
If it has expired then the task is requeued to be executed again.




## Min Ready Seconds

```html
MinReadySeconds: 60

```

Minimum time pod should be ready to check readiness of a pod


## Server

```html
server:
  deployment:
    image_tag: 1-95a53
    image: ""
```

It is used for providing server configurations.



### Deployment

It gives the details for deployment

Key     | Description
-------|--------
`image_tag` |It is the image tag
`image`      |It is the URL of the image



## Service Monitor

```html
servicemonitor:
  enabled: false
```

It gives the set of targets to be monitored.

## Db Migration Config

```html
dbMigrationConfig:
  enabled: false
```

It is used to configure database migration

## Application Metrics

Application metrics can be enabled to see your application's metrics-CPU usage,Memory Usage,Status,Throughput and Latency.

# Deployment Strategies
```html
deployment:
  strategy:
  ```
It is used to assign strategy to deployment.
<br />
 
  
 ## Blue Green Stategy
 ```html
blueGreen:
  autoPromotionSeconds: 30
  scaleDownDelaySeconds: 30
  previewReplicaCount: 1
  autoPromotionEnabled: false
```

Key   | Description
------|------
`autoPromotionSeconds` | It will make the rollout automatically promote the new ReplicaSet to active Service after this time has passed
`scaleDownDelaySeconds` | It is used to delay scaling down the old ReplicaSet after the active Service is switched to the new ReplicaSet.
`previewReplicaCount` | It will indicate the number of replicas that the new version of an application should run
`autoPromotionEnabled` | It will make the rollout automatically promote the new ReplicaSet to the active service.

<br />

## Rolling Strategy
```html
rolling:
  maxSurge: "25%"
  maxUnavailable: 1
```

Key   | Description
------|------
`maxSurge` | No. of replicas allowed above the scheduled qauntity.
`maxUnavailable`| Maximum number of pods allowed to be unavailable.

<br />

## Canary Strategy
```html
canary:
  maxSurge: "25%"
  maxUnavailable: 1
  steps:
    - setWeight: 25
    - pause:
        duration: 15 # 1 min
    - setWeight: 50
    - pause:
        duration: 15 # 1 min
    - setWeight: 75
    - pause:
        duration: 15 # 1 min
```

Key   | Description
------|------
`maxSurge` | It defines the maximum number of replicas the rollout can create to move to the correct ratio set by the last setWeight
`maxUnavailable` | The maximum number of pods that can be unavailable during the update
`setWeight` | It is the required percent of pods to move to next step
`duration` | It is used to set the duration to wait to move to the next step.

<br />

## Recreate 
```html 
recreate: 
```
It terminate the old version and release the new one.

[Does your app has different requirements in different Environments? Also read Environment Overrides](../environment-overrides)




