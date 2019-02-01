## Version control

![how not to git](img/howtogit007.png)

Note:
links on top
* https://guides.github.com/introduction/git-handbook/
* https://en.wikipedia.org/wiki/Version_control
* https://en.wikipedia.org/wiki/Distributed_version_control
* https://en.wikipedia.org/wiki/Git
* https://betterexplained.com/articles/a-visual-guide-to-version-control/
* https://betterexplained.com/articles/intro-to-distributed-version-control-illustrated/
* https://github.com/Krten
* http://opensuse.github.io/branding-guidelines/
* https://github.com/hakimel/reveal.js
* https://de.wikipedia.org/wiki/Versionsverwaltung
* https://guides.github.com/features/mastering-markdown/
* https://github.com/arslanbilal/git-cheat-sheet
* https://github.com/detailyang/awesome-cheatsheet
* https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf
* https://betterexplained.com/articles/aha-moments-when-learning-git/
* http://nvie.com/posts/a-successful-git-branching-model/
* http://a5anka.github.io/images/gitflow_5_Vincent_Driessen.png
* https://en.wiktionary.org/wiki/git
* https://git-scm.com/blog
* https://git-scm.com/book/en/v2
* http://rogerdudler.github.io/git-guide/
* https://www.sitepoint.com/git-for-beginners/
* https://www.youtube.com/playlist?list=PLg7s6cbtAD17Gw5u8644bgKhgRLiJXdX4 (Git & GitHub YouTube short tutorials)
* https://linuxacademy.com/blog/linux/git-terms-explained/
* https://learngitbranching.js.org/
* https://lab.github.com/

--

### Why?
* The problem: How to save a file in different versions?
![how not to git](img/howtogit001.png) ![how not to git](img/howtogit002.png)

--

### Root cause
* The existence of the *Save As*-Button or version control can be summed up to a simple root cause: 
  * **You want to work in a new file without destroying the source data** (e.g. a document, source code, a picture or whatever)
* **However** that does not mean, that this is easy to solve ;)

--

### A bit of boring theory ;)
* **Version control** in general describes any **system** to **track changes** in **documents** or **files**
* The **changes** are usually identified by a *number* called **revision number** or just **revision**
  * **Revisions** are **saved** in an **archive** with at least the attributes: **timestamp** and **author**
  * **Revisions** can be **compared**, **restored** and *depending on filetype* **merged**

--

### Easy example 1/2
* **Testdocument.txt** has the following attributes:
  * **Revision**: 0
    * **Author**: Bob
    * **Timestamp**: 2018-01-23T17:04:30+01:00
* **Testdocument.txt** has the following attributes:
  * **Revision**: 1
    * **Author**: Alice
    * **Timestamp**: 2018-01-23T18:04:30+01:00

--

### Easy example 2/2
**Contents of Testdocument.txt**

|Revision 0   | Revision 1   |
|------------ | -------------|
|Hello!       | Hello World! |

---

## Version control systems (VCS)
### Sorry - still some theory ;)

--

### Main tasks 1/2
* **Logging / Tracking** of changes
  * It is possible to find out which **change** was done and by **whom** and **when** at **any time**
* **Restoring** of old **revisions** of **any file**
* **Archiving** of every **state** of a project
  * It is possible to access all **versions** of a project at **any time**

--

### Main tasks 2/2
* **Enabling collaboration** in teams
  * **Coordinating** multiple access on files by different developers
  * **Synchronization** of files between different developers
  * **Short- and Long-term undo** if a file was messed up or will be messed up at some point
  * **Simultanous development** in **different branches**
  * **Merging** from *development* branches to *productive* branches

--

### Common vocabulary 1/2
* Clone
* Branch
* Checkout
* Change
* Commit
* Conflict / Merge conflict
* Resolve
* Forward integration / Reverse integration

Note:
Clone = Cloning means creating a repository containing the revisions from another repository. This is equivalent to pushing or pulling into an empty (newly initialized) repository. As a noun, two repositories can be said to be clones if they are kept synchronized, and contain the same revisions.

Branch = a set of files under version control may be branched or forked at a point in time so that, from that time forward, two copies of those files may develop at different speeds or in different ways independently of each other

Checkout = To check out (or co) is to create a local working copy from the repository. A user may specify a specific revision or obtain the latest. The term checkout can also be used as a noun to describe the working copy.

