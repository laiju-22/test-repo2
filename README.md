# Sagemaker Cloudformation Stack Deployment Pipeline

## 1 Sign in

### 1.1 Login Credentials

If you use the AWS Console link, the account alias is pre-filled. For IAM user name, provide your
Philips email address.

- ![0-sign-in](./images/0-sign-in.png)

Note: The AWS access key and password are for programmatic access, so you do not need them
here.

### 1.2 Personas

Directly log on HSDP Development account, not switch to a different role.

## 2 Workflow for Sagemaker Cloudformation Stack Deployment Pipeline

### 2.1 Start AWS console and select Cloudformation service

- ![1-aws-console-home](./images/1-aws-console-home.png)

### 2.2 Start to create Cloudformation


- ![2-stacks](./images/2-stacks.png)

- ![3-create-stack](./images/3-create-stack.png)

- ![4-select-template](./images/4-select-template.png)

Select Stacks from cloudformation, and choose create stack option, after that upload manually a specified cloudformation template.

Use the Cloudformation template from the git repo https://github.com/philips-internal/HSP_PS_AIToolSuite/blob/master/Source/mlops/src/mlops_entry_point.yaml

The Cloudformation template file name is "mlops_entry_point.yaml", upload this file as Cloudformation template.

### 2.3 Provide required stack details

- ![5-stack-details](./images/5-stack-details.png)

The required cloudformation stack details are provide manually in specified tabs.

### 2.4 Configure stack options

- ![6-config-stack](./images/6-config-stack.png)

We can include tags, stack policy and Rollback configuration here, in default case skip this options.

### 2.5 Verify stack config details

- ![7-verify-config](./images/7-verify-config.png)

Here, verify the user provided stack details, if everything correct, click on acknowlekdgement option and Submit. 

### 2.6 Verify Cloudformation Stack creation

- ![8-cf-stack-creating](./images/8-cf-stack-creating.png)

In Cloudformation service, select stack then we will see new cloudformation stacks are create in progress.

### 2.7 Verify Pipeline Status

- ![8-pipe-line-failed](./images/8-pipe-line-failed.png)

Verify the pipeline status in CodePipe line service, we will see Pipeline execution is "Failed" status, 
because we are not provide yet infrastructure details from specific git repo where infrastructure is available.

### 2.8 Initiate github connection for provide infrastructure

These are the following steps for initiate github connection to the build pipeline.
Choose the specific git user and repository where the infrastructure script is available, and create the connection.

- ![9-connection](./images/9-connection.png)

- ![10-aits-infra-github-connection](./images/10-aits-infra-github-connection.png)

- ![11-update-pending-connection](./images/11-update-pending-connection.png)

- ![12-install-new-app](./images/12-install-new-app.png)

- ![12-select-git-account](./images/12-select-git-account.png)

- ![13-select-required-repo](./images/13-select-required-repo.png)

### 2.9 Initiate the release changes

After established the connection with git repository, follow the bellow steps for release the changes in CodePipeline,
and re-initiate the cloudformation infrastructure deployment.

- ![14-initiate-release-changes](./images/14-initiate-release-changes.png)

- ![15-release](./images/15-release.png)

### 2.10 Pipeline Build Execution Restart and Deploying Infracture

Pipeline build execution restart and deploy the cloudformation infrastructure.

- ![16-build-start](./images/16-build-start.png)

- ![17-deployment](./images/17-deployment.png)

- ![18-deployment-code-artifact](./images/18-deployment-code-artifact.png)

- ![19-deployment-done](./images/19-deployment-done.png)








