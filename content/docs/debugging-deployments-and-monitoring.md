# Debugging Deployments And Monitoring
## Debugging Deployment


If the deployment of an app is not successful, then debugging needs to be done for successful deployment.

This can be done through App Details section which can be accessed by Applications->App_Name->App Details.Over here, the status of the app can be seen as Healthy.If there are some error with deployment then the status won't be Healthy.


.

### Events

![Debuggind Deployment](/depdebugeventedit.JPG "Debuggind Deployment")
Apart from these metrics, Events of the app are available on bottom left corner

Events shows the events that took place during the deployment of an app.These events are visible duirng the first 15 minutes of deployment of the app.


### Logs

![Debuggind Deployment](/depdebuglogsedit.JPG "Debuggind Deployment")

Logs contain the logs of the pod deployed which can be used by the user for debugging.

### Pod Status

![Debuggind Deployment](/depdebugpodstatusedit.jpg "Debuggind Deployment")

The Pod Status shows the status of the pods deployed and check whether the pods are up or not.

### Other

![Debuggind Deployment](/depdebugotheredit.jpg "Debuggind Deployment")

Status of Pods, ReplicaSet, Services, Endpoints, Ingress, ConfigMap, Secret, ExternalSecret, StatefulSet and ServiceMonitor can be accessed by clicking on the name of that component.

## Monitoring

![Debuggind Deployment](/depdebug1edit.JPG "Debuggind Deployment")

Monitoring of an app can be done from here.

Metrics like CPU Usage, Memory Usage, Status 5xx, Throughput and Latency are visible over here.

Key | Description
----|----
`CPU Usage` | CPU being used by app
`Memory Usage` | Memory being used by app
`Status 5xx,4xx,2xx` | Response status hits
`Throughput` | Throughput of the app
`Latency` | Latency of the app









  