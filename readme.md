# Instructions

Lambda function for cognito autoconfirm users.

[Cognito](https://aws.amazon.com/cognito/) 
[Lambda](https://aws.amazon.com/lambda/)

[Documentation](https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-lambda-pre-sign-up.html)

## Overview

- [Instructions](#instructions)
  - [Overview](#overview)
  - [Configure Lambda](#configure-lambda)
    - [1. Create Lambda Function](#1-create-lambda-function)
    - [2. Upload Code](#2-upload-code)
    - [3. Deploy](#3-deploy)
  - [Configure Cognito](#configure-cognito)

## Configure Lambda

### 1. Create Lambda Function

Go to amazon lambda and create a function

![Create Function](./doc/img/01_lambda_create_function.png)

Set up a name for the function and a runtime, int his case node.js 16.x. Then click "create the function".

![Add Name](./doc/img/02_lambda_set_up_name.png)


  
### 2. Upload Code

You can manually copy the content of index.js of this solution to the index.js of the code source.

![Copy Code](./doc/img/03_lambda_copy_code.png)



Or as alternative you can upload the code, if you are windows user, running the following code. It will just create a .zip file with the index.js

```bash
tar -a -c --exclude="*.zip" --exclude="./doc/" --exclude="readme.md" -f lambda.zip *
```

And then upload from the "Upload from" button.


![Upload code](./doc/img/03_lambda_upload_code.png.png)




### 3. Deploy


The changes are not saved until you deploy it.


![Deploy](./doc/img/04_lambda_deploy.png)

![Deplyoed](./doc/img/05_lambda_deployed.png)


**[⬆ back to top](#overview)**


## Configure Cognito

Go to cognito user pool that you want the user to autoconfirm. Then on "General Settings/Triggers" you will se your function available on each Lambda function dropdown. Select it on Pre sign-up.


![Config Cognito](./doc/img/06_lambda_config_cognito.png)


**[⬆ back to top](#overview)**