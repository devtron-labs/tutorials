---
bookCollapseSection: false
weight: 31
---
# Debugging Deployments And Monitoring
## Debugging Deployments


If the deployment of an app is not successful, then debugging needs to be done to check the cause of error.

This can be done through **App Details** section which can be accessed by:- 

Applications->AppName->App Details

Over here, the status of the app can be seen as Healthy.If there are some error with deployment then the status won't be Healthy.


.

### Events

![Debuggind Deployment](./app_detail1.jpg "Debuggind Deployment")
Events of the app are accessible from the bottom left corner

Events shows the events that took place during the deployment of an app.These events are available until 15 minutes of deployment of the app.


### Logs

![Debuggind Deployment](./app_detail2.jpg "Debuggind Deployment")

Logs contain the logs of the pods/containers deployed which can be used by the user for debugging.

### Pod Status

![Debuggind Deployment](./app_detail3.jpg "Debuggind Deployment")

The Pod Status shows the critical information like container-image, restartCount, state, phase, podIP, startTime etc. and status of the pods deployed..

### Deleting Pods

![Debuggind Deployment](./app_details4.jpg "Debuggind Deployment")

Pods can be deleted in many cases, for e.g.,
When we need to setup a new environment, we can delete a pod and new pod will be created automatically depending on the replcaCount.

Pods can be deleted by selecting "Delete Pod"


### Other

![Debuggind Deployment](./app_details5.jpg "Debuggind Deployment")

Status of Pods, ReplicaSet, Services, Endpoints, Ingress, ConfigMap, Secret, ExternalSecret, StatefulSet and ServiceMonitor can be accessed by clicking on the name of that component.

## Monitoring

![Debuggind Deployment](./app_detail7.jpg "Debuggind Deployment")

Monitoring of an app can be done from here.

Metrics like CPU Usage, Memory Usage, Status 5xx, Throughput and Latency are visible over here.

Key | Description
----|----
`CPU Usage` | CPU being used by app
`Memory Usage` | Memory being used by app
`Status 5xx,4xx,2xx` | Response status hits
`Throughput` | Throughput of the app
`Latency` | Latency of the app









  
