# aws-ecr-codepipeline
This repository demonstrates how you can use Terraform to provision a AWS CodePipeline &amp; CodeBuild setup that builds and pushes Docker containers to AWS ECR.

1. clone repo locally
2. cd into the ifrastructure folder find cicd-pipeline-with-ecr.tf
3. edit file replacing below values  with what you want
  * repo_name                 = ""your-docker-image-build-name"                                                       
  * organization_name         = "yourorg"    
4. run terrafrom apply
  * ex: terraform apply -auto-approve -var image_name=yourdockerfile
  
5. look for output from terraform, find "ecr_image_respository_url"

6. in aws console find your newly created codecommit repo , should be value you specified in the .tf file as "repo_name"

7. Clone this repo to your workstation
  * you may need to setup HTTPS Git credentials for AWS CodeCommit if you havent already.

8. Add your docker file, code, buidlspec.yml, buildspec_test.yml to this local cloned repo.

9. Modify the buildspec.yml file add   "ecr_image_respository_url" where  indicated, under build and post build.
  
10. git add., git commit -am"initial" then git push the new files to code commit.

11. in aws console go to codepipline to see your pipeline working.

12. if it doesnt work, troubleshoot.
