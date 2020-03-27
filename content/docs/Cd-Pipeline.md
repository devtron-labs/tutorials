# CD Pipeline 

## Create CD Pipeline

![Add CI Pipeline](/workflow-editor5.PNG "Add CI Pipeline")

Click on "+" on CI Pipeline to attach a CD Pipeline

<br />

![Add CI Pipeline](/workflow-editor6.PNG "Add CI Pipeline")
Select Deploy to Environment to create CD Pipeline


<br />

![Workflow](/workflow-editor8-resize.PNG)

<img src="/workflow-editor8.PNG" alt="drawing" width="450" height="500"/>

Key | Description
----|----
`Pipeline Name` | Enter the name of the pipeline to be created
`Environment` | Select the environment
`Deployment Strategy` | Select the type of deployment strategy that  you want to enable by clicking "Add Deployment Strategy"


Click on `Create Pipeline` to create the CD Pipeline

<br />

![Add CI Pipeline](/workflow-editor9.PNG "Add CI Pipeline")

The CD Pipeline is created

<br />


## Update CD Pipeline 

You can update the CD Pipeline, updatations such as adding Deployment Stage, Deployment Strategy but you cannot update the name of CD Pipeline or it's Deploy Environment, if you require to change such configurations you need to make another CD Pipeline 

<br>

 To Update a CD Pipeline, go to the App Configurations and then click on Workflow editor
 
 <br>

![Update CD Pipeline](/update_pipeline_cd.jpg "Update CD Pipeline")

Click on your CD Pipeline to Update/Delete the  CD Pipeline

<br>


![Update CD Pipeline](/edit_cd_pipeline.jpg "Update CD Pipeline")

Click on `Update Pipeline` to update the CD Pipeline

<br>


## Delete CD Pipeline

If you no longer require the CD Pipeline, you can also Delete the Pipeline.

<br>

![Delete CD Pipeline](/edit_cd_pipeline.jpg "Delete CD Pipeline")


Click on `Delete Pipeline` to delete the CD Pipeline

<br>


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



## Triggering CD Pipelines

![CI Pipelines](/CI3.JPG "Triggering CI Pipelines")

After CI Pipeline is complete, CD Pipeline can be triggered by selecting "Select Image".

![CI Pipelines](/CD1.JPG "Triggering CI Pipelines")

Select an image to deploy and then click on "Deploy" to trigger the CD Pipeline.
The running images are tagged as "Running"


![CI Pipelines](/depdebug1edit.JPG "Triggering CI Pipelines")

The status of the current deployment can be seen by selecting App Details which shows "Progressing" for 1-2 minutes and then gradually shows "Healthy" based on the deployment strategy.
Here, it can be seen that triggering CD Pipeline was successful and the deployment is in "Healthy" state.



[To further diagnose deployments, Click here](../debugging-deployments-and-monitoring)