Change = A change (or diff, or delta) represents a specific modification to a document under version control. The granularity of the modification considered a change varies between version control systems.

Commit = To commit (check in, ci or, more rarely, install, submit or record) is to write or merge the changes made in the working copy back to the repository. The terms commit and checkin can also be used as nouns to describe the new revision that is created as a result of committing.

Conflict = A conflict occurs when different parties make changes to the same document, and the system is unable to reconcile the changes. A user must resolve the conflict by combining the changes, or by selecting one change in favour of the other.

Resolve = The act of user intervention to address a conflict between different changes to the same document.

Forward integration = The process of merging changes made in the main trunk into a development (feature or team) branch.

Reverse integration = The process of merging different team branches into the main trunk of the versioning system.

--

### Common vocabulary 2/2
* Merge
* Pull, Push
* Repository
* Tag
* Trunk
* Working copy
* Head

Note:
Merge = A merge or integration is an operation in which two sets of changes are applied to a file or set of files. Some sample scenarios are as follows:
 A user, working on a set of files, updates or syncs their working copy with changes made, and checked into the repository, by other users.
 A user tries to check in files that have been updated by others since the files were checked out, and the revision control software automatically merges the files (typically, after prompting the user if it should proceed with the automatic merge, and in some cases only doing so if the merge can be clearly and reasonably resolved).
 A branch is created, the code in the files is independently edited, and the updated branch is later incorporated into a single, unified trunk
 A set of files is branched, a problem that existed before the branching is fixed in one branch, and the fix is then merged into the other branch. (This type of selective merge is sometimes known as a cherry pick to distinguish it from the complete merge in the previous case.)

Pull / Push = Copy revisions from one repository into another. Pull is initiated by the receiving repository, while push is initiated by the source. Fetch is sometimes used as a synonym for pull, or to mean a pull followed by an update.

Repository = The repository is where files current and historical data are stored, often on a server.

Tag = A tag or label refers to an important snapshot in time, consistent across many files. These files at that point may all be tagged with a user-friendly, meaningful name or revision number. See baselines, labels and tags.

Trunk = The unique line of development that is not a branch (sometimes also called Baseline, Mainline or Master)

Working copy = The working copy is the local copy of files from a repository, at a specific time or revision. All work done to the files in a repository is initially done on a working copy, hence the name. Conceptually, it is a sandbox.

Head = Also sometimes called tip, this refers to the most recent commit, either to the trunk or to a branch. The trunk and each branch have their own head, though HEAD is sometimes loosely used to refer to the trunk.

--

### Visualization
![Visualization of branches](img/howtogit005.png)

--

### Distributed version control systems 1/3
* **Distributed version control systems** (DVCS) are a **peer-to-peer** based approach to version control
* Advantages over a centralized (*client-server based*) approach are
  * Allows users to work productively when offline
  * Common operations are faster, because there is no need to communicate with a central server
  * Communication is only necessary when sharing changes

--

### Distributed version control systems 2/3
* Further advantages over a centralized VCS
  * Allows private work, users can use their changes for early drafts they do not want to publish
  * Working copies effectively function as *remote backups*
    * This is indeed nothing, a sysadmin would ever recommend
    * Do backups of your machines, you cannot rely on users *working copies* lying on desktop machines

--

### Distributed version control systems 3/3
* Disadvantages compared to a centralized VCS
  * Initial cloning of a repository is slower as compared to centralized checkout (all branches and revision history are copied to your local machine)
  * More storage required for every user to have a complete copy of the complete codebase history

---

## Git

--

### Some facts on git

* A **distributed version control system** (DVCS)
* Aimed at speed, data integrity and support for distributed, non-linear workflows
* Was created by Linus Torvalds in 2005 (for the development of the Linux kernel)
* Free software distributed under GNU GPL v2

--

### The name of Git
* *"I'm an egotistical bastard, and I name all my projects after myself. First 'Linux', now 'git'."* (Linus Torvalds)
  * (Britain, slang, pejorative) *A silly, incompetent, stupid, annoying or childish person (usually a man).*
* The name **git** was given by Linus Torvalds when he wrote the very first version. 
  * He described the tool as *the stupid content tracker*

--

