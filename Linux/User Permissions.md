### Linux User Accounts
* Each user account contains 2 unique identifiers; username and UID
* When a user account is created, its username is mapped to a unique UID

#### Username
* Is used to access the user account
* Also known as login name
* Username is flexible
* Can be changed, but must be unique in system. Two users can’t use the same username

#### UID = User Identifier
* A number assigned by Linux to each user on the system
* UID is fixed. It cannot be changed
* Once assigned, it always remains the same for that user account
* UID is used to authenticate and monitor the activity of user account
* So while username is used by the user, the UID is used by the
system

There are 3 types of user accounts:
#### Superuser account
* Built-in root user - unrestricted permissions
* For administrative tasks: You need to login as Root user or execute commands as root (sudo command)
* Has always a UID of 0

#### User account
* A regular user we create to login
* E.g. tom => /home/tom

#### Service account
* Also called system accounts
* Relevant for Linux Server Distros
* Each service will get its own user
* E.g. mysql user will start mysql application

#### Best Practice in Security:
* Don't run services with root user
* Instead create own user for it

> Always 1 root user per computer
> But multiple regular and service users possible

There are 2 ways to manage the user accounts:
#### Linux - Standalone management
* Unlike Windows, users and groups are unique to the computer but not unique across all computers
* User accounts are managed on that specific hardware
* This means that the UID on Computer 1 might be the exact same UID on Computer 2, even if it is not the same user.

#### Windows - Centrally Managed User Accounts
* Users and groups are unique across all computers in the system
* Login to any hardware that is connected to this system
* That's one of the reasons, why Windows is often preferred in companies or universities
* Employees can login to their account on every computer

* For Linux having multiple users is important for administering servers
* Instead of having a shared user, each user of the team should have a separate user account:
> To give permissions per team member (junior - less permissions, senior - more permissions)
> Traceability - who did what on the system?

### How to manage permissions
* You can give permissions on user or group level
#### User Level
* Give permissions to Users directly
#### Group Level
* Group Users into Linux Groups
* Give permissions to the Group
* The way to go, if you manage multiple Users
* Built-in root user always has a GID (group ID) of 0
#### /etc/passwd file
* Contains a list of all user accounts
* Each user account is stored in an individual line
* Everyone can read it, but only root user can
change the file

#### Basic User & Group Commands
* There are different Linux commands to manage user accounts and groups
* Create a new User
```
```
* Create a new Group
```
```
* Modify a User account
```
```
* Note there are 2 available user & group commands:
```
adduser     addgroup
deluser     delgroup
```
* Interactive
* More user friendly, so easier to use
* It chooses conformant UID and GID values for you
* Creates a home directory with skeletal config automatically
* Or asks for input in interactive mode

```
useradd     groupadd
userdel     groupdel
```
* Low-level utilities
* You need to provide the infos yourself

### File Ownership & Permissions
* User permissions are related to reading, writing and executing files
* Each file and folder has 2 different owners (user + group)
#### 3 types of rights
* Read
* Write
* Execute
#### 3 categories of access
* Owner = user who owns the file/folder
* Group = group that owns the file/folder
* Others = People who aren't part of the owning group or is not the owner
#### Change ownership
* chown <username>:<groupname> <filename>

> By default, owner is the user, who created the file
> Owning group is the primary group of that user

* List file permissions, by printing files in a long listing format (ls -l):

* 3 ways to set or change permissions:

#### 1st way: Adding or removing permissions
```
Example:
sudo chmod g-w config.yaml
```
Means: Remove write permission of group owner from config.yaml file

#### 2nd way: Set the whole permission
```
Example:
sudo chmod g=rwx config.yaml
sudo chmod o=r-x config.yaml
```
Means: Set read, write and execute permission for group for config.yaml file
Set read and execute permission for others for config.yaml file

#### 3rd way: Set permission with numeric values
```
Example:
sudo chmod 740 script.sh
```
Means: Sets full permissions for the owner, read-only for the group, and nothing for the other users.