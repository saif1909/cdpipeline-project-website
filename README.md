# Project to deploy static website in AWS S3 bucket using AWS codepipeline
*   Technologies used:
    *   Git
    *   Github
    *   AWS codebuild
    *   AWS codepipeline
    *   AWS S3(for hosting)

*   Project Description:
    *   Project is aimed at automating the deployment of a static website in AWS S3 bucket using its hosting feature
    *   for CI we used git and github as version control system and AWS codebuild to build the code
    *   for CD we have used AWS codepipeline with three stages 
        *   getting source files from github using webhooks
        *   building the source code using AWS codebuild
        *   deploying in S3 bucket
*   Steps Involved:
    *   Creating the git repository in local and adding source files
    *   creating new project in github and adding the project URL as remote branch
    *   Generating the SSH keys using SSH-keygen and adding public key to github 
    *   Committing the local changes to remote repository
    *   creating new project in AWS codebuild and adding git repository URL with webhooks
    *   creating S3 buckets for deploying and changing the bucket settings to host a static website
    *   creating a new AWS codepipeline and adding the stages of source, build and deploy
    *   Attaching newly created IAM roles for codepipeline with required S3 bucket access
    *   Running the codepipeline
    *   If codepipeline runs successfully check the files in S3 bucket and using S3 Url
    *   check the deployment process by commiting a new changes from local git repo and see if changes are reflected in the S3 url
*   Challenges faced:
    *   errors while running codepipeline in build stage which is fixed by giving S3 access to the roles created for codepipeline
 

