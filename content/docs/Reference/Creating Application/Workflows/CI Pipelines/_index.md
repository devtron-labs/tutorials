---
weight: 10
---
# CI Pipelines

<br>

## Create Workflow

Workflow is a logical sequenece of different stages used for continous integration and continous deployment of an application

<br>
![Create new workflow](./workflow-editor.PNG "Create new workflow")
Click on Create Workflow to create a new workflow
<br>

![Create new workflow](./workflow-editor1.PNG "Create new workflow")
Enter the desired name of the workflow and click on Add Workflow to add a new workflow
<br>

##  Create CI Pipeline


<br>
![Add CI Pipeline](./workflow-editor2.PNG "Add CI Pipeline")

<br>
After creating the workflow,click on Add CI Pipeline to add a new CI Pipeline
<br>

![Add CI Pipeline](./add_pipeline.jpg "Add CI Pipeline")

<br>
Click on Continous Integration to create a new CI Pipeline

<br>
![Create CI Pipeline](./create_pipeline.jpg "Create CI Pipeline")
<br>
Click on Create Pipeline to create the  pipeline

Key | Description
-----|-----
`Pipeline Name` | Name of the pipeline
`Source Type` | Select the source through which CI Pipeline will be triggered.
`Branch Name/Tag Regex` | Enter branch name/tag regex
`Pre-build Stages` | Scripts to be executed before building image
`Post-build Stages` |  Scripts to be executed after building image
`Advanced Configurations` | Arguments for CI

<br />

## Update CI Pipeline

You can update all the CI pipeline configurations after the CI pipeline is created except for the pipeline name, if you wish to change that you need to create another CI Pipeline

<br>
 To Update a CI Pipeline, go to the App Configurations and then click on Workflow editor
 
 <br>
 

![Update CI Pipeline](./update_pipeline_ci.jpg "update CI Pipeline")

<br>

Click on your CI Pipeline, to update the changes to your CI Pipeline.

<br>


![Update CI Pipeline](./edit_pipeline.jpg "update CI Pipeline")


<br>
Click on `Update Pipeline` to update the changes you have made to your CI Pipeline

<br>

## Delete CI Pipeline 

You can delete the CI pipeline, if you don't require the CI pipeline. You can only delete CI Pipeline if you have no CD Pipeline created in your workflow or to delete CI Pipeline you first have to delete CD Pipeline if you have created it.

<br>
To Delete a CI Pipeline, go to the App Configurations and then click on Workflow editor

<br>

![Delete CI Pipeline](./edit_pipeline.jpg "update CI Pipeline")


<br>
Click on `Delete Pipeline` to delete the CD Pipeline

<br>


##  Pre/Post CI Stage

##### Pre-build Stages: 
These stages are run in sequence before the docker image is built

<br>
![Create new workflow](./pre_build.jpg)
<br>


##### Post-build Stages
These stages are run in sequence after the docker image is built


<br>
![Create new workflow](./post_build.jpg)
<br>

## Automated Test suite integration in CI step using devtron-ci.yaml

User can run the Test case using the Devtron Dashboard `or` by including the Test cases in `devtron.ci.yaml` file in the source git repository. For reference, check: [https://github.com/kumarnishant/getting-started-nodejs/blob/master/devtron-ci.yaml](https://github.com/kumarnishant/getting-started-nodejs/blob/master/devtron-ci.yaml)

The test cases given in the script will run before the Test Cases given in the  `devtron.ci.yaml`


<br>

![Yaml File](./yaml.jpg "Create Yaml File")

<br>

Field | Description
------|------------ 
`version`   | specify the version of yaml
`appliesTo` | applies the changes to a specified branch 
`type`      | branch type on which changes are to be applied, it can be BRANCH_FIXED or TAG_PATTERN 
`value`     | branch name on which changes are to be applied, it can take a value as name of branch ("master") or as a regular expression ("%d.%d.%d-rc")
`script`    | script which you want to execute, you can also execute the docker commands here
`beforeDockerBuildStages` | script to run before the docker build step
`afterDockerBuildStages`  | script to run after the docker build step
`outputLocation`          | location where you want to see the output of report of Test cases 

<br>



## External CI Pipeline

You can use Devtron for Deployments on Kubernetes while still using your own CI tool such as Jenkins. External CI feature can be used for such cases where 
the CI tool is hosted outside Devtron architecture.

<br>


![Create CI Pipeline](./external_pipeline.jpg "External CI Pipeline")

<br>

You can send the 'Payload script' to your CI tool such as Jenkins and `Devtron` will receive the build image everytime the CI Service is triggered or
you can you use the `Webhook URL` which will build image everytime CI Service is triggered using `Devtron` Dashboard. 

<br>

<br>


Key | Description
-----|-----
`Pipeline Name` | Name of the pipeline
`Source Type`   | 'Branch Fixed' or 'Tag Regex'
`Branch Name` | Name of the branch

<br>


## Linked CI Pipeline

If one code is shared across multiple applications Linked CI Pipeline can be used, and only one image will be build for multiple applications because
if there is only one build, it is not advisable to create multiple CI Pipelines.

<br>
![Create CI Pipeline](./linked.jpg "Linked CI Pipeline")

<br>