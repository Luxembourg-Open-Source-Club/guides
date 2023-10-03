# LOSC Guides

If you are new, this guide will help you set up your computer so that you can
contribute and learn more about contributing using both **Git** and **GitHub**.

In our experience, most of you will be running Windows 10/11 as your main Operating System (OS).
However, we prefer to use a linux based OS, as it makes solving/detecting problems related
to OS easier to find (If you already use MacOs or a Linux distribution, skip to [Updating System](#updating-system).
In addition, if we pass a command, the same should then work for everyone.
This said, in case you are using Windows you have 2 possible solutions. The first
is to set up a Virtual Machine (VM), where you will need to install a Linux distrubution.
We advice you to use a debian based like [Ubuntu 22.04](https://ubuntu.com/). The second option, and
the easiest one, is to use [WSL](https://learn.microsoft.com/en-us/windows/wsl/install) (Windows Subsystem for Linux).
Please follow the instructions under [For Windows Users](#for-windows-users).

## For Windows Users

### Setting up a Virtual Machine

Before you consider this alternative, you should be aware that in terms of performance,
its not the best, as you will be running 2 OS on the same hardware. Thus, you will have
a weaker computer.

Here's is a [tutorial](https://www.youtube.com/watch?v=v1JVqd8M3Yc) that you can follow to set up a VM using Virtual Box.

### Installing WSL

This is very simple. You will need to open powershell as an administrator and then
enter this command: `wsl --install`. For more information, you can find it [here](https://learn.microsoft.com/en-us/windows/wsl/install)

After installation, you can just search for Ubuntu using Windows search tool.

## Updating System

> From this point forward, we assume you are using a Linux based OS (MacOS included).

It is always nice to keep your system up to date. Therefore, even if you are a Linux user for a while,
you can and should use the following command:

```sh
sudo apt update && sudo apt upgrade -y
```

In this one line, we can distinguis 2 different commands which are separated by `&&`.
Let's go through both commands. `sudo` is a program that takes another program and
run's it with root priviledges (same as administrator in Windows). `apt` is another
program (Advanced Packaging Tool) which in other words is a package manager. `update` & `upgrade` are
2 possible flags of the program `apt`. **Update** means that you fetch any new changes
to programs you have installed. You may think that it will install updates, but no, it just lets
the OS know that there has been changes. **Upgrade** however, this will based on the fetched
information now install all updates. The additional flag `-y` just means that you accecpt
everything by default to be upgraded.

## Installing Git

In some Linux distributions, Git does not come installed by default. Thus, we will
need to install it. But don't worry, it's very simple! You just need to type the following
command:

```sh
sudo apt install git
```

Notice that if you need to install other programs, you will use the same command but changing
`git` with the desired program name.

## Why Use CLI?

> CLI = Command Line Interface also known as terminal

At this point you might be asking, "why do people use CLI, this is so ugly!". Well,
the answer is pretty simple, its fast. Therefore, instead of you so through the file explorer
finding files, or find applications to run, that process can be done more efficiently and way faster
using CLI. As an example, if you use VS Code as you text editor, and it is installed
(if you are using WSL and you have VS Code on your Windows it should also work), try typing `code` on the
terminal. Yep, that's right, you just opened VS Code.

So to finish the answer, once you get used to the CLI, you will not want to leave from CLI 😅, saying
this from my own experience.

## Some Basic CLI Commands

To get you started, we will be leaving here some of the most common commands:

1. `sudo`: Give you root privileges (Be careful when using this command, it is too powerful)
1. `cd <path>`: Change Directory. This is the way you can move around. If you use `cd ./<folder/path>`
   you will be moving from where you are to this folder. You can also use `cd ../` to go backwards. Or lastly,
   you can simply use full paths, such as `cd /home/`.
1. `ls`: List directory, shows all files and folder from the current directory. Additionally, you can
   also use a path similar to `cd`
1. `mkdir <name>`: Creates a new directory with a name \<name>. Additionally, you can
   also create a directory using a path. For instance, `mkdir /home/hello_world` which creates
   a directory _hello_world_ inside `/home`.
1. `touch <name>`: Create a file with a name \<name>. Note that you need to also include the extension.
   For example, if you want to create a text file, it could look like this: `touch test.txt`
1. `pwd`: Print Workding Directory. Essentially, prints out the full path to where you are.
1. `rm <file>`: As the name suggests, you can remove/delete a file. (**Once removed, there is no way to retrieve it!!**). You can also remove
   directories using `rm -r <dir name>`
1. `mv <file/folder>`: Move a file/folder from one place to another. You can also use this to rename.

For a more details and more commands, check out this [link](https://www.educative.io/blog/bash-shell-command-cheat-sheet).

## Configuring Git

Whenever you have a fresh installation of your OS of choice, you will need to configure Git, respectively name and email.
To do so, you can use the following commands:

```sh
git config --global user.name "Your Name"
git config --global user.email "Your Email" # Here you should try to use the same email as in your GitHub account
```

You can additionally set up your preferred editor using `git config --global core.editor <your editor>` (use code for VS Code)
