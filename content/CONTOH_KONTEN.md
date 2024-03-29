---
title: "TES KONTEN"
date: 2017-10-26
author: "Jake VanCampen"
comments: true
---
When I began working on the computer full time earlier this year, I was still using the GUIs of my computer and had little intuition for how to organize my work in a coding Environment. Now I use exclusively the command line to navigate my MacBook Pro; collaborate and track my work using Github; and I write most assignments, and now blog posts in markdown.


The largest behavioral change for me was working primarily in text editors, Github, and the command line. After lots of practice I prefer these environments. It has taken a good deal of time and research to find the tools, and personal settings necessary to keep my workflow going efficiently on the computer. Here I will discuss the tools and tricks I use, basically a list of personal settings that is likely to change in the next week, but will provide a snapshot for others and myself of where I am at currently.


## iTerm

I use a terminal emulator called [iTerm](https://www.iterm2.com/documentation-one-page.html) that is highly functional and customizable. I have used it for a while, and it's unlikely I will use anything else anytime soon. It features text selection, split panes, and a hotkey window (love this). There are also options for profiles and nice tab-switching functionality.


## Setting up Bash preferences

One of the first settings I changed when I started working on the command line is to customize the prompt it's self. The settings that determine this are found in the hidden file: `.bash_profile` in your directory. If you are not familiar with these hidden files, to find them on an OSX terminal or UNIX environment you can type `ls -a` on the command line to list all files. These hidden files can be edited using your favorite text editor. After some experimenting this is the prompt I like the most:

```bash
JVC [08:44:28] (Users)
→
```

This kind of customization can be done by editing the `PS1` environment variable in your `.bash_profile` so that every time you open a new shell, you customized prompt will appear instead of the canonical `$`. My prompt for example was written by adding the following line to my `.bash_profile` file.

```bash
export PS1="\e[38;5;45mJVC \e[38;5;208m[\T] \e[38;5;13m(\W)\e[m \n→"
```

Another sweet hack that can be customized via editing `.bash_profile` are aliases. Aliasing allows you to essentially create your own typed shortcuts for common tasks that you would type on the command line.

The two I find very helpful are:

```bash
# jupyter notebook shortcut
alias jn="jupyter notebook"
#always show filetype
alias ls="ls -F"
```


The `ls -F` alias is very useful to quickly discern directories, symbolic links, and executables while navigating my computer from the command line.

## .inputrc

Another incredible hack that I learned from a bioinformatics mentor is a set of tools for streamlining command line input. Essentially they are a list of settings that can be added to a `.inputrc` file, if it doesn't exist you can just create one:

```bash
touch ~/.inputrc
```

These setting originally came from this talk on [Power Shell Usage: bash tips and tricks](http://www.ukuug.org/events/linux2003/papers/bash_tips/). There are a number of tricks found on that page, I only have some. Here is a summary:


**Partial Command Completion**
Type partial command, then hit arrow-UP or arrow-DOWN multiple times.
This limits the searching of your history to just history items
prefixed with your partial commands. This one is listed first for a reason!

```
"\e[A": history-search-backward
"\e[B": history-search-forward
```

**Case Insensitive Completion**
Ignore case during tab completion.
If you're trying to tab complete on, say, DOWNLOADS, then you can
type 'dow' and then TAB, and it will tab complete to DOWNLOADS.
```
set completion-ignore-case on
```


**Magic Space**
This allows you to quickly check that your shortcut will not make your wolrd implode. A shortcut to access the last command in bash/UNIX is `!$`. With magic-space you can type `!$` then type space, and it will auto-fill your last command.

```
$if Bash
  Space: magic-space
$endif
```

**Tab=Possible Completions**
This allows for tab completion to show all possible completions if there are more than one possibility. This can be useful for navigating file systems very quickly if you sort-of know what is there.

```
set show-all-if-ambiguous on
```

## Git Settings

Github necessitates many commands that need to be typed repetitively. I got lazy very early and added the following aliases to my .gitconfig file.

```
[alias]
	co = checkout
	br = branch
	st = status
	cm = commit -m
```


These aliases definitely increased my productivity when working in Git, and made it easier to lean more complex features of Git, because I could complete simple tasks faster. Theses can also by added by


## Text editors

**SublimeText3**

I used SublimeText3 for about six months. I was able to quickly edit and write code because of the very clear syntax highlighting that the editor provides. SublimeText3 also support the use of a code linter for Python called flake8, which is really helpful for writing cleaner Python code. I started using this code linter because of a Pythonista I follow by the name of Dan Bader. I certainly recommend looking at his [blog](https://dbader.org/) and very excellent [youtube videos](https://www.youtube.com/channel/UCI0vQvr9aFn27yR6Ej6n5UA/videos).

**Atom**

Atom is another excellent text editor that is feature-packed and fully hackable. Atom features seamless git integration, markdown preview, text and code completion, syntax highlighting, and supports the Python code linter style I used in SublimeText3. I recently discovered Atom from another developer and reproducible data scientist, [Zach Sailer](https://github.com/Zsailer), and have fully migrated.


## Interpreters

**Jupyter Notebook**

The Jupyter notebook is a server-hosted interpreter that supports many languages, but was designed with Python specifically in mind. The Jupyter project aims to improve the future of reproducible data science, and has done an excellent job thus far; many publications now have data on Jupyter notebooks that can be run by anyone. Jupyter, or ipython notebooks are very useful for developing in Python providing an inline interpreting and graphing. I use jupyter notebooks when writing code for Data Visualization in Python.

**Rstudio**

Rstudio has been essential for me to learn R. There are many tools built into Rstudio, and getting to know each one has overall helped me learn the ins and outs of R very well. Rstudio allows you to have 'projects' that are kind of a copy of your working environment for a specific project in a directory. Then there are the Rmarkdown documents that render chunks of R code into a markdown file with your writing inline using a tool called `knitr`. They can be knit into html, or pdf format and provide a method for making very clean looking data analysis reports.

## The End

These tools have increased my productivity and ability to learn new concepts in bioinformatics and data science more efficiently. Because technology changes rapidly, I am excited to look back on this snapshot a year from now to see how my preference for these tricks has changed and certainly add some new ones!
