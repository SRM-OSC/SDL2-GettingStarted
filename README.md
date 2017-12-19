# SDL2-GettingStarted

## About

This repository is for team members to test their SDL2 skills and create a project according to the code given in the book.
Read the instructions below to understand how to work as a team.

## Working as a group

##### _EACH TEAM MEMBER MUST CLONE THE PROJECT — DO NOT FORK IT!_

## Adding a new feature

> **master** is a protected branch and hence cannot be modified directly by anyone except *srm-osc-admin*.

Everytime someone wants to add a new feature, create a new branch for it and open a pull request when you are done.
If your pull request gets at least 1 approval then it can be merged to master.

## Setting Up Your Branches

*Before creating a new branch, make sure you are up to date with the master branch. Simply:*

```sh
$ git pull origin master
```

Don’t ever work on the master branch. Let’s refresh your memories on how to make branches:

```sh
$ git checkout -b branchName
```

> Tip: Each branch should be made based on each feature, not page. For example, some branches could be:
> fbAuth,
> editUserInfo,
> addingGulp,
> etc.

When you make a branch, it's only created locally. So, we need to make it exist on
your remote so your team members can see it.

```sh
$ git push --set-upstream origin sameBranchName
```

This will make your branch visible on GitHub to other team members and set the upstream to push to
your specific branch. Double check to make sure your new branch is there by going to your
organization on GitHub, then to branches.

## Adding, Committing, and Pushing

##### If you've completed the steps above, you're ready to code on your branch now!

*You add and commit your files the same way you've always done it when you’re on a branch, but:*

> BEFORE YOU COMMIT, MAKE SURE YOU ARE ON YOUR BRANCH, NOT MASTER.

After you add and commit your files, push your changes to your branch on GitHub:

```sh
$ git push origin sameBranchName
```

##### Now, if you’re ready to make a pull request in order to merge your branch's code with Master, head over to GitHub:

* _Your Organization >> Branches >> Your Branch >> Compare & Pull Request_
* _YOUR PULL REQUEST NEEDS AT LEAST 1 APPROVAL IN ORDER TO MERGE_


## Merging Master Into Your Branch

* _THIS PART IS JUST FOR INFORMATION PURPOSES_

You should keep your branch up-to-date with master. First, commit any changes on your branch.
Make sure your work in good shape and committed, so it won't be a difficult process if there are conflicts.

```sh
# on your branch
$ git add -A
$ git commit -m “blah"
$ git checkout master
$ git pull origin master
```

Now, merge your branch with master. There could be conflicts if you haven't been pulling regularly.
No worries, this can usually be fixed in just a few minutes.

```sh
$ git checkout branchName
$ git merge master
```

#### If you tried a merge which resulted in complex conflicts and want to start over, you can recover:

```sh
# on your branch
$ git merge --abort
```

* _ALWAYS DELETE THE BRANCH AFTER IT HAS BEEN MERGED_

## Deleting Branches

When you are finished with a feature, and everything has been merged with the master branch via pull request,
you should delete your branch associated with that feature locally and on GitHub to keep things clean and organized.
You can delete it manually on GitHub by going to the organization then to branches, or you can delete it with:

```sh
$ git push origin :BranchName
```

The difference from before is simply the colon :

To delete your branch locally:

```sh
$ git branch -d branchName
```

To FORCE branch deletion locally:

```sh
$ git branch -D branchName
```

### _Important Reminders:_

* Tell your team every time a pull request has been merged with master. Don’t let your team members fall behind master.
* Pull often, just to be sure. Even if no one has told you about changes on master, pull anyways. It doesn’t hurt.
* Under Branches on GitHub you can find a visual representation of how far behind or head your branch is from master.
* Double check with team members before merging.
* Make sure you are on a branch before you start working. Get in the habit of checking.