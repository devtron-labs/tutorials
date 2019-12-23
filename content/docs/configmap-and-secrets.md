## Config Maps
The ConfigMap API resource holds key-value pairs of configuration data that can be consumed in pods or used to store configuration data for system components such as controllers. ConfigMap is similar to Secrets, but designed to more conveniently support working with strings that do not contain sensitive information.

Click on ConfigMaps to config a map

![Config Map](/config.PNG "Create config map")

Key  | Description
-----|-----
`Name` | Name of the configmap
`Environment Variable` | Select if there are Environment Variables to be injected in pods
`Data Volume` | Select if a directory accessible to all containers running in a pod needs to be added
`Kubernetes ConfigMap` | ConfigMap created by Devtron
`Key` | Key 
`Value` | Value for a given key



![Data Volume](/configvolumepath.PNG "Data Volume")

### Volume Mount Path
Enter the path of the volume mount

![External Config Map](/extconfig.PNG "External config map")

### Kubernetes External ConfigMap
The user will have to ensure that the config map is available to the pod.

Click Save ConfigMap to save the config map




![Config Map Added](/configmapadded.PNG "Config Map is added")

The config map is created




## Secrets 
Secret objects let you store and manage sensitive information, such as passwords, OAuth tokens, and ssh keys. Putting this information in a secret is safer and more flexible than putting it verbatim in a Pod definition or in a container image.

![Secret](/secret.PNG "Secret")
Click on Add Secret to add a new secret



![Add Secret](/addsecret.PNG "Add Secret")

Key | Description
---- | ----
`Name` | Name of the secret to be added
`Data Type` | Data type of the secret to be added
`Data Volume` | Select if a directory accessible to all containers running in a pod needs to be added
`Environment Variable` | Select if there are Environment Variables to be injected in pods
`Key` | Key
`Value` | Value for a given key



![Data Volume](/secretdatavol.PNG "Data Volume")

### Volume Mount Path
Enter the path of the volume mount

![Save Secret](/secretenv.PNG "Save Secret")



Click on Save Secret to save the secret

![Save Secret](/secretadded.PNG "Save Secret")

Secret is added





