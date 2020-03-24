## External CI Pipeline

You can use Devtron for Deployments on Kubernetes while still using your own CI tool such as Jenkins. External CI feature can be used for such cases where 
the CI tool is hosted outside Devtron architecture.

<br>


![Create CI Pipeline](/external_pipeline.jpg "External CI Pipeline")

You can send the 'Payload script' to your CI tool such as Jenkins and `Devtron` will receive the build image everytime the CI Service is triggered or
you can you use the `Webhook URL` which will build image everytime CI Service is triggered using `Devtron` Dashboard. 

<br>

<br>


Key | Description
-----|-----
`Pipeline Name` | Name of the pipeline
`Source Type`   | 'Branch Fixed' or 'Tag Regex'
`Branch Name` | Name of the branch

