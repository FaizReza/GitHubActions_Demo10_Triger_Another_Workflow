## build.yml
#### This demo workflow is to show how to trigger another workflow using repository dispatch event
##### Deploy workflow is triggered with a client payload containing environment information
##### Roken permission is required to trigger another workflow
##### "trigger-deploy" is the event type defined in the deploy workflow
##### Permissions are set to allow creating dispatch events and triggering other workflows
##### This workflow can be triggered manually using workflow_dispatch event
##### Another workflow Deploy.yml listens for the repository_dispatch event to perform deployment

## deploy.yml
#### This demo workflow listens for repository dispatch events to perform deployment
##### The workflow is triggered by the "trigger-deploy" event type which is sent from another workflow defined in Demo10.1_build.yml
##### It retrieves environment information from the client payload
