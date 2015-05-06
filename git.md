# SVI's guide to git

## General Tips

- Don't commit straight to `master`. Create a new branch, and merge it using a pull request. 

## Creating a feature branch

```
$ git checkout -b [your-github-username/name-of-branch]
```

This creates a new branch that originates from your current branch. Generally, you'll want to branch from the latest version of master:

```
$ git checkout master
$ git pull
```

And once you've checked out the latest version of master, you can go ahead and checkout a branch. 

## Rebasing 

Once you've committed some code, it's good practice to rebase. Rebase-ing essentially syncs your branch with another branch, which helps avoid future merge conflicts. 

```
$ git rebase origin/master
```

You can rebase with almost anything: 
* Any remote branch `git rebase origin/pre-req-feature`
* Or your local branches `git rebase my-previous-branch`

## Changing history

### Changing the last commit

```
$ git commit --amend
```

You stage the changes you want by editing a file and running `git add` on it or `git rm` to a tracked file. The subsequent `git commit --amend` takes your current staging area and makes it the snapshot for the new commit.

### Changing multiple commits

To edit the past n commits, for example, the past 3 commits: 

```
$ git rebase -i HEAD~3
```

Running this command gives you a list of commits in your text editor. Note that these commits are listed in the opposite order than you normally see them using the `log` command. 

For each commit listed, you run any of these commands: 

```
# Commands:
#  p, pick = use commit
#  r, reword = use commit, but edit the commit message
#  e, edit = use commit, but stop for amending
#  s, squash = use commit, but meld into previous commit
#  f, fixup = like "squash", but discard this commit's log message
#  x, exec = run command (the rest of the line) using shell
```

You can also remove a commit by deleting that commit's line. 

Before pushing, I generally do an interactive rebase against `origin/master` to see all of the commits I'm about to push. I often fixup multiple small commits into a larger one and reword unclear commit messages. 

```
$ git rebase -i origin/master
```

### Force pushing your new history

If you just overwrote history in your local repo by rebasing or amending commits that have already been pushed, you'll need to force push: 

```
$ git push -f origin [your-branch-name]
```

More info about rewriting history available [here](http://www.git-scm.com/book/en/v2/Git-Tools-Rewriting-History). 

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

## Hub

hub is a command line tool that wraps `git` in order to extend it with extra features and commands that make working with GitHub easier.

hub is great, it lets you do thinks like open PRs without leaving the command line!

To install hub, follow the [installation instructions](https://github.com/github/hub#installation). And don't forget to [set up aliasing](https://github.com/github/hub#aliasing)!
