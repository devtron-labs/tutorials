# Deploying Charts

![Deployment Charts](/depchart1.JPG "Deployment Charts")

Select Discover and then select the chart that you want to use

![Deployment Charts](/depchart2.JPG "Deployment Charts")

Select the version that you want to use from the upper right corner

![Deployment Charts](/depchart3readme.JPG "Deployment Charts")

Click on README.MD to get more idea about the configurations of the chart

Select Deploy to deploy the chart


Key | Description
----|----
`App Name` | The name of the app
`Project` | Project of the app
`Environment` |Environment of the app to be deployed
`Chart Version` | Version of the chart to be used

The configuration values can be edited in the section given below Chart Version.


![Deployment Charts](/depchart4config.JPG "Deployment Charts")
ReadMe.md present on the left can be used by the user to set configuration values


![Deployment Charts](/depchart4readme.JPG "Deployment Charts")
Hit Deploy Chart to deploy the chart


![Deployment Charts](/depchartdeployedredo.JPG "Deployment Charts")
You can see the status of the chart deployed

User can click on Values.Yaml to reconfigure the deployment



![Deployment Charts](/depchartreconfig.JPG "Deployment Charts")
Configuration values can be edited over here by the help of ReadMe.md

Select Update And Deploy to update new settings



# Deploying Chart Groups 

To deploy multiple applications and work with them simulataneously, you can use `Chart Groups`.

To create Chart Groups 
Click on  `Discover` and Click on `Create Group`

![Chart Group](/screen2.jpg  "Chart Groups")

Add the Group Name and Description and click on `Create Group`

![Create Group](/create_group.jpg  "Create Groups")

You can select the Charts that you want to add in your Chart Group by clicking on '+' sign. 
You can select a particular chart multiple number of times according to your requirements.

![Select Chart ](/select_charts.jpg  "Select Charts")

Select the `Version` and `Values` for your charts.

You can use `Default Values` or the `Custom Values`, just make sure the Value that you select for your Chart is comptabile with the `Version` of the Chart that you are using.

![Select Chart ](/select_charts2.jpg  "Select Charts")


