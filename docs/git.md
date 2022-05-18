# Introduction to git

By far the most widely used modern version control system in the world today is Git.


## git commands

### Getting started:

1. Create a new repo on GitHub/ Bitbucket/ GitLab/ ...
2. Initizalize your project
```
git init
```
3. Connect to your repo
```
git remote add origin git@github.com:SKnoedler/test
```
4. Authenticate (https or ssh)
4.1 SSH (mac os)
- mkdir -p ~/.ssh
- ssh-keyscan -t rsa github.com >> ~/.ssh/known_hosts
- ssh-keygen -t rsa -C "user.email"
- open the public key with this command $ cat ~/.ssh/id_rsa.pub and copy it.
- Add the id_rsa.pub key to SSH keys list on your GitHub profile.


 
