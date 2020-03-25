# Configuring Pre/Post Pipeline Stages

##  Pre/Post CD Stage

##### Pre-deployment Stage
Configure actions like db migration, that you want to run before the deployment.

![Add CI Pipeline](/cd_pre_build.jpg "Add CD Pipeline")

`Execute in application Environment`: If checked, the pre-cd / post-cd pods are created in the deployment cluster otherwise they're created in the devtron build cluster,
running in Deployment cluster is recommended if your scripts interact with the cluster services which are not publically exposed

##### Post-deployment Stage
Configure actions like jira ticket close,that you want to run after the deployment.

![Add CI Pipeline](/cd_post_build.jpg "Add CD Pipeline")

`Execute in application Environment`: If checked, the pre-cd / post-cd pods are created in the deployment cluster otherwise they're created in the devtron build 
cluster, running in Deployment cluster is recommended if your scripts interact with the cluster services which are not publically exposed

<br>


