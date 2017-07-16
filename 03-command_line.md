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

> > 
* clear - clear command window
* ls - list files
* ls -a - list files include hidden
* pwd - present working directory
* cd - change directory
* cd .. - move up one directory
* mkdir *foldername* - create a directory
* touch *filename* - create a file in working directory
* cp frida.txt lincoln.txt - copies frida.txt to lincoln.txt
* mv superman.txt superhero/ - move the superman.txt to superhero directory
* rm waterboy.txt - remove waterboy.txt
* rm -r comedy - will remove the comedy folder
* grep Mount mountains.txt - searches for 'Mount' in mountains.txt
* grep -i - makes grep search without case sensitivity
* grep -R Arctic /home/ccuser/workspace/geography - returns all files in the dir with 'Arctic'

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls` list files  
`ls -a`  list files include hidden  
`ls -l`  list files in long name  
`ls -lh` print file sizes in  human readable  
`ls -lah` hidden files, long name, file size in human readable   
`ls -t` order files and directories by the time they were last modified    
`ls -Glp` long format, shows which are directories '/' and colored  

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > 
* ls -lh
* ls -Glp
* ls -Glpth: show file folders, long name, human-readable, newest file first
* ls -R : show subdirectories
* ls -1 : each entry on a new line

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> >
Source: https://www.computerhope.com/unix/xargs.htm
This reads items from the standard input, delimited by blanks or newlines, and executes the command (the default command is echo, located at /bin/echo) one or more times with any initial-arguments followed by items read from standard input. 

Example from source:
find /tmp -name core -type f -print | xargs /bin/rm -f
Find files named *core* in or below the directory /tmp and delete them. Note that this will work incorrectly if there are any filenames containing newlines or spaces.

 

