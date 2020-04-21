---
title: Triggering Cd
weight: 2
bookToc: false
---
## Triggering CD Pipelines

![CI Pipelines](/img/CI3.JPG "Triggering CI Pipelines")

After CI Pipeline is complete, CD Pipeline can be triggered by selecting "Select Image".

![CI Pipelines](/img/CD1.JPG "Triggering CI Pipelines")

Select an image to deploy and then click on "Deploy" to trigger the CD Pipeline.
The running images are tagged as "Running"


![CI Pipelines](/img/depdebug1edit.JPG "Triggering CI Pipelines")

The status of the current deployment can be seen by selecting App Details which shows "Progressing" for 1-2 minutes and then gradually shows "Healthy" based on the deployment strategy.
Here, it can be seen that triggering CD Pipeline was successful and the deployment is in "Healthy" state.



[To further diagnose deployments, Click here](../debugging-deployments-and-monitoring)
