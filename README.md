# n8n-runners


## How to run the n8n-task-runners in AWS Fargate

1. AWS Fargate allows you to run multiple containers in a single cluster

2. So for n8n + external mode, you have the main n8n container and the task runner container inside the AWS Fargate cluster.  

3. You build the docker image `docker buildx build -t n8nio/runners:custom .`. You tag the runners

4. Go to AWS Elastic Container Registry. Create the repository inside the AWS Console fpr AWS ECR

5. Go the the terminal -  
Login Succeeded

aws ecr get-login-password --region us-east-2 | docker login --username AWS --password-stdin 726101440593.dkr.ecr.us-east-2.amazonaws.com

Explain the command below

--region - the AWS region

--username -> AWS is the username of the Docker repo

-- password-stdin -> The password is the accountID and the region. together a unique url that is also the password.  

6. https://docs.aws.amazon.com/AmazonECR/latest/userguide/getting-started-cli.html#cli-create-image


This is the url from AWS dics