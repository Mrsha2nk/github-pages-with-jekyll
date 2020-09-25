---
title: "Welcome to my blog"
date: 2019-01-20
---

CI/CD with AWS CodeBuild and Git Branches
Each project in our Cloud Native application is built and deployed using CodeBuild. 
The first step when creating a new component starts with provisioning a CodeBuild instance in the deployment environment using CloudFormation.
Each of our high level deployment environments 
 - development
 - staging
 - production
 
are essentially a *separate AWS Account* (AWS_PROFILE) and a file containing a collection of environment variables (AWS_ENV). 
CodeBuild stores the collection of environment variables so that we can run multiple environments concurrently.
Additionally, the CodeBuild instances are connected to our source code repository, GitHub, which triggers a build when the source is modified.
