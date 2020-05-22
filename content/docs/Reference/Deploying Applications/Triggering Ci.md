---
title: Triggering Ci
weight: 1

---

## Triggering CI Pipelines
![CI Pipelines](../../tri_ci.jpg "Triggering CI Pipelines")

The CI Pipeline can be triggered by selecting "Select Material"


![CI Pipelines](../../tri_ci2.jpg "Triggering CI Pipelines")

Various commits done in the repository can be seen, here along with details like Author, Date etc.
Select the commit that you want to trigger and then select "Start Build" to trigger the CI Pipeline.

<br />

`Refresh` icon, refreshes Git Commits in CI and Fetches the latest "Repository"

`Ignore Cache` : This option will ignore the previous build cache and create a new build cache. If selected, will take a longer build time than usual.


![CI Pipelines](../../tri_ci3.jpg "Triggering CI Pipelines")

It can be seen that the pipeline is triggered, here and is the **Running** state.

Click on your **CI Pipeline** or Click on **Build History** to get the details about the CI Pipeline such as logs, reports etc.

<br />

![CI Pipelines](../../tri_ci5.jpg "Triggering CI Pipelines")

<br />

You can read the **logs** of the CI Pipeline from here.

<br />

![CI Pipelines](../../tri_ci6.jpg "Triggering CI Pipelines")

Click on **Source code** to know the details such as commit id, Author etc. of the Git Material that you have selected for build.

<br />

![CI Pipelines](../../tri_ci4.jpg "Triggering CI Pipelines")

Click on **Artifacts** to download the reports of the build and to see the details of Docker Repository.


<br />