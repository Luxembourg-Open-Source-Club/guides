# An Introduction to Git

**Git** is a _Distributed Version Control System_ (DVCS) which can be used to
keep track of different versions of files, by using a concept of **Snapshots**.
Different from other VCS (Version Control System) tools, Git saves everything **locally**
on each computer a repository has been cloned.
Therefore, Git can be used offline without the need of requesting a server for updates.

Some of the main differences of Git when compared to other tools, are the following:

- Speed
- Simple design
- Strong support for non-linear development (thousands of parallel branches)
- Fully distributed
- Able to handle large projects like the Linux kernel efficiently (speed and data size)

## Installation

For most linux based systems, it is likely you already have Git installed on your system.
You can check if it is installed if you type `git` in the terminal. In case you get
an error this command does not exist, then likely you will need to install.
In case you are using a Debian based OS, then you just just use `sudo apt install git`.

> For MacOs, you should already have it installed by default!

For Windows, you will need to manually install it. You will need to go to [Git](https://git-scm.com/) website.

## Git & GitHub

While you might think that **Git** and **GitHub** are the same thing, they are not.
Git is the DVCS, which runs locally on any computer. On the other hand, GitHub it
is merely a web app, which gives a set of tools to facilitate the Git workflow, and
more importantly, it serves as a cloud storage to store all your Git repositories.

## Git States

When working with Git, you need to be aware that it has some states. This is a way of letting Git
now the current status of your repository, repo for short, like if you have modified a file.
We can distinguish 4 different states:

- **Untracked**: This state indicates that Git is not aware that a file exists. This happens
  when a new file has been created.

- **Modified**: This state indicates that one of the files that git is currently tracking has been modified.

- **Staged**: This state indicates that modified files have been marked to be added to the
  next commit snapshot.

- **Committed**: This state indicates that the staged files are permanently stored in the
  Git worktree.

## Configuring Git

When using Git for the first time, you will need to configure it. To start using it however, only 2 changes
must be made. These are you name and email. To configure, you can type the 2 commands from below
on the terminal. To verify the changes have been made, you can type the command before the actual information.

```sh
git config --global user.name "John Doe"
git config --global user.email "johndoe@example.com"
```

## A Git Workflow

There are many workflows possible. Nevertheless, the next is the most common one:

1. Modify/Add a file in your repository
1. You selectively stage just those changes you want to be part of your next commit,
   which adds only those changes to the staging area.
1. You do a commit, which takes the files as they are in the staging area and
   stores that snapshot permanently to your Git directory.

## Git Commands

There exists a lot of commands for Git, which you can check by using `git --help`. For that reason,
this guide will only show the most commont commands, and these are also the commands that are
required to perform the [Git Workflow](#a-git-workflow) from above.

### Initiate a Git Repository

To initiate a new Git repo, you will need to first create a folder for the same. Once inside, you
can then use the command from below to initiate a Git repo inside the folder.

```sh
git init
```

### View Repository Status

Whenever you have a Git repo, you can check its status (the states). You can now
what files are modified, untracked etc.

```sh
git status
```

### Stage Files

In order to stage the files you have modified/added, you can use the command from below.
Take in mind, that if you use `git add .`, it will add every file that has been modified.
However, that is not a good practice as it might be difficult to track what was the change
performed. In addition, you could add dotfiles that are not useful to keep track.

```sh
git add <name_of_file/path_to_file>
```

### Commit Staged Files

After you have stated files, you should then perform a commit. As said previously, when you
commit, you are permanently telling git to store the changes. Commits are an important
step, as it will let you, and others, see what has been changed in that commit.
Therefore, it is good practice to write a clear and consie message of what was the change.

```sh
git commit -m "You message"
```

You can also use the command `git commit` which will open a text editor to write the commit.
If you do this, you can first write the consise message (Try to stay under 60 characters), and if you enter a new line, this will
be consider as the detailed description. For instance:

```md
This is the title

After this line, any text will be consider as the main message body, the detailed description.
```

### Commands for remote repos (GitHub)

Whenever you want to have the remote repository that leaves on GitHub, you can **clone**
the repo to you computer. When you are in a GitHub repo (on the web), you can get the
URL from the button named _code_. Then use the command:

```sh
git clone <url>
```

Once you have commited the changes locally and you want to place them on the cloud,
you can **push** you changes using the command:

```sh
git push
```

Finally, if you want to retrieve new changes from the cloud, for example some collaborators
have changed something, you can then **pull** the changes using the command:

```sh
git pull
```

### Logging

You can get a list of all the commits done by using the command

```sh
git log
# or
git log --graph # to see a grah
```

### Creating/switching Branches

TODO: Missing Explanation of branches

```sh
git checkout -b <branch_name>
```

```sh
git checkout <branch_name>
```

```sh
git branch
```
