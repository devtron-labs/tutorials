# Debugging Deployments
![Debuggind Deployment](/depdebug1edit.JPG "Debuggind Deployment")

If the deployment of a pod is not successful, then debugging needs to be done for successful deployment.

This can be done through App Details section.Over here, the status of the app can be seen as Healthy.If there are some error with deployment then the status won't be Healthy.

To debug issues with deployment, metrics like CPU Usage, Memory Usage, Status 5xx, Throughput and Latency can be used.

Key | Description
----|----
`CPU Usage` | CPU resource used by pod
`Memory Usage` | MEmory resource being used
`Status 5xx` | Response status
`Throughput` | Throughput of the pod
`Latency` | Latency of the pod

Apart from these metrics, Events of the pods which are visible for 15 minutes after the deployment of the pod are available on bottom right corner.

![Debuggind Deployment](/depdebugeventedit.JPG "Debuggind Deployment")

Events shows the events that took place during the deployment of a pod.These events are visible duirng the first 15 minutes of deployment of the pod.


![Debuggind Deployment](/depdebuglogsedit.JPG "Debuggind Deployment")

Logs contain the logs of the pod being deployed which can be used by the user for debugging.

![Debuggind Deployment](/depdebugpodstatusedit.jpg "Debuggind Deployment")

The Pod Status shows the status of the pod being deployed and check whether the pod is up or not.

![Debuggind Deployment](/depdebugotheredit.jpg "Debuggind Deployment")








  
