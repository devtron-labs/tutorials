# Deploying Charts

Charts can be deployed individually or by creating a group of Charts.

Both methods are mentioned in the given document.


## Deploy a Chart

![Deployment Charts](/depchart1.JPG "Deployment Charts")

Select Discover and then select the chart that you want to use

<br>

![Deployment Charts](/custom.jpg "Deployment Charts")

Select the Chart Version that you want to use from the upper right corner

Select the Chart Value, you can either use the default Values or create custom value by clicking on ` Create Custom`

Click on README.MD to get more idea about the configurations of the chart

![Deployment Charts](/custom2.jpg "Deployment Charts")

Select `Deploy` to deploy the chart

<br>

Key | Description
----|----
`App Name` | The name of the app
`Project` | Project of the app
`Environment` |Environment of the app to be deployed
`Chart Version` | Version of the chart to be used

The configuration values can be edited in the section given below Chart Version.


![Deployment Charts](/depchart4config.JPG "Deployment Charts")

<br>

ReadMe.md present on the left can be used by the user to set configuration values



![Deployment Charts](/depchart4readme.JPG "Deployment Charts")
<br>

Click on `Deploy Chart` to deploy the chart


![Deployment Charts](/depchartdeployedredo.JPG "Deployment Charts")
You can see the status of the chart deployed

User can click on Values.Yaml to reconfigure the deployment



![Deployment Charts](/depchartreconfig.JPG "Deployment Charts")
Configuration values can be edited over here by the help of ReadMe.md

Select Update And Deploy to update new settings



## Deploy Chart Groups 

To deploy multiple applications and work with them simulataneously, you can use `Chart Groups`.

To create Chart Groups 
Click on  `Discover` and Click on `Create Group`

![Chart Group](/screen2.jpg  "Chart Groups")

Add the Group Name and Description and click on `Create Group`

![Create Group](/create_group.jpg  "Create Groups")

You can select the Charts that you want to add in your Chart Group by clicking on '+' sign. 
You can select a particular chart multiple number of times according to your requirements.
<br>
![Select Chart ](/select_charts.jpg  "Select Charts")

Select the `Version` and `Values` for your charts.

You can use Default Values or the Custom Values, just make sure the Value that you select for your Chart is comptabile with the Version of the Chart that you are using.

![Select Chart ](/select_charts2.jpg  "Select Charts")


To edit the Chart Configuration, Click on 'Edit'

![Edit Chart ](/edit_group.jpg  "Edit Charts")

You can `Add` more Charts to your existing Chart Group or `Delete` Charts from your existing Chart Group. 

After making changes, Click on `Save` to save changes to your Chart Group. 

![Save Chart ](/edit_group2.jpg  "Save Charts")

If you wish to edit the Chart Configuration, Double Click on that Chart and edit the Configurations in YAML File.

![Save Chart ](/edit_chart1.jpg  "Save Charts")

<br>

You can edit the `App Name`, `Chart Version`, `Values`, `Deploy Environment` and the YAML file.

<br>

Key | Description
----|----
`App Name` | The name of the app
`Project` | Project of the app
`Environment` |Environment of the app to be deployed
`Chart Version` | Version of the chart to be used



Click on `Deploy` to initiate the deployment of a Chart in Chart Group.