### What does the manpage say?
* "Git" can mean anything, depending on your mood.
  * Random three-letter combination that is pronounceable, and not actually used by any common UNIX command. The fact that it is a mispronounciation of "get" may or may not be relevant.
  * Stupid. contemptible and despicable. simple. Take your pick from the dictionary of slang.
  * "Global information tracker": you are in a good mood, and it actually works for you. Angels sing, and a light suddenly fills the room. 
  * "Goddamn idiotic truckload of sh*t": when it breaks

---

## Hands-on
### Enough of theory

--

### First-time git setup 1/3

* Install git

```bash
zypper in git
```

--

### First-time git setup 2/3

* There are *three layers* where git can be configured:
  * System-wide: `git config --system`
    * Lives in: `/etc/gitconfig`
  * User-specific: `git config --global`
    * Lives in: `~/.gitconfig`
  * Repository-specific: `git config --local`
    * Lives in: `.git/config` of the repository you are using at the moment
* Keep hierarchy in mind: repository overwrites user overwrites system

--

### First-time git setup 3/3
* Set some important config values

```bash
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
$ git config --global core.editor vim
# now try the following commands
$ git config --list
$ git config --global --list
$ git config --system --list
```

--

### git init
```bash
git init
Initialized empty Git repository in /tmp/howtogit/demo/.git/
```

* Initializes a brand new Git repository and begins tracking an existing directory
* It adds a hidden subfolder within the existing directory that houses the internal data structure required for version control

--

### git clone
```bash
git clone https://github.com/TheRealBro/how-to-git.git
Cloning into 'how-to-git'...
remote: Counting objects: 137, done.
remote: Compressing objects: 100% (104/104), done.
remote: Total 137 (delta 31), reused 127 (delta 25), pack-reused 0
Receiving objects: 100% (137/137), 5.68 MiB | 1.24 MiB/s, done.
Resolving deltas: 100% (31/31), done.
```

