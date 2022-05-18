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
Example with ssh on a mac:
- mkdir -p ~/.ssh
- ssh-keyscan -t rsa github.com >> ~/.ssh/known_hosts
- ssh-keygen -t rsa -C "user.email"
- open the public key with this command $ cat ~/.ssh/id_rsa.pub and copy it.
- Add the id_rsa.pub key to SSH keys list on your GitHub profile.

5. Push your code
```
git add . && git push --set-upstream origin main
```

6. create a new branch
```
git checkout -b new-branch
```

7. Switch to an existing branch
```
git fetch && git checkout new-branch-1 && git pull
```
- The git fetch command downloads commits, files, and references from a remote repository to your local repository.
- The git checkout command switches to the sepciefied branch
- The git pull command is used to download content from a remote repository and immediately update the local repository to match the content.

