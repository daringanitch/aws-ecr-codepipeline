# aws-ecr-codepipeline-demo
This repository demonstrates how you can use Terraform to provision a AWS CodePipeline &amp; CodeBuild setup that builds and pushes Docker containers to AWS ECR.

1. clone repo
2. cd into the ifrastructure folder find cicd-pipeline-with-ecr.tf
3. edit file replacing below values  with what you want
  * repo_name                 = "docker-image-build"                                                             # Required
  * organization_name         = "yourorg"    
4. run terrafrom apply
  * ex: terraform apply -auto-approve -var image_name=yourdockerfile