* Creates a local copy of a project that already exists remotely
* The clone includes all the project’s files, history, and branches
* *Yes, in Germany, fiber equals copper. :/*

--

### git add
```bash
user:/tmp/howtogit/how-to-git> touch demofile.txt
user:/tmp/howtogit/how-to-git> git add demofile.txt
```

* Stages a change
* It’s necessary to stage and take a snapshot of the changes to include them in the project’s history
* This command performs staging, the first part of that two-step process
* Any changes that are staged will become a part of the next snapshot and a part of the project’s history
* Staging and committing separately gives developers complete control over the history of their project without changing how they code and work

--

### git commit 1/2
```bash
git commit
```

* Opens an editor to set a commit message

```bash
# Changes to be committed:
#       new file:   demofile.txt
#
added empty demofile.txt
```

* After editing and saving the commit message this happens

```bash
[master 63522a3] added empty demofile.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 demofile.txt
```

--

### git commit 2/2
* Saves the snapshot to the project history and completes the change-tracking process
* In short, a commit functions like taking a photo. Anything that’s been staged with `git add` will become a part of the snapshot with `git commit`
* What did I do wrong?

--

### git status
```bash
git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   demofile2.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        demofile3.txt
```

* Shows the status of changes as untracked, modified, or staged
* What did I do before i typed: `git status`?

--

### git branch 
```bash
git branch 
* master

git branch -av
* master                            00d313d Merge pull request #2 from TheRealBro/edit-tbro-20180123
  remotes/origin/HEAD               -> origin/master
  remotes/origin/edit-tbro-20180123 c134d5b latest changes 2018-01-23 22.56
  remotes/origin/master             00d313d Merge pull request #2 from TheRealBro/edit-tbro-20180123

git branch foobar
git branch
  foobar
* master
```
* Shows / modifies the branches being worked on

--

### git checkout
* Is used to switch branches in a repository
* `git checkout foobar` would take you to the `foobar` branch whereas 
* `git checkout master` would drop you back into `master`
* Be careful with your staged files and commits when switching between branches

--

### git merge

* Merges lines of development together
* This command is typically used to combine changes made on two distinct branches
* For example, a developer would merge when they want to combine changes from a feature branch into the master branch for deployment

(*Side note: This is where the term **merge request** in GitLab comes from*)

--

### git pull
```bash
git status 
On branch master
Your branch is behind 'origin/master' by 2 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

git pull 
Updating 98b9fa1..00d313d - Fast-forward
 img/howtogit004.png         | Bin 0 -> 139292 bytes
 slides.md                   | 136 (++++++++--- ...)
 2 files changed, 129 insertions(+), 7 deletions(-)
 create mode 100644 img/howtogit004.png
```

* Updates the local line of development with updates from its remote counterpart (if a teammate has made commits to a branch on a remote repository)

(*Side note: This is where the term **pull request** in GitHub comes from*)

--

### git push 

* Updates the remote repository with any commits made locally to a branch
* **Do not push to master!**

![do not push to master](img/howtogit006.png)

---

## Some example workflows

--

### Contribute to an existing repository

```bash
# download a repository on GitHub.com to our machine
git clone https://github.com/me/repo.git
# change into the `repo` directory
cd repo
# create a new branch to store any new changes
git branch my-branch
# switch to that branch (line of development)
git checkout my-branch

# make changes, for example, 
# edit `file1.md` and `file2.md` using the text editor

# stage the changed files
git add file1.md file2.md
# take a snapshot of the staging area (anything that has been added)
git commit -m "my snapshot"
# push changes to github
git push --set-upstream origin my-branch
```

--

### Start a new repository and publish it to GitHub
```bash
# create a new directory
# and initialize it with git-specific functions
git init my-repo
# change into the `my-repo` directory
cd my-repo
# create the first file in the project
touch README.md
# git is not aware of the file, stage it
git add README.md
# take a snapshot of the staging area
git commit -m "add README to initial commit"
# push changes to github
git push --set-upstream origin master
```

--

### Contribute to an existing branch on GitHub
```bash
# assumption: a project called `repo` already exists on the machine
# and a new branch has been pushed to GitHub.com 
# since the last time changes were made locally

# change into the `repo` directory
cd repo
# update all remote tracking branches
# and the currently checked out branch
git pull
# change into the existing branch called `feature-a`
git checkout feature-a

# make changes, for example, 
# edit `file1.md` using the text editor

# stage the changed file
git add file1.md
# take a snapshot of the staging area
git commit -m "edit file1"
# push changes to github
git push
```

---

## GitLab
### Live Demo

---

## Sources & more

--

## Sources 1/3
* https://guides.github.com/introduction/git-handbook/
* https://en.wikipedia.org/wiki/Version_control
* https://en.wikipedia.org/wiki/Distributed_version_control
* https://en.wikipedia.org/wiki/Git
* https://betterexplained.com/articles/a-visual-guide-to-version-control/
* https://betterexplained.com/articles/intro-to-distributed-version-control-illustrated/
* https://github.com/Krten
* http://opensuse.github.io/branding-guidelines/

--

## Sources 2/3
* https://github.com/hakimel/reveal.js
* https://de.wikipedia.org/wiki/Versionsverwaltung
* https://guides.github.com/features/mastering-markdown/
* https://github.com/arslanbilal/git-cheat-sheet
* https://github.com/detailyang/awesome-cheatsheet
* https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf
* https://betterexplained.com/articles/aha-moments-when-learning-git/
* http://nvie.com/posts/a-successful-git-branching-model/

--

## Sources 3/3
* http://a5anka.github.io/images/gitflow_5_Vincent_Driessen.png
* https://en.wiktionary.org/wiki/git
* https://git-scm.com/blog
* https://git-scm.com/book/en/v2
* http://rogerdudler.github.io/git-guide/
* https://www.sitepoint.com/git-for-beginners/
* https://www.youtube.com/playlist?list=PLg7s6cbtAD17Gw5u8644bgKhgRLiJXdX4 (Git & GitHub YouTube short tutorials)
* https://linuxacademy.com/blog/linux/git-terms-explained/
* https://learngitbranching.js.org/
* https://lab.github.com/

--

## Copyright
* Copyright and licenses of the used graphics - as stated in the graphics
* Licenses of the source materials - as stated in the source links
* To this presentation LICENSE file of therepository applies:
  * https://github.com/TheRealBro/how-to-git/blob/master/LICENSE

--

## Thank you for your attention :)
### This presentation can be found here
### https://therealbro.github.io/how-to-git/
### https://github.com/TheRealBro/how-to-git
### https://learngitbranching.js.org/
