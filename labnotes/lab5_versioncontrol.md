# Version Control and Git

## What is Versioning?
- just the idea of having multiple iterations
- 'we're going to write a paper together, and try to keep our work synchronized somehow'
- we are all familiar using google docs, writing on the same page and seeing the revision history, same thing with wkipedia
- in a sense, this creates a series of versions

## Git and Github
- git is a specific type of version control software
- git lets you track revisions and merge and integrate peoples' changes
- github, on the other hand, is a centralized server fto track and maintain your work across versions, using the git program to track versions
- so what is git? a model of version synchronization
- github has some other nicefeatures
	- like a built in wiki tool, if you have many people and want to keep track of what you're ding
	- it has an issue tracker
	- there are some social/wiki tools, it manages your identities through accounts and such

## Git
+ start off with an empty folder - we can call this your project
+ when you run `git init` on your folder in the command line, git starts tracking what goes on in the folder.
+ imagine that git is like a little friendly presence keeping track of your folder
+ say you've added some pictures and mp3s to your folder, you have a bunch of stuff
+ now you can say 'let's look at the paper, the images, and the mp3, but not some etc notes in this folder' by writing `git add [file1] [fil2] [etc]`
+ once you've added these things, you can commit them as a specific version by saying `git commit`
+ the next day, so you write some more of the paper, find another picture, repackage your notes and the new stuff, and you can stage+commit those things
+ staging is like adding
+ google docs does this for _any_ change you make in your document, just blindly committing things to your ledger. with git, you are in charge of the stage and commit steps

## Enter Github
+ So you are working happily making versions and saving your progress
+ Out in the cloud lives a server of github
+ You can do a `git push` to synchronize your versions to the cloud, and push them to your github
+ Now you have a ledger on your local machine, and a cloud representation of the same things, code, shakespeare research, etc
+ Let's say Max wants to join in on your paper. Max can call `git clone [ourpaper]` and get the folder with the paper from github, with the ledger we created, and pull the directory and all its contents and the history onto your computer
+ now you are both working on a common project with a common timeline and history, a common ledger of our work
+ in git lingo, the last thing you have done, the 'today I did', this is called the **HEAD**. 
+ If you have three versions pushed to your timeline, and Max came to clone it, then he got the paper as it stands. If Max cloned your work and then added some information, changed files, made new versions, etc. then he "advanced the head". This is because hemoved the timeline ahead.
+ Now Max can push his new version to github, and your head might be out of date, behind his. When you sit down to work, your version will be behind, and then you add all these things not knowing about Max's changes. When you push your new changes, git says "No!!"
	- git says "someone has advanced the head!" you have diverging drafts, your branches of the timeline have diverged.
	- git will tell you to "pull before pushing", meaning acquire his changes before pushing your edits to the timeline
	- if you're lucky, the 'peer produciton low cost of integratino' will manifest in both of you working on different sections and git will be able to integrate everything seamlessly. if you're unlucky, you might need to manually pick and choosewhat to add and keep.

## Why would you use this instead of Google Docs?
+ Real-time viewing of other people's changes seems much more seamless than pulling and pushing and all that
+ Google Docs is 'synchronous' editing, where everyone is writing on the same sheet at the same time
+ Github is 'asynchronous', where we aren't bothering each other, and then we can bring it together
+ With code, when you need to test all your changes before you add it to the final project, this system works perfectly
+ Because Github is very project-based, it will work much better for folders of documents, etc.