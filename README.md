# l7se-do-DockerBasics


* DockerFile: creates a Docker image using the official NGINX image.  Website files are copied into the html folder in the Docker image.
* infrastructure.yml: a CloudFormation IaC template file that creates an EC2 server, plus installs Docker.
* deploy.yml: GitHub Actions workflow that connects to AWS, runs CloudFormation to create the EC2 server, builds & pushes the Docker image to ECR, then uses SSH to connect to the EC2 server, and pull & run the image from ECR.

* Pre-requisites include ECR repository, EC2 key pair and setting up OIDC to allow GitHub to connect to AWS


