# Welcome Glorious Geckos!

Welcome to Glorious Practice for our project workflow!

This is the workflow that we will use in our Sprints while we are sharing codebases each other. I am assuming that:
- You have a GitHub account.
- You have installed Git to your computer and connected with GitHub account.
- You have installed Git Bash or some kind of command line to your computer.
- You know how Git works. Which means that:
  - You know the basic concepts of Git. What *commits* and *branches* are.
  - You know `git status`, `git add`, `git commit` and `git push`
  - If you don't know, please visit these links:
    - https://www.youtube.com/watch?v=noZnOSpcjYY&list=PLg7s6cbtAD15G8lNyoaYDuKZSKyJrgwB-
    - https://www.atlassian.com/git/tutorials/setting-up-a-repository

If we are all on board let's move on! What am I trying to do here with this repo? It's all about getting used to Git and our workflow, made some mistakes and ask questions to each other and the community!

## Our objectives are:
1. Clone this repo.
2. Make our new branch from default branch.
3. Make some changes and commit them.
4. Push our changes to remote.
5. Make a Pull Request.
6. Merge the Pull Request with our default branch.

## 1. Clone this Repo
* Make a new directory on your local device named as 'practice-for-geckos'
* Open Git Bash or an other command line. Make a new directory named *practice-for-geckos* and change directory:

`mkdir practice-for-geckos` and `cd practice-for-geckos`
* Type into terminal: `git clone https://github.com/DarisCalinor/practice-for-geckos.git`

It will download this repo to your local disc.
* `cd practice-for-geckos` to change directory.
* `git status` You should see in command line
```
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
```
* Check for your remote with typing `git remote -v` You should see:
```
$ git remote -v
origin  https://github.com/DarisCalinor/practice-for-geckos.git (fetch)
origin  https://github.com/DarisCalinor/practice-for-geckos.git (push)
```

## 2. Make Our New Branch from Default Branch
* Default branch for this repo is `master`. So, when we create a branch, we are making it from `master`.

_Note: We will use `development` branch as default when we are in the coding sprints._
* Create a new branch with your nickname. I will be using **_daris-calinor_**

`git checkout -b daris-calinor`

_Note: There are other ways to create a branch. You change your branch with `git checkout`, but when you add an `-b` flag, you will first create a branch with given name and then checkout to that branch._
* Now that we are in our branch, we can make some changes!

## 3. Make Some Changes and Commit Them!
* Create a new html file and name it with your nickname! I will be using **_daris_**
* `touch [your nickname here!].html`
* Open the file with your favorite text editor. Copy and paste this:
```
<!DOCTYPE html>
<html>
<head>
  <title>Chingu Voyage-4</title>
</head>
<body>
<div>
  Hello Glorious Geckos!
</div>
</body>
</html>
```
* Save and close the file.
* Go to terminal and type `git status` You will see:
```
$ git status
On branch daris-calinor
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        daris.html

nothing added to commit but untracked files present (use "git add" to track)
```
* Now we have added new file there but it is untracked. Firstly add it to staging area.

`git add daris.html`
_Note: Later you can use `git add -A` to add all changed files together._

`git status` to check. **Always check you added right files to staging area.** Now you will see these lines:
```
$ git status
On branch daris-calinor
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   daris.html
```
* Make the commit!

`git commit -m "Add daris.html file to repo"`

* When you type `git status` again you will see:
```
$ git status
On branch daris-calinor
nothing to commit, working tree clean
```

### Optional: Further reading on writing commit messages, 7 rules and using VIM Editor!
https://chris.beams.io/posts/git-commit/

https://stackoverflow.com/a/36427485/8965331

It is time for the push, Geckos!

## 4. Push Our Changes to Remote
* To push your commit(s) to repo on GitHub simply type:

`git push --set-upstream origin daris-calinor`

_Note: After this you can only use git push for this branch. It will automatically push your commits to defined origin._

* `git status` to check it again. You'll see:
```
$ git status
On branch daris-calinor
Your branch is up to date with 'origin/daris-calinor'.

nothing to commit, working tree clean
```

## 5. Make a Pull Request
* Go to https://github.com/DarisCalinor/practice-for-geckos

* Click Pull Request on the repo menu bar (just right to the Code tab).
* Click green "New Pull Request" button.
* Set base: master and compare: _your-branch-name_ under the Compare Changes heading.
* You will see your recent commit, how many commit that you have sent and how many files are changed.
* Click "Create Pull Request"
* You can change title or commit body or leave it to be.
* Create that pull request!

## 6. Merge the Pull Request with our Default Branch
* I will make the merge, don't worry about that ;)

Try another branches and another commits as you go, get comfortable. If you stuck, fire a question!

After this one we will take look at Issues and Waffle. If you know all of this, just let me know, I'll make the process faster!

Cheers!
