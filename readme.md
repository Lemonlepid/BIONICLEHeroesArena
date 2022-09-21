# BIONICLE Heroes Arena

## Collaboration guide:
First download Git client: https://git-scm.com/downloads (at the top of the page)
When installing, leave all settings as default.

Decide where the project is going to live on your PC. Let's say mine is D:/Games. Make sure to use forward-slashes (/) in your paths, and if there are spaces, include the whole thing in quotes (e.g. "D:/My Games/New Folder/")

Open up Git Bash and type the following:
(you can copy each line and middle-click to paste into the terminal)
```sh
cd D:/Games
git clone https://github.com/Lemonlepid/BIONICLEHeroesArena.git
```
Git will eventually (when you make changes) ask you to log in with your credentials. You will need a GitHub account for this.

When you clone, Git client is a bit outdated and may try to clone the "master" branch. Type the following to fix this:
```sh
git checkout main
```
### Getting the latest changes
When somebody has done work that you want to use, enter the following command to get the latest:
```sh
git checkout main
git pull
```
If you have also edited some of the files that have been changed, you will get a merge conflict. At that point call Tom for help...

### Pushing your changes
When you have done work, you can upload it to the repo by pushing a "commit". A commit is a list of changes, usually accompanied by a message explaining why.
It is best practice to commit often, after each significant step in your work.
```sh
# Get the latest state of the repo before you commit, to avoid merge conflicts later
git checkout main
git pull
# lists all files:
git status
# to list only the tracked files (i.e. files that were already in the repo) do this instead:
git status -uno
# You need to tell Git which changes you want to include in your commit.
# to add a new file to the repo:
git add <filename>
# to automatically add all changed tracked files:
git add * -u
# check the status again, making sure that all the green (staged) files are intended:
git status
# create your commit, with a message explaining what you did
git commit -m "Adding some new functionality"
# push your new commit to the online repo
git push
```
