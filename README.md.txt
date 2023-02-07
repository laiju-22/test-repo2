# Sagemaker Cloudformation Stack Deployment Pipeline

## 1 Sign in

### 1.1 Login Credentials

If you use the AWS Console link, the account alias is pre-filled. For IAM user name, provide your
Philips email address.

- ![](./images/0 sign in)

Note: The AWS access key and password are for programmatic access, so you do not need them
here.

### 1.2 Personas

Directly log on HSDP Development account and initiate the Sagemaker Cloudformation Stack Deployment Pipeline, not switch to a different role.

## 2 Workflow for Sagemaker Cloudformation Stack Deployment Pipeline

### 2.1 Start AWS console and select Cloudformation service

- ![](./images/1 aws console home.png)

### 2.2 Start to create Cloudformation


- ![](./images/2 stacks.png)

- ![](./images/3 create stack.png)

- ![](./images/4 select template.png)

Choose the Cloudformation template from the git repo https://github.com/philips-internal/HSP_PS_AIToolSuite/blob/master/Source/mlops/src/mlops_entry_point.yaml

The Cloudformation template file name is "mlops_entry_point.yaml", upload this file as Cloudformation template.

### 2.3 Provide required stack details

- ![](./images/5 stack details.png)

### 2.4 Configure stack options

- ![](./images/6 config stack.png)

We can include tags, stack policy and Rollback configuration here, default case skip this options.

### 2.5 Verify stack config details

- ![](./images/7 verify config.png)

### 2.6 Verify Cloudformation Stack creation

- ![](./images/8 cf stack creating.png)

In Cloudformation service, select stack then we will see new cloudformation stacks are create in progress.

### 2.7 Verify Pipeline Status

- ![](./images/8 pipe line failed.png)

Verify the pipeline status in CodePipe line service, we will see Pipeline execution is "Failed" status, 
because we not provide a infrastructure script from specific git repo where infrastructure is available.


### 2.8 Initiate github connection

- ![](./images/9 connection.png)

- ![](./images/10 aits infra github connection.png)

- ![](./images/11 update pending connection.png)

- ![](./images/12 install new app.png)

- ![](./images/12 select git account.png)

- ![](./images/13 select required repo.png)

### 2.9 Initiate the release changes

- ![](./images/14 initiate release changes.png)

- ![](./images/15 release.png)

### 2.10 Pipeline Build Execution Restart and Deploying Infracture

- ![](./images/16 build start.png)

- ![](./images/17 deployment.png)

- ![](./images/18 deployment code artifact.png)

- ![](./images/19 deployment done.png)








