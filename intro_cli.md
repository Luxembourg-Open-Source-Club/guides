## A Short Introduction to CLI

Command Line Inteface, CLI for short, is an application that allows users to interact with their OS
using only text, and for that matter only keyboard. If you have never heard of the term CLI, it is the same as a terminal
which I believe is the more general name.

At this point you might be asking: "Why do people use CLI, this is so ugly!". Well,
the answer is pretty simple, it's fast and reliable. Therefore, instead of you going through the file explorer
finding files, or find applications to run, that process can be done more efficiently and way faster
using CLI, all through only using a keyboard. As an example, if you use VS Code as your text editor, and it is installed
(if you are using WSL and you have VS Code on your Windows it should also work), try typing `code` on the
terminal. Yep, that's right, you just opened VS Code.

So to finish the answer, once you get used to the CLI, you will not want to leave from CLI 😅, saying
this from my own experience.

Now be aware that CLI, or bash which is the linux SHELL/terminal has a very large amount of commands to
cover. Nevetheless, this guide aims at introducing you the common used commands.

## Some Basic Bash Commands

As we are interacting with our OS through a CLI interface, we need a tool for that. That software is called **Bash**. It is what we use to navigate the terminal.

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

## Useful Tools

Bash also has a good variety of small tools that let you do a lot of things.
Let's start with a very simple tool, `echo`. You can think of echo as a print function
of any programming language.

For instance, type `echo "Hello world"` in ther terminal. It will print you back _Hello World_.
Why would this be useful you may ask. Imagine you want to create file and want to
add to the file "Hello World". You could use the `>` operator which will place text
inside a file. For example:

```bash
touch hello.txt
echo "Hello World" > hello.txt
```

Now you can use another tool to check the contents of the file. This is `cat`.

```bash
cat hello.text
# Expected Ouput: Hello World
```

So with cat you can check very fast what a file contains inside. There is also a tool very similar
to `cat` which is `less`. Essentially will simplify the text output comparated to `cat`.

You also have the operator `|`, known as the pipe. With it, you can combine to tools,
and send the output of one, to the input of the other. For exmample,

```bash
cat hello.txt | grep "world"
```

You should have world highlighted.

In the example from above, we have used first the command `cat` to give us the content
of the file `hello.txt` and then "piped" the ouput to another program, `grep`.
Grep is a very powerfull tool. It allows you to search for words, substrings, etc in a file,
or in this case the ouput of cat.

With these 3 tools, we believe that you should have on your hands some great power.
In case you want to check more programs available, here's a§[cheat sheet](https://hpc.ua.edu/wp-content/uploads/2022/02/Linux_bash_cheat_sheet.pdf)
