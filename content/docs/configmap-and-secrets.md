## Config Maps
**Click on ConfigMaps to config a map**
![Config Map](/config.PNG "Create config map")

Key  | Description
-----|-----
`Name` | Name of the configmap
`Environment Variable` | Environment Variables to be injected in pods
`Data Volume` | A directory accessible to all containers running in a pod
`Kubernetes ConfigMap` | ConfigMap created by Devtron
`Key` | Key 
`Value` | Value for a given key

![Data Volume](/configvolumepath.PNG "Data Volume")

### Volume Mount Path
Enter the path of the volume mount

![External Config Map](/extconfig.PNG "External config map")

### Kubernetes External ConfigMap
The user will have to ensure that the config map is available to the pod.

**Click Save ConfigMap to save the config map**


![Config Map Added](/configmapadded.PNG "Config Map is added")

**The config map is created**

## Secrets 

![Secret](/secret.PNG "Secret")
**Click on Add Secret to add a new secret**

![Add Secret](/addsecret.PNG "Add Secret")

Key | Description
---- | ----
`Name` | Name of the secret to be added
`Data Type` | Data type of the secret to be added
`Data Volume` | A directory accessible to all containers running in a pod
`Environment Variable` | Environment Variables to be injected in pods
`Key` | Key
`Value` | Value for a given key

![Data Volume](/secretdatvol.PNG "Data Volume")

### Volume Mount Path
Enter the path of the volume mount

![Save Secret](/secretenv.PNG "Save Secret")

**Click on Save Secret to save the secret**







