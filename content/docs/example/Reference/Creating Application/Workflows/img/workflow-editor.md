# Workflow Editor
**Workflow is a logical sequenece of different stages used for continous integration and continous deployment of an application**
<br />

<br />

![Create new workflow](./workflow-editor.PNG "Create new workflow")
**Click on Create Workflow to create a new workflow**
<br />

![Create new workflow](./workflow-editor1.PNG "Create new workflow")
**Enter the desired name of the workflow and click on Add Workflow to add a new workflow.**
<br />

![Add CI Pipeline](./workflow-editor2.PNG "Add CI Pipeline")
**After creating the workflow,click on Add CI Pipeline to add a new CI Pipeline**
<br />

![Add CI Pipeline](./workflow-editor3.PNG "Add CI Pipeline")
**Select on Continous Integration to create a new CI Pipeline.**

<br />

<img src="workflow-editor-combo.jpg" alt="drawing" width="400" height="700"/>

Key | Description
-----|-----
`Pipeline Name` | Name of the pipeline
`Source Type` | Select the source through which CI Pipeline will be triggered.
`Branch Name/Tag Regex` | Enter branch name/tag regex
`Pre-build Stages` | Scripts to be executed before building image
`Post-build Stages` |  Scripts to be executed after building image

**Click on Create Pipeline to create the  pipeline**

<br />

![Add CI Pipeline](./workflow-editor5.PNG "Add CI Pipeline")

**Click on "+" on CI Pipeline to attach a CD Pipeline**

<br />

![Add CI Pipeline](./workflow-editor6.PNG "Add CI Pipeline")
**Select Deploy to Environment to create CD Pipeline**

<br />

<img src="workflow-editor7.PNG" alt="drawing" width="450" height="500"/>

Key | Description
----|----
`Pipeline Name` | Enter the name of the pipeline to be created
`Environment` | Select the environment
`Deployment Strategy` | Select the type of deployment strategy that  you want to enable by clicking "Add Deployment Strategy"

<br />

<img src="workflow-editor8.PNG" alt="drawing" width="450" height="500"/>

**Select Create Pipeline to create the CD Pipeline**

<br />

![Add CI Pipeline](./workflow-editor9.PNG "Add CI Pipeline")

**The CD Pipeline is created**

<br />





