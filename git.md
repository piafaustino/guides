# SVI's guide to git

## General tips
- Don't commit straight to `master`. Create a new branch, and merge it using a pull request. 
- 



## Creating a feature branch

```
$ git checkout -b [name-of-branch]
```

This creates a new branch which originates from your current branch. Generally, you'll want to branch from the lastest version of master. 

```
$ git checkout master
$ git pull
```

To avoid merge conflicts, you want generally want to create a new branch based off the latest version of master. 


## Opening a PR

Once your branch is pushed, you can create a PR. 

```
$ git push origin [branch-name]
```

#### Using HUB

```
$ git pull-request
```

hub will open a text editor to let you set the PR title and description right from the command line. 


#### Using GitHub.com

- Go to GitHub.com and find the repo.  
- Go to the branches tab. 
- Click the `New pull request` button next to your branch

## Rebasing 

```
$ git rebase origin/master
## Hub

hub is a command line tool that wraps `git` in order to extend it with extra features and commands that make working with GitHub easier.

hub is great, it lets you do thinks like open PRs without leaving the command line!

To install hub, follow the [installation instructions](https://github.com/github/hub#installation). And don't forget to [set up aliasing](https://github.com/github/hub#aliasing)!