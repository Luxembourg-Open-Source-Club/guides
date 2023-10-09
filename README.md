# LOSC Guides

If you are new, this guide will help you set up your computer so that you can
contribute and learn more about contributing using both **Git** and **GitHub**.

In our experience, most of you will be running Windows 10/11 as your main Operating System (OS).
However, we prefer to use a Linux based OS, as it makes solving/detecting problems related
to OS easier to find (If you already use macOS or a Linux distribution, skip to [Updating System](#updating-system).
In addition, if we pass a command, the same should then work for everyone.
This said, in case you are using Windows you have 2 possible solutions. The first
is to set up a Virtual Machine (VM), where you will need to install a Linux distrubution.
We advice you to use a debian based like [Ubuntu 22.04](https://ubuntu.com/). The second option, and
the easiest one, is to use [WSL](https://learn.microsoft.com/en-us/windows/wsl/install) (Windows Subsystem for Linux).
Please follow the instructions under [For Windows Users](#for-windows-users).

## For Windows Users

### Setting up a Virtual Machine

Before you consider this alternative, you should be aware that in terms of performance,
it's not the best, as you will be running 2 OS on the same hardware. Thus, you will have
a weaker computer.

Here's is a [tutorial](https://www.youtube.com/watch?v=v1JVqd8M3Yc) that you can follow to set up a VM using Virtual Box.

### Installing WSL

This is very simple. You will need to open Powershell as an **administrator** and then
enter this command: `wsl --install`. For more information, you can find it [here](https://learn.microsoft.com/en-us/windows/wsl/install)

After installation, you can just search for Ubuntu using Windows search tool. We recommend pinning this to your taskbar for easy access to your Linux terminal.

## Updating System

> From this point forward, we assume you are using a Linux based OS (macOS included).

It is always nice to keep your system up to date. Therefore, even if you are a Linux user for a while,
you can and should use the following command:

```sh
sudo apt update && sudo apt upgrade -y
```

In this one line, we can distinguish 2 different commands which are separated by `&&`. Let's go through both commands.

`sudo` is a program that takes another program and
runs it with **root** priviledges (same as administrator in Windows). `apt` is another
program (Advanced Packaging Tool) which in other words is a **package manager**. `update` & `upgrade` are
2 possible flags of the program `apt`. **Update** means that you fetch any new changes
to programs you have installed. You may think that it will install updates, but no, it just lets
the OS know that there has been changes. **Upgrade**; however, based on the fetched
information will now install all updates. The additional flag `-y` just means that you accecpt
everything by default to be upgraded.

All updates on your computer are done like this: applications, libraries, operating system updates, etc. **Centralized** is the key word ;)

## Installing Git

In some Linux distributions, Git does not come installed by default. Thus, we will
need to install it. But don't worry, it's very simple! You just need to type the following
command:

```sh
sudo apt install git
```

Notice that if you need to install other programs, you will use the same command but changing
`git` with the desired program name.

## A Beginner CLI Guide

[Beginner CLI Guide](./intro_cli.md)

## A Beginner Git Guide

[Beginner Git Guide](./intro_git.md)
