# My git example

This is a simple git example

To start a git project, run

`git init`

To see what changes are in the folder, run

`git status`


>$ git status
>On branch master
>
>Initial commit
>
>Untracked files:
>  (use "git add <file>..." to include in what will >be committed)
>
>README.md
>desktop.ini
>
>nothing added to commit but untracked files present (use "git add" to track)
>

Now, let's add desktop.ini to gitignore, run

`echo "desktop.ini" > .gitignore`

Then, let's add our README.md to tracking, run

`git add README.md`

If you have even more file to add and don't want to do it one by one, simply run

`git add .`

Now you are almost done, to commit your changes, run

`git commit`

you will now be prompted to enter a commit message

Once your changes are committed, your local copy of git is ready for later use. If you want to share it on a GitHub repository or alike, add a git remote to your local git (Note: you might need to head to GitHub to create a empty / bare repository first)

`git remote add origin https://github.com/bowenwen/my_git_example.git`

`git push -u origin master`

You might now need a new branch, to either collaborate on a new feature or testing out stuff outside of your master branch code, to do this, simply run:

`git branch my_branch`

If you run `git status` now, you will see that you are still on the master branch, to work in the new branch, you need to check out the new branch. Make sure to commit or stash all your changes before switching branch as it will discard any changes:

`git checkout my_branch`

This is where I save a new `README.md`, run `git status` again, you will see `README.md` has changes, let's commit and push to the new branch:

`git add .`

`git commit`

`git push origin my_branch`

Finally, if you are interested in taking a closer look at the different branches and their commit history, try

`gitk`

Now, if you want to merge the two branches on GitHub or alike, you may do so. Doing so brings master branch up to date to my_branch. Let's pull the changes from GitHub, and check out what have changed with `gitk`, let's do a last final commit to master to finish off this tutorial.

`git checkout master`

`git pull origin master`

`git add.`

`git commit`

`git push origin master` 

You are now ready to take on the world with your new git skill!
