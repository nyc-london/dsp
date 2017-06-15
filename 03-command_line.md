# Learn command line

Please follow and complete the free online [Command Line Crash Course
tutorial](https://web.archive.org/web/20160708171659/http://cli.learncodethehardway.org/book/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. Each "chapter" focuses on a command. Type the commands you see in the _Do This_ section, and read the _You Learned This_ section. Move on to the next chapter. You should be able to go through these in a couple of hours.

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > REPLACE THIS TEXT WITH YOUR RESPONSE

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a` 
`ls -l` 
`ls -lh` 
`ls -lah` 
`ls -t` 
`ls -Glp`  

> > 

`ls` = list directory contents 
`ls -a` = lists all files including hidden files 
`ls -l` = uses a long listing format
`ls -lh` = long listing format with file size in human readable form
`ls -lah` = long listing format with file size in human readable form (including hidden files)
`ls -t` = sort by modification time, newest first
`ls -Glp` =  uses a long listing format (with no group names)

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > REPLACE THIS TEXT WITH YOUR RESPONSE

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > xargs means "combine arguments."  xargs builds and executes command lines by gathering together arguments it reads on the standard input.

xargs grep typedef < file-list
(1) This command searches for the files listed in the file 'file-list'; and
(2) prints all of the lines in them that contain the word 'typedef'

 

