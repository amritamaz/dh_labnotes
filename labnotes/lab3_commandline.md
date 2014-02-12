# Week 4 Lab - Command Line Basics

    
## Level 1

+ `pwd`  - present working directory - where am I?
+ `cd ______` - change directory - mvoe into a new folder
+ `ls` - list all the files in the directory/folder I am currently in
+ `cd ..` - go up a directory
+ `cd -` - jump to the last directory you were in
+ `pushd ________`, `popd _________`
	- create a stack of directories and push and pop paths off the stack to navigate quickly through directories
	
## Your Best Friends
+ `man [any command]` learn more about pwd, cd, ls, and more!
	- man stands for _manual_
	- read the manual pages and navigate using the spacbar, arrow keys, and q to quit
+ `clear` - clear your terminal
	
## Level 2
+ `touch ______` - create a file
+ `mkdir ______` - make a directory
+  `rm ____` - delete a file or directory
	+ to delete a folder, use `rmdir ___` or `rm -r ___`
	+ the `-xx` word after rm is a **flag**. flags can be used with any command, use the man pages to see what flags are out there!
	+ to use multiple flags, pair them together with one flag or multiple:
	
			rm -r -v myfile
			rm -rv myfile
+ `cp [myfile] [newfilename]` - copy a file from one name to another
	+ alternatively, you can copy a file directly into a new directory:
		+ `cp [file] [otherdirectory]` - with the same name
		+ `cp [file] [otherdir/newname.ext]` - with a new name
+ `mv [file1] [newdir or new filename]` - this is a rename or move command. 
	+ `mv [file] ../[some directory above it]` - copy or move one directory up

## Level 3
+ `history` - give you a history of what you've done
	- alternatively, you can use the up and down arrow keys in a blank bash prompt to see your past commands
+ **BONUS** - `CTRL+R [some past command]` - tries to match past commands from your history
+ history is really long. rather than scrolling, it would be more optimal to paginate the list. to do this, we use pipes `|` to pipe it into a paginating command
+ `history | less` pipes your history into a paginating command, where you can just scroll and stuff. press `q` to quit.
+ Editing files! We use a program called **nano**.
	+ To open a file in nano (new or otherwise) `nano [filename]`
	+ write in the file!
	+ press `CTRL+O` to save
	+ press `CTRL+X` to exit
+ `cat [somefile]` - output files into the command line terminal without having to open them in nano or anything
+ **BONUS: learning to ~~grep~~** 
	- `grep` is like search for the shell
	- `history | grep [some phrase]` - search your history for a specific phrase
	- you can use grep for anything - full text search, anything
	- grep is an advanced tool, can grow with you a lot

## Our Homework
+ learn to use the `find` command
+ much more complicated than grep or anything else, but is the equivalent of Spotlight or something on Mac
+ grep + find is like, advanced bash commands