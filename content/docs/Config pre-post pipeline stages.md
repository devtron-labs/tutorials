# Configuring Pre/Post Pipeline Stages

##  Pre/Post CI Stage

##### Pre-build Stages: 
These stages are run in sequence before the docker image is built

![Create new workflow](/pre_build.jpg)

##### Post-build Stages
These stages are run in sequence after the docker image is built

![Create new workflow](/post_build.jpg)
<br>

## Automated Test suite integration in CI step using devtron-ci.yaml

User can run the Test case using the Devtron Dashboard `or` by including the Test cases in `devtron.ci.yaml` file in the source git repository. For reference, check: [https://github.com/kumarnishant/getting-started-nodejs/blob/master/devtron-ci.yaml](https://github.com/kumarnishant/getting-started-nodejs/blob/master/devtron-ci.yaml)

The test cases given in the script will run before the Test Cases given in the  `devtron.ci.yaml`


<br>

![Yaml File](/yaml.jpg "Create Yaml File")

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

##  Pre/Post CD Stage

##### Pre-deployment Stage
Configure actions like db migration, that you want to run before the deployment.

![Add CI Pipeline](/cd_pre_build.jpg "Add CD Pipeline")

`Execute in application Environment`: If checked, the pre-cd pods are created in the deployment cluster otherwise they are created in the devtron build cluster

##### Post-deployment Stage
Configure actions like jira ticket close,that you want to run after the deployment.

![Add CI Pipeline](/cd_post_build.jpg "Add CD Pipeline")

`Execute in application Environment`: If checked, the post-cd pods are created in the deployment cluster otherwise they are created in the devtron build cluster

<br>


