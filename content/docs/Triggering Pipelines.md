# Triggering Pipelines
## Triggering CI Pipelines
![CI Pipelines](/triggers.JPG "Triggering CI Pipelines")

The CI Pipeline can be triggered by selecting "Select Material"


![CI Pipelines](/CI1.JPG "Triggering CI Pipelines")

Various commits done in the repository can be seen over here along with details like Author, Date etc.
Select the commit that you want to trigger and then select "Start Build" to trigger the CI Pipeline

![CI Pipelines](/CI2.JPG "Triggering CI Pipelines")

It can be seen that the pipeline has been triggered over here and running

Select the CI to get the details about the CI Pipeline.

![CI Pipelines](/CIlogs.JPG "Triggering CI Pipelines")

The logs of the CI Pipeline can be accessed from here.

![CI Pipelines](/CIhistory.JPG "Triggering CI Pipelines")

Select "History" to get the hisotry of the CI Pipeline.
It contains the history of the CI Pipeline triggered along with reports of pre-stages and post-stages that can be downloaded by clicking "Download Reports"



## Triggering CD Pipelines

![CI Pipelines](/CI3.JPG "Triggering CI Pipelines")

After CI Pipeline is successfully triggered, CD Pipeline can be triggered by selecting "Select Image".

![CI Pipelines](/CD1.JPG "Triggering CI Pipelines")

The user will have to select an image to deploy and then select "Deploy" to trigger the CD Pipeline.

![CI Pipelines](/CD2.JPG "Triggering CI Pipelines")

The deployment is initiated

![CI Pipelines](/CD3.JPG "Triggering CI Pipelines")

Here, it can be seen that triggering CD Pipeliine was successfull and the deployment is in "Healthy" state.



[To further diagnose deployments, Click here](../debugging-deployments-and-monitoring)



