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
6. Make a comment for a pull request.
7. Make changes in our code when our pull request is still active.
8. Review another's pull request.
9. Make sure we are up to date with default branch.
10. Answering reviews and push it back.

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

## 6. Make a Comment for a Pull Request

So far, so good. Before continue with issues on GitHub, there are some matters we're gonna touch on. Such as making comments on PR (from now on PR means Pull Request).

Now I'm going to make a comment for your PR. Embrace it and answer me! :grin:

But first, please read these articles:
- About Comments
  - Commenting on a pull request: https://help.github.com/articles/commenting-on-a-pull-request/
  - Creating a permanent link to a code snippet: https://help.github.com/articles/creating-a-permanent-link-to-a-code-snippet/
  
* Go to your Pull Request when notification come.
* Reply those comments (just write something it doesn't matter).
* Make sure you leave a reaction to comments! :thumbsup::-1::heart:

## 7. Make Changes in Your Code When Your Pull Request is still Active.

There are always typos in the code :smiley: Don't be shy to comment each other's code and encourage yourself and other geckos to be more **_GLORIOUS!_** :sunglasses:

* Make requested changes in the file on your local.
  - Make sure you are in the correct branch! **Your branch** :sunglasses:
* Make the commit. Let me remind you:
  - `git status` : Check the working directory for unstaged files.
  - `git add -A` : Add them all to stage. (You might see the term: _Staging changes_).
  - `git status` : Check your staged files. Is that what you want?
    - Defining the what you want: type `git diff` and see what has changed?
    - If those are not the changes you want to commit, it is not too late. Think about the `git reset`
    - If so, make the commit already!
  - `git commit -m "Your commit message"`
  - `git status` again to see if everything is ok.
    - If you want to `git log` to see all commit. And give it a try on `git log --oneline`
* Push it again.

  - `git push origin <Your Branch Name Here!>`

Hopefully, your Pull Request is now updated. Go and check it on GitHub!

## 8. Review Another's Pull Request
* What is that _Pull Request Review_? Please read the listed articles below:
  - About Pull Request Reviews
    - About pull request reviews: https://help.github.com/articles/about-pull-request-reviews/
    - Reviewing proposed changes in a pull request: https://help.github.com/articles/reviewing-proposed-changes-in-a-pull-request/
    - Viewing a pull request review: https://help.github.com/articles/viewing-a-pull-request-review/
* So, you know what is reviewing a PR. I have asked to review each other's PRs now.
* Please go and check it, and;
  - Write some comments here and there.
  - Request PR's owner to add a div element to his/her HTML file.
    - Don't ask so much, just a div. You decide what to write!
* Complete Review with requesting change and submit it.

## 9. Make Sure We are up-to-date with Default Branch
Now, we have something to update. But before we will do more changes, it is a good idea that checking that is our default branch up-to-date. We want to do this because we want to minimize the merge conflicts.

So, you may say nothing change with our default branch (`master` in this case) but you are wrong. While I wrote this README.md, I'm pushing commits to master and overwrite it. So, your README.md file on your local and my README.md file (as long as you read these lines) are different. Go and check it, you can't find these lines in README.md on your local.
  - _Note: Shalini you won't see any changes in  README.md file. Because when you will `git pull`, you will have the latest master branch on remote. But that's OK, anyway you do these steps, too._

Let's make our local master is up-to-date.

* First, terminal on your local, check out to master branch.

  - `git checkout master`

* Second make a pull from remote repository.

  - `git pull origin master`
  - Go and check README.md file again. If eveything went OK, you will see the updated file.

* Now go back to your branch (In my case it is daris-calinor)

  - `git checkout <Your Branch Name>`

    - _Note-1: If you forget your branch name type `git branch` It will list all your local branches._

    - _Note-2: If you want to see all branches (local + remote) type `git branch -va`_
    
    - _Note-3: When using terminal, write two or three letter of the command/branch name/file name etc. and press TAB key to auto-complete._ 
    
* When you are in your branch check the logs:
  - `git log`
    - _Note: When you merge with `git merge` there is a commit added to your log. (yes there are other ways for merging strategies, like `git rebase` but we will use this one.)_
    
* So what we did:
  - Go to default branch
  - Pull it from remote
  - Go to our branch
  - Merge with default branch
  - Now we are up-to-date and ready to work on
  
* **This will be our one of the main things we will do regularly in our code sprints.**

## 10. Answering Reviews and Push it Back
* Now, all you need to do is make those changes and push it again.
* You know all the process.
* After you have updated your pull request please [Request a Pull Request Review](https://help.github.com/articles/requesting-a-pull-request-review/) from the team member who wanted the changes.
* When you have requested for PR Review of another team-mate, go and review it. If everything is like commented, submit a Approved Review.
* I will merge the Approved Reviews with the master.
