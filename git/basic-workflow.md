# Basic Workflow

Outlined is a basic workflow for working locally on a git branch and then pushing it up to Github to do a PR.  Assuming these would be done sequentially...

Check what branch you are on currently:
```
$ git branch
```

Check if you have any outstanding changes to the files since the last commit:
```
$ git status
```

Get the latest commits to master from GitHub:
```
$ git pull origin master
```

Time to start your coding work.  So create a branch to work on:
```
$ git checkout -b lily-branch-name
```

Anytime you can check what files you've changed by typing:
```
$ git status
```

Happy with your work?  Then:
```
$ git add -A
```

Don't forget to commit your changes after you add them.  Include a useful message.  Or a cute emoji if you are feeling fancy.
```
$ git commit -m "Your commit message goes here"
```

Now push your branch up to Github for code review:
```
$ git push origin lily-branch-name
```

Next, goto Github and create a Pull Request for that branch!

Once, it's approved, you can update your master branch locally and delete the old branch.

First, check what branch you are currently on:
```
$ git branch
```

Switch to master if necessary:
```
$ git checkout master
```

Get the latest commits from Github:
```
$ git pull origin master
```

Finally, delete the old branch locally since it was merged into master:
```
$ git branch -d lily-branch-name
```

And start over the process with a new branch!  Repeat ad nauseam.

```
$ git checkout -b lily-new-branch-name
```
