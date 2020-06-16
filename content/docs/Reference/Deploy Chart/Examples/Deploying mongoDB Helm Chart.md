---
title: Deploying MongoDB Helm chart
weight: 2
---

# Deploying mongoDB Helm chart

## Introduction 

Let's assume that you are building an application which needs mongoDB.

<br />


![Helm Chart](../../../mongo.jpg "Deploying Chart"){: align="center}

<br />


Deploying applications as Helm Charts is the easiest way to create applications on Devtron. 

This guide will introduce you to how to deploy the mongoDB's Helm chart. 


## Step 1: Discover the Chart from the Chart Store

Select the `Charts` section from the left pane, you will be landed to the `Chart Store` page. Click on `Discover` and find `stable/mongodb-replicaset` Helm Chart.

<br />

![Create Group](../../../first.jpg  "Create Groups")

<br />

## Step 2: Configure the Chart 

After selecting the stable/mongodb helm chart, click on `Deploy` 

<br />

![Create Group](../../../second.jpg  "Create Groups")&nbsp;&nbsp;

<br />

Enter the following details, to deploy mongoDB chart:

<br />


Key        | Description
-----------|-------------
`App Name` | Name of the Chart
`Project` | Select the name of your Project in which you want to deploy the chart
`Environment` | Select the environment in which you want to deploy the chart
`Chart Version` | Select the latest Chart Version
`Chart Value` | Select the latest default value or create a custom value


<br />

### Configure `values.yaml` 


In this example `replicas` is set to **1** and `persistenceVolume` is set to **false**. You can configure it according to your project's requirements. 

To learn about different parameters used in the chart, you can check [Documentation of mongodb Helm chart](https://hub.helm.sh/charts/bitnami/mongodb)

<br />


![Create Group](../../../15.jpg  "Create Groups")

<br />

Click on `Deploy` after you have finished configuring the chart. 

<br />


## Step 3: Check the Status of Deployment

After clicking on `Deploy` you will land on a page, that shows the Status of the deployment of the Chart. 

The Status of the chart should be `Healthy`. It might take few seconds after  initiating the deployment of the chart.

<br />


![Create Group](../../../16.jpg  "Create Groups")

<br />


In case the Status of the deployment is `Degraded` or takes a long time to get deployed. 

Click on the `Status` or check the logs  of the pods to debug the issue.


## Step 4: Extract the Service name

Copy the service name, it will be used to connect your application to mongoDB .

<br />


![Create Group](../../../18.jpg  "Create Groups")

<br />























