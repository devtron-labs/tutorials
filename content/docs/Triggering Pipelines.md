# Triggering Pipelines
## Triggering CI Pipelines
![CI Pipelines](/triggers.JPG "Triggering CI Pipelines")

The CI Pipeline can be triggered by selecting "Select Material"


![CI Pipelines](/CI_select.JPG "Triggering CI Pipelines")

Various commits done in the repository can be seen over here along with details like Author, Date etc.
Select the commit that you want to trigger and then select "Start Build" to trigger the CI Pipeline

Checking on "Ignore Cache" option will ignore the previous cache and create a new one. and will take a longer build time.

At left side, there is "Refresh" icon, it refreshes Git Commits in CI and Fetches the latest "Repository"

![CI Pipelines](/CI2.JPG "Triggering CI Pipelines")

It can be seen that the pipeline has been triggered over here and running

Select the CI Pipeline or select CI Details to get the details about the CI Pipeline.

![CI Pipelines](/CIlogs.JPG "Triggering CI Pipelines")

The logs of the CI Pipeline can be read from here.
CLick on "History" tab to get the history of the CI Pipeline.

![CI Pipelines](/CIhistory.JPG "Triggering CI Pipelines")

It contains the history of the CI Pipeline triggered along with reports of pre-stages and post-stages that can be downloaded by clicking "Download Reports"



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



