### Getting commits from main

Say you've been working on some feature, in a branch `feat-1`.

Then, you get a request to make a change to some older code that `feat-1` doesn't touch.

Best practice would suggest

```
# take youself back to main
git checkout main
# make a new branch from main, in which you'll apply the patch
git checkout -b patch-1
# apply the patch, add, commit, and then
git push origin patch-1
# go up to Github get it merged.
```

Now, to keep life simple, you will probably want to put that change back into `feat-1` before you continue, fortunately, it's 
as simple as getting onto the `feat-1` branch and running

```git pull origin main```

In fact, I would consider it good practice to always run the above command when you checkout a branch.

### Making a pull request

Make sure you have all of your work committed on a local branch:

```
git status
git add .
git commit -m "my great new work"
```

Once that's done, you need to send that information to Github via:

```
git push origin <name of branch>
```

From there use the GUI on Github.com to set up a pull request.
