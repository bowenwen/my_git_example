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


