---
title: Deploying MongoDB Helm chart
weight: 2
---

# Deploying mongoDB Helm chart

## Introduction 

Let's assume that you are building an application which needs mongoDB. 


![An image](../../../mongo.jpg) <!-- .element height="50%" width="70%" "border"="1px solid #D0D4D9" "padding"="16px"-->

&nbsp;&nbsp; 

Deploying applications as Helm Charts is the easiest way to create applications on Devtron. 

This guide will introduce you to how to deploy the mongoDB's Helm chart. 


## 1. Discover the Chart from the Chart Store

Select the `Charts` section from the left pane, you will be landed to the `Chart Store` page. Click on `Discover` and find `stable/mongodb-replicaset` Helm Chart.

&nbsp;&nbsp;

![Create Group](../../../first.jpg  "Create Groups")

&nbsp;&nbsp;

## 2. Configure the Chart 

After selecting the stable/mongodb helm chart, click on `Deploy` 

&nbsp;&nbsp;

![Create Group](../../../second.jpg  "Create Groups")

&nbsp;&nbsp;

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

&nbsp;&nbsp;

![Create Group](../../../mongo1.jpg  "Create Groups")

&nbsp;&nbsp;

Click on `Deploy` after you have finished configuring the chart. 

<br />


## 3. Check the Status of Deployment

After clicking on `Deploy` you will land on a page, that shows the Status of the deployment of the Chart. 

The Status of the chart should be `Healthy`. It might take few seconds after  initiating the deployment of the chart.

&nbsp;&nbsp;

![Create Group](../../../mongo4.png  "Create Groups")

&nbsp;&nbsp;

In case the Status of the deployment is `Degraded` or takes a long time to get deployed. 

Click on the `Status` or check the logs  of the pods to debug the issue.


## 4. Extract the Service name

Copy the service name, it will be used to connect your application to mongoDB .

&nbsp;&nbsp;

![Create Group](../../../mongo6.png  "Create Groups")&nbsp;&nbsp;

&nbsp;&nbsp;
























