### Identity and Access Management (IAM)
* With IAM service you can specify **who can access which services and resources**
* Create and manage AWS Users and Groups
* Assign policies (set of permissions)

```
    * ROOT user is created by default
    * ROOT user has unlimited privileges
    * Best Practice: Create an admin user with less privileges that manages the whole AWS account
```

### Different Types of IAM Users
1. **Human Users**
2. **System Users:** For example Jenkins needs permission to
deploy Docker containers on AWS

### Groups
* For granting access to multiple IAM users

### IAM Roles
* IAM role is similar to an IAM user
* Instead of being uniquely associated with one person, a
role is intended to be assumable by anyone who needs it
* Also Policies cannot be assigned to AWS services directly
* So role is used to **grant AWS services access to other AWS services**

```
  How to:
  1. Create IAM Role
  2. Assign Role AWS Service
  3. Attach Policies to that Role
```

* For more information, refer to the AWS IAM documentation: 
* https://docs.aws.amazon.com/IAM/latest/UserGuide/

### Regions & Availability Zones (AZ)
* Cloud providers have physical data centers
* Data centers all over the world
* **Region =** physical location, where data centers are clustered
> You have to select, which region you want your server
* Each group of logical data centers is called an Availability Zone
* **Availability Zones =** one or more discrete data centers