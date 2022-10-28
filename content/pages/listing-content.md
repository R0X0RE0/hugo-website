---
title: "Listing Content"
author: "RoxNoAnne"
date: 2022-10-26T20:35:38-04:00
description: "There are many different ways to list content in Linux. This article will talk about 4 different ways you can list content in a directory on Linux."
draft: false
---
# What are the possible ways of listing content in Linux?
You can look for files in a directory in the terminal. There a few ways to execute this, and they're convenient.

### Solution A. The `ls` command
With the `ls` command, the text is color coded and you can use arguments to modify the output and how it looks. Personally, if I need details, I use `ls -hal` to list contents in the directory.

### Solution B. `echo *`
This isn't really recommended, because it's more barebones than anything, and you can't modify how the output looks really. The `*` wildcard is being used to look for everything that's in the directory.

### Solution C. `printf "$(<command>)"`
You can replace `<command>` with the two commands from the two solutions above.  

The output of `printf "$(ls)"` is...
```sh
roxnoanne@debian:~/Documents/projects/hugo/quickstart$ printf "$(ls)\n"
archetypes
config.toml
content
data
layouts
public
resources
static
themes
```

The output of `printf "$(echo *)"` is about the same, but the command is longer.

### Solution D. Tab Completion
Take a command that involves directories and/or files, such as `mv`, `cp`, `rm`, `mkdir`, `nano/vi`, and `cd`. `mv` is used to move and rename files and directories, `cp` is used to copy files and directories, `rm` is used to remove files and directories, `mkdir` is used to create directories, `nano` is the easier text editor to use in the terminal, `vi/vim` is a modal text editor with a steep learning curve, and `cd` is used to access different directories. If you press tab on these commands, the console will give an output listing the possible files and directories you can access.
