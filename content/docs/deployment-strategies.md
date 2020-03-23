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