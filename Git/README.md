### Git Best Practices
#### Commit-related best practices:
* Use descriptive and meaningful commit messages
* Commit in relatively small chunks
* Commit only related work
* Adequately configure the commit authorship (name and email address) with git config

#### Avoiding very large deviations between local and remote repository:
* Keep your feature/bugfix branch up-to-date with remote master and/or develop branch. So pull often from remote git repository
* Branches shouldn’t be open for too long or master branch should be merged into your feature/bugfix branch often

#### Other:
* Don’t "git push" straight to main branch
* Use -force push carefully! Do NOT force push into master or develop branches or better only when working alone in a branch
* Create a separate branch for each feature or bugfix and name the branch with prefix “feature/xx” and “bugfix/xxx” respectively
* Doing Code Reviews via Merge Requests
* Use .gitignore file to ignore e.g. editor specific files, build folders