---
title: Triggering Cd
weight: 2
bookToc: false
---

## Triggering CD Pipelines

![CI Pipelines](../../tri_cd.jpg "Triggering CI Pipelines")

After CI Pipeline is complete, CD Pipeline can be triggered by Clicking on 
*Select Image*.

![CI Pipelines](../../CD1.JPG "Triggering CI Pipelines")

Select an image to deploy and then Click on **Deploy** to trigger the CD Pipeline.

The running images are tagged as *Running*


![CI Pipelines](../../tri_cd5.jpg "Triggering CI Pipelines")

The  status of the current deployment can be viewed by Clicking on **App Details** that will show the *Progressing* state for 1-2 minutes and then gradually shows *Healthy* state or *Hibernating* state, based on the deployment strategy.

Here, triggering CD Pipeline is successful and the deployment is in "Healthy" state.


[To further diagnose deployments, Click here](https://docs.devtron.ai/docs/reference/debugging-deployments-and-monitoring/)

