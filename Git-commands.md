# Git Commands

## Git version

```
git --version
```

## Set user.name and user.email

```
git config --global user.name 'NAME'
git config --global user.email 'EMAIL'
```

## Initialize new repository

```
git init
```

## Get the status of the repository

```
git status
```

## Add files to staging area

```
git add index.html
git add *.html
git add .
```

## Remove files from the staging area

```
git rm --cached index.html
```

## Commit files to the repository

```
git commit
git commit -m "Initial commit"
```

## Create a branch

```
git branch secondbranch
```

## Switch to branch

```
git checkout secondbranch
```

## Merge branches

```
git merge secondbranch
```

## Link to remote

```
git remote add origin https://github.com/MstrBlonde/REPONAME.git
```

## View remote gits

```
git remote
```

## Push to remote

```
git push -u origin master
```

## Clone a repo from remote

```
git clone https://github.com/MstrBlonde/REPONAME.git
```

## Generate SSH key

```
ssh-keygen -t  rsa -b 4096 -C "mstrblonde@gmail.com"
```
