### Elastic Compute Cloud (EC2)

* A **virtual server** in AWS Cloud, providing computing capacity

* Steps to deploy a web application on EC2 instance
  1. Create an EC2 instance on AWS
  2. Connect to EC2 instance with ssh
  3. Install Docker on remote EC2 instance
  4. Run Docker container (docker login, pull, run) from private repository
  5. Configure EC2 Firewall to access application externally from the browser

* Steps to launch EC2 instance
  1. Choose OS Image
  2. Choose capacity
  3. Network configurations
  4. Add storage
  5. Add tags
  6. Configure Security Group

* Connect to EC2 server via ssh using downloaded private ssh key:
```
ssh -i secret.pem user@ip-address
```

#### Deploy to EC2 Instance from Jenkins
* Steps to deploy to EC2 instance
    1. Connect to EC2 instance from Jenkins server via ssh (ssh agent)
    2. Execute "docker run" on EC2 instance

* Steps to connect to EC2 instance from Jenkins server via ssh (ssh agent)
    1. Install SSH Agent Plugin
    2. Configure credential
    3. Use credential in "deploy" stage in Jenkinsfile