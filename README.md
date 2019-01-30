# aws-ecr-codepipeline-demo
This repository demonstrates how you can use Terraform to provision a AWS CodePipeline &amp; CodeBuild setup that builds and pushes Docker containers to AWS ECR.


Step 1: cd into the ifrastructure folder find cicd-pipeline-with-ecr.tf
*edit file replacing below values  with what you want
*repo_name                 = "docker-image-build"                                                             # Required
*organization_name         = "yourorg"     
