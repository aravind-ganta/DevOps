### What is Version Control?
* Also known as "source control"
* Practice of tracking and managing changes to software code
* It enables multiple people to simultaneously work on a single project
* Code is hosted centrally on the internet
* Every developer has an entire copy of the code locally
* Version Control keeps a history of changes
    * You can revert commits
    * Each change labelled with commit message
> Every code change and file is tracked!
* Remote Git Repository: where the code is hosted, e.g. on Gitlab or GitHub
* Local Git Repository:local copy of the code on your machine
* Git Client:to connect and execute git commands can be UI or Command Line Tool
* Code is fetched ("pulled") from
remote repo and "pushed" to it
* Most of the time, Git knows how to merge changes automatically
* But you have a "Merge Conflict", when e.g. same line was changed. Then you need to resolve it manually
* To avoid merge conflicts:
> Best Practice: Push and Pull often from remote repository to stay in sync
* Note: Breaking changes doesn't affect you until you pulled the new code

### Working with Git
#### git add <file>:

* To include the changes of a file
into the next commit
* Moves the changes from "working directory" to the "staging area"

#### git commit -m "commit message":
* To save your changes in your local repository
* Creates a new commit, which you can go back to later if needed

#### git push <remote> <branch-name>:
* After committing your changes, you want to send your changes to the remote Git server
* Uploads your commits to the remote repo

### Setup Git Repository
#### 1) Remote Repository
* Different Git Repositories to register:
    * GitLab
    * github
* These are platforms that host your repository
* Companies have own Git servers hosted by them
* Your repository can be private or public. E.g. Private for companies, Public for open source projects
* You can do a lot via the Platforms UI

#### 2) Local Repository
* Having the remote repository set up, you need a way to connect with the remote repository to copy or "clone" git project to your local machine
* Git client needs to be installed
    * UI client
    * Git Command Line Tool
* You need to authenticate with
GitHub/GitLab/...
* For that, your public SSH Key must be added to the remote platforms:
* As an alternative:
    * If you have already an existing project locally, you can initialize a git repository with "git init"
    * Then you can push it to GitLab/GitHub/...

### Concept of Branches
* Branches are used for better collaboration
* A "main" branch (also called "master") is created by default when a new repository is initialized
* Each developer can then create temporary branches e.g. for a feature or bugfix and work on it without worrying to break the main branch
* Common branch names:
main, dev, feature, bugfix E.g. bugfix/ticket-2134
> Best Practice: 1 branch per bugfix or feature
* Branch is based on main branch. So, it starts from same codebase:
* When finished, the complete branch can be merged back to the main branch
> Goal is to have a stable main branch, ready for production deployment

### Merge Requests or Pull Requests
* For that we have "merge request" or also called "pull request"
* It's basically a request to merge one branch into another
(usually in the main branch)
* Reviewer can see the changes made and either approve or decline the merge request
> Best Practice: Other developer reviews code changes before merging

### Why to know Git as DevOps Engineer?
#### Use Case 1) Infrastructure as Code 
* As a DevOps engineer you write code (configuration files
and scripts) to create and provision infrastructure
* So these files should also "live" in a remote repository and be tracked and versioned by Git
#### Use Case 2) Automation Scripts
* As a DevOps engineer you write automation scripts e.g. with Python to automate different tasks
* Just like software code, files should be:
    * Tracked - history of changes
    * Shareable to collaborate as team
    * Securely stored in one place
#### Use Case 3) CI/CD Pipeline and Build Automation
* CI means: On each merge, checkout code from repository, test and build application
* For that, you need integration for the build automation tool with application git repository
* You need to setup integration with build automation tool and git repository
* You need to know git commands for example for:
    * Getting commit hash of specific commit
    * Check if changes happened in frontend or backend code
#### Git Cheatsheet:
* Source: https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet