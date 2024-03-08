# kodey-servereless-sample

This repository is an example Kodey.ai Coding Agent Workflow

## Objectives

In this sample, we will explore how Kodey.ai can create projects and integrate serverless code and automate it.

## Project Setup & Steps 

1. Signup for a new Kodey.ai account or login to your existing Kodey.ai environmenty (link-here)
2. Configure your Kodey.ai integrations to the desired issue tracker and cloud git provider.
3. Fork this repository, and clone it to the cloud git provider of your choosing (Github, Azure DevOps, Bitbucket)
4. Create the sample issue / work item in your issue tracker. Copy and Paste the issue description from below.
5. Execute the below prompt in the Kodey.ai chat UI
6. Validate the commits and pull requests in your cloud git provider

### SAMPLE PROMPT - Github Tools (Making Project That hits API requests extract data and define serverless file)
```
    branch name to create: feature/serverless-project-sample

    Information to agent: Do as the steps below are defined one by one. You are working in github repo so make sure to use tools related to github repo.
    NOTE: You should write the actual implementation of code not just comments. 

    Steps:

    step 1: Using GithubCreateNewBranch tool, Create a new branch with name <branch name to create> first and then do the steps below.

    step 2: Using WebCrawler Tool, get the information on how to authorize when calling fhir cerner api for https://fhir.cerner.com/authorization/.

    stpe 3: Using WebCrawler Tool, understand how to make request to each endpoint mentioned in fhir cerner immunization endpoint from https://fhir.cerner.com/millennium/r4/clinical/medications/immunization/

    step 2:  using GithubCreateNewFile tool, Create a new file called lambda_function.py which have lambda function that will have functions to call the above mentioned endpoints and get the data.
    NOTE: All the credentials and tokens should be stored in environment variables and be read from environment variables in the code.

    step 3: using GithubCreateNewFile tool, cerate a new file called requirements.txt and add the packages required to run the code.

    step 4: using GithubCreateNewFile tool, Create a new Docker file that contains the instructions to build the docker image for the lambda function created in the previous step.

    step 5: using GithubCreateNewFile tool, Create a new file called serverless.yml which should contain the configuration for the serverless framework to deploy the lambda function and the API Gateway.
    
    step 6: using GithubCreatePullRequest tool, create a new Pull Request from the above created branch with title "FHIR CERNER API ENDPOINTS".

```

### SAMPLE PROMPT - Azure DevOps Tools (Making Project That hits API requests extract data and define serverless file)
```
    branch name to create: feature/serverless-project-sample

    Information to agent: Do as the steps below are defined one by one. You are working in azure repo so make sure to use tools related to azure repo.
    NOTE: You should write the actual implementation of code not just comments. 
    
    Steps:

    step 1: Using AzureDevopsBranchesCreateBranch tool, Create a new branch with name <branch name to create> first and then do the steps below.

    step 2: Using WebCrawler Tool, get the information on how to authorize when calling fhir cerner api for https://fhir.cerner.com/authorization/.

    stpe 3: Using WebCrawler Tool, understand how to make request to each endpoint mentioned in fhir cerner immunization endpoint from https://fhir.cerner.com/millennium/r4/clinical/medications/immunization/

    step 2:  using AzureDevopsRepositoryCreateNewFile tool, Create a new file called lambda_function.py which have lambda function that will have functions to call the above mentioned endpoints and get the data.
    NOTE: All the credentials and tokens should be stored in environment variables and be read from environment variables in the code.

    step 3: using AzureDevopsRepositoryCreateNewFile tool, cerate a new file called requirements.txt and add the packages required to run the code.

    step 4: using AzureDevopsRepositoryCreateNewFile tool, Create a new Docker file that contains the instructions to build the docker image for the lambda function created in the previous step.

    step 5: using AzureDevopsRepositoryCreateNewFile tool, Create a new file called serverless.yml which should contain the configuration for the serverless framework to deploy the lambda function and the API Gateway.
    
    step 6: using AzureDevopsPullRequestsCreatePullRequest tool, create a new Pull Request from the above created branch with title "FHIR CERNER API ENDPOINTS".


    step 7: using AzureDevopsIssuesUpdateIssue tool, update the issue status to done.
```

### SAMPLE PROMPT - Jira / Bitbucket (Making Project That hits API requests extract data and define serverless file)
```

    branch name to create: feature/serverless-project-sample

    Information to agent: Do as the steps below are defined one by one. You are working in azure repo so make sure to use tools related to azure repo.
    NOTE: You should write the actual implementation of code not just comments. 
    
    Steps:

    step 1: Using BitBucketCreateNewBranch tool, Create a new branch with name <branch name to create> first and then do the steps below.

    step 2: Using WebCrawler Tool, get the information on how to authorize when calling fhir cerner api for https://fhir.cerner.com/authorization/.

    stpe 3: Using WebCrawler Tool, understand how to make request to each endpoint mentioned in fhir cerner immunization endpoint from https://fhir.cerner.com/millennium/r4/clinical/medications/immunization/

    step 2:  using BitBucketWriteCode tool, Create a new file called lambda_function.py which have lambda function that will have functions to call the above mentioned endpoints and get the data.
    NOTE: All the credentials and tokens should be stored in environment variables and be read from environment variables in the code.

    step 3: using BitBucketWriteCode tool, cerate a new file called requirements.txt and add the packages required to run the code.

    step 4: using BitBucketWriteCode tool, Create a new Docker file that contains the instructions to build the docker image for the lambda function created in the previous step.

    step 5: using BitBucketWriteCode tool, Create a new file called serverless.yml which should contain the configuration for the serverless framework to deploy the lambda function and the API Gateway.
    
    step 6: using BitBucketCreateNewPullRequest tool, create a new Pull Request from the above created branch with title "FHIR CERNER API ENDPOINTS".

    step 7: Update this jira issue status to done.

```

## Once you have set the description of the issue in your relavant system. You need to use kodey UI Chat and execute below statement to get the work done. 

### Github Issue and Github Repo
```
   Get the issue with id <issue_id> from github repo and do as the description of the issue says.
```

### Azure Repo Issue and Azure Repo
```
   Get the issue with id <issue_id> from azure repo and do as the description of the issue says.
```

### Jira Issue and Bitbucket Repo
```
   Get the issue with id <issue_id> from bitbucket repo and do as the description of the issue says.
```

## Confirming Successful Sample Outputs

1. Confirm that the branch was created on the issue / work item
2. Confirm that the code created in the associated pull request contains the following
3. Confirm that the work item/issue/ticket in your relevant issue tracking platform is updated.