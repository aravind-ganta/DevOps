### AWS Command Line Interface (CLI)
* Instead of using the UI, we can use the AWS CLI to interact with our AWS account
    * UI Access through password
    * CLI Access through Access key ID and Secret Access Key
* For that you need to configure your AWS CLI:
> aws configure

  ```
  AWS Access Key ID [None]: AKIAEXAMPLE
  AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
  Default region name [None]: us-east-1
  Default output format [None]: json
  ```

#### Command Structure
* aws = the base call to the aws program
* command = the AWS service
* subcommand = specifies which operation to perform

* Launch EC2 Instance via AWS CLI
```
aws ec2 run-instances --image-id ami-0abcdef1234567890 \
    --count 1 --instance-type t2.micro \
    --key-name MyKeyPair \
    --security-group-ids sg-xxxxxxxx \
    --tag-specifications 'ResourceType=instance,Tags=[{Key=Name,Value=MyEC2Instance}]'
```