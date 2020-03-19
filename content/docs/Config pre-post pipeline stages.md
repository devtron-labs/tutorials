
# Configuring Pre/Post Pipeline Stages

##  Pre/Post CI Pipeline

![Create new workflow](/pre_build.jpg)


![Create new workflow](/post_build.jpg)

##  Pre/Post CD Pipeline

![Add CI Pipeline](/cd_pre_build.jpg "Add CD Pipeline")

`Execute in application Environment`: If checked, the pre-cd pods are created in the deployment cluster otherwise they are created in the devtron build cluster

Key | Description
----|----
`Pipeline Name` | Enter the name of the pipeline to be created
`Environment` | Select the environment
`Pre-deployment Stage` | Scripts to be executed before deployment

![Add CI Pipeline](/cd_post_build.jpg"Add CD Pipeline")

`Execute in application Environment`: If checked, the post-cd pods are created in the deployment cluster otherwise they are created in the devtron build cluster

Key | Description
----|----
`Deployment Strategy` | Select the type of deployment strategy that  you want to enable by clicking "Add Deployment Strategy"
`Post-deployment Stage` | Scripts to be executed after deployment


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