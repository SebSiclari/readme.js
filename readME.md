# Demo

Writing something random !


# Subheader 

Just working on the Youtube turotila to understand Git 



GIT STATUS- the git status command shows you all of the files that were updated or deleted or created but have not been saved in a commit yet.

GIT ADD .- so you might see that there are some untracked files when you run the git status command, and that is because thye have not been committed yet or the changes have not been saved yet there fore that is what Git Add is for.  
SO what GIT ADD really does is it gets ready those files for them to be committed.


git add filename- you can also add by name rather than by dot (which adds all of the files that were uncommitted or not ready to be committed.)

git commit-we commit or save the changes made to the files we were playing with

git push- so although the changes were made the chnages and most uodated verison of the files are not live on Github and we make it live by using the push command which means I want to push klive to a remote reposiotry where my project is hosted. 



SSH Key- we generated a key 
testkey.pub is the key that you are going to upload in your github interface
pub stands for public 
testkey on private key 


origin- just stands for the location of the Git repository



git clone- cloning a repository creates an exact copy of all files and chnages in a git repository at the time of the clone. 
cloning a remote creates a local verison of that repository on your machine.  
Giving you the opportunity to experiment on the project withotu affecting the original code base
Cloning alos establishes a connection between the local repository on your mahcine and the remote repository on Github 
this allows push and pull actions 
with the remote project 


Aliases
Are custom shortcuts that define which command will expand ot longer or combined commands. 
ALiases save you the time and energy cost of typing frequently used commands. 
Git provides its own alias system.
A common use for Git aliases is shortening the commit command. 

so if you move to a different repository then the laias will go back to its original status aka st goes abck to status 

REMEBER THAT COMMMITTING IS THE EQUIVALENT TO SAVING 
Git committing is an operation that acts upon a collection of files and directories 
Git commits can be captruebd and buil up locally, then pushed to a remote serve on Github as needed using the git push -u origin 


GIT ADD
it adds changes and command in the working directory to staging area. 
It tells Git that you want to include updates to a particular file. 
Changes are not actually recorded until you run gitcommit. 
gitreset command is used to undo a commit or staged snapshot. 
In addition to git add and git commit, a third command gitpush is essential for a complete collaborative Git workflow. 

THE STAGING AREA
The primary function of the git add command, is to promote pending changes in the working directory, to the git staging area.
The staging area is one of Git's more unique features, 



GIT DIFF 
Diffing is a function that takes two inputs of data sets and outputs the chnages between them.
git diff is a multi-use Git command that when executed runs a diff function on Git data sources. 
These data sources can be commits branches, files and more. 
$:> echo "this is a diff example" > diff_test.txt :
executing this command will chnage the content of the difff_test. txt file  


GIT STASH(STASHING)
The git stash command takes your uncommitted chnages 
saves them away fro later use and then reverts them from your working copy 
You can reapply previously stashed chnages with git stash pop
Git stash will not stash files that have been ignroed 
Git stash will not stash new files in your working copy that have not yet been staged.
You are not limited to a single stash 
You can run stash several times to create multiple stashes 
By default stashes are dienitfied as a wokr in progress 
You can view a summary of a stash with git stash show

Creating a  branch form yout stash 
If the chnages on your branch diverge from the chnages in your stash;
you may run into conflicts when popping or applying your stash. 
Instead you can use git stash branch to create a new branch to apply stashed chnages to



.gitignore
Git sees every file in your wokring copy as one of three things:
tracked - a file which has been previously staged or committed 
untracked - a file which has not been staged or committed
ignored - a file which Git has been explicitly told to ignore. 

Ignored files are usually build artifacts and manchin generated files that can be derived from your repository source or should otherwise not be committed,


git ingonre command tells git to pretty much ignore the file 
or better pretend like it never existed 
You might want to ignroe files for example a file that is not necessary that is not needed to run your application 


Ignoring a previously committed file. 
If you want to ignore a file that you have commited 
in the past, you'll need to delete the file form your rpeository and then add a .gitignore rule for it. 
Using the --cached option with git rm means that the file will be deleted from your repository  



INSPECTING A REPOSITORY 
git status-
The git status command displays the state of the wokring direcotry and the staging area 


Usage 
git status to list whihc files are tracked or untracked 
Git status command i srealtively straightforward command. 
It ismply shows you what's been going on with git add and git commit. 

It is good to check the state of your repository before committing changes so that you do not accidentally commit something you do not mean to. 


git Log
The git Log command displays committed snapshots. It lets you list the project history, filter it, and search for specific chnages. 

WHile git status lets you inspect the working directory and the staging area. git log only operates on the committed history. 

Log output can be customized in several ways, from simply filtering commits to displaying them ina completely user-defined format. 

git add *.html will add only the files which have a .html extension

.gitignore- we can tell git which files ot exclude by creating a .gitignore file which we will use to specify files and file patterns for git to ignore. 

 Branching
 Vraninching is something almost all control systems have. It allows you to work on a cpoy of the code in the main line wihtout affecting hte main line directly. 
 You would create a new branch if you're working on a bugfix or new feature. 
 When you are done you would merge all of your chnages abck into the main line.  
to switch to master branch we do this git checkout master
maste ris always the master branch 
SO if you make chnaes ina ne wbranch those changes will nto appear on the master branche so what you want to do is merge them so it appears on the master branch 



STASH 
lets say you've been working on a branch and you are not ready to commit them yet but you need to swithc to another branch to do a quick bugfix or work on osmething else
so what the stash command does is take that dirty state of your branch including tracked modifications and staged chnages and saves it on a stack of unfinished changes that can be reapplied at any time. 
when you re ready to come back and continue working on this branch you can reapply your chnages from the stash using git stash apply.
Now you are ready to continue on. 


Even though you are interacting with the rmeote repository eveyrhting is still happening locally you have to manually retrieve and push chnages to the remote repository. 
We can see a list of existing remote repositories we have using git remote 

CLONING A REPOSITORY 
It pulls down the entire rpeository including the entire commit history and as such, git pouts everything in its own folder 

At some point we need to keep it up-to-date and there are two ways of doing that by fetching and by pulling. 
Git fetch origin- will go out to the server and get any chnages made since you last cloned or fetched, fetching will pull the data into your local repository but will not merge it into your work you will need to merge manually.
Git pull origin-will automatically fetch and merge the changes from the remote branch into your current branch 



Tagging and Git Tag
Tagging is generally used to capture a point in history that is used for a marked version release.
In other words when you want to create a release point for a stable version of your code. 
Or when you want to create a historic point for your code/data that you can refer at any future
A tag is like a branch that does not chnage. 
To create a new tag execute the following comman:
git tag tagname
Two types of tags
Annotated tags and ligthweight tags. 
Annotated tags are stored as full objects in the Git database. 
To reiterate, they store extra meta data such as: the tagger name, email, and date. 
Annotated tags are viewved as better than annotated tags so you can have all fo the associated meta-data.
They are sotred as a completete git object 
to create one- git tag -a v1.1 -m "some description"

lightwieight tags- git tag v1.4-lw 

Git Blame
The git blame command is a versatile torubleshooting utility that has extensive usage options. 
This is used to examine specific points of afile's history and get ocntext as to who the last author was that mdofifed the line. 
It is used to explore the history of specific code and answer questions about what, how, and why the code was added to a repository. 
The state of the example repository can be explored using the git log. 
git blamse only operates on individula files. 
It is a common open source software practice to include a README file in the root of a git repository as documentation source for the project. 
git blame -e shows the authors email address instead of the username. 


Git Blame vs Git Log
While git blame dipslays the last author that mdoified a line, often times you will want to knw when a line was originally added. 
This can be cumbersome to achieve using a git blame. It rquires a comibination of the -w, -C, and -M options 
It can be far more conveneniete to use the gitlog command. 
Git blame igves you the details of a file like the author who updated that file o=and every single line in that file. 


Undoing Commits & Changes 
git log- one of the best utitlities for revieiwing the history of a Git repository. 

When you have found a commit reference to the point in history you want to visit, you can utilize the git checkout command to visit that commit. 
Git checkout is an easy way to load any of these saved snapshots onto your development machine.
The head usually points to main ro some other local branch, but when you check out a orevious commit, HEAD no longer points to a branch- it points directly to a commit. 
This is called a detached Head state.

git checkout -b newbranchname will create a new brance named newbranchname and switch to that state. 




Git reset 
gitreset is an extensive command with multiple uses and functions. 
If we invoke git reset --hard the commit history is reset tot he specified commit

Udoing the last commit
These strategies are all applicable to the most recent commits. The strategies are all applicable to the most recent commit as well. 
In some cases though, you might not need to remove or reset the last commit. 

git commit --amend, this will have git open the configured systme edito and let you mdoify the last commit message. 



GIT CLEAN 
we will focus on a detailed discussion of the git clean command. 
Git clean is to some extent an 'undo' command.
Git clean command operates on untracked files. 


git clean -xf- so the -x option tells git to also include any ignored files. The -x options iwll act on all ignored files, not just project build specific ones. 
This could be unintended things like ./. IDE configuration files. 

The git REVERT command 
The git revert command can be considered an undo type command. It is not a traditional undo operation though. Instead of removing the commit from the project hsitory, it figures out how to invert the chnages introduced by the commit with the resulting inverse content.
This prevents Git from losing history which is important for the integrity 
It hsould be used when you want to apply the inverse of a commit from your porject history. 

The git commit --amend- is a convenient way to modify the most recent commit.
It lets you combine staged changes witht he previous commit instead of cretign an entriely new commit. 

It can also be used to simplue edit the previous message without changing snapshot. But, amending does not just alter the most recent commit, it replaces it entirely, meaning the amended commit will be a new entity with its own ref. 

Git rebase 
you can use git rebase to combine a sequence of committs into a new base commit.
In standard mode git rebase allows you to literally rewrite history automatically appying commits in your current working branch to the passed branch ehad





Git RM-

The git rm command is used to remove files from a Git repository.
It can be thought of as the inverse of git add command. 
It can be used to remove individula files or a collection of files. 

--dry-run will not actually rmeove files but rather output what files it owld have removed. 




Git Reflog-
reflogs track when Git refs were updated in the local repository. 
Reflogs are stored in directories under the local repository.
Time qualifiers can be combined. 
Additional PLural forms are accepted  





COLLABORATING 
GIT rmeote command- is one peice of the borader system which is reposnible for syncing changes. 
Records registered through the git remomte command are used in cnjunction
with the git fetch, git push, and igt pull commands.
Remote connections are more like bookmarks rather than direct links into other repositories.
Instead of providing real-time access to another repository, thye serve as convenient names that be used to reference a not-so-conveneient URL.

The following commands are used to view the current state of the rmeote list. 

git remote- lists the remote connections you have to other repositories. 

git remote -v- same as the above ocmmand, but includ the URL of each connection. 

git remote add- creates a new connection to a remote repository. After adding a remote you will be aleo to use <name> as a convenitner shortcut for <url>

Git Remote Discussion
Git is designed to give each developer an entirely isolated development environment. This means that information is not automatically passed back and forth between repositories. Instead, developers need to manually pull upstream commits into their local repository or manually push their local commits back up to the central repository. 

The Origin Remote 
when you clone a repository with git clone, it automatically creates a remote connection called origin pointing back to the cloned repository. 
This is useful for developers creating a local copy of a central repository, since it provides an easy way to pull upstream changes or publish local commits. 


 Repository URLS 
 Git supports mnay ways to reference a remote repository. Two of the easiset ways to access a remote repo are via the HTTP and the SSH protocols. 
 HTTP is an easy way to allow anonymous read-only access to a repository. 
 Generally thoguh it is not possible to push commits to an HTTP address.
 For read-write access, you should use SSH instead:

Git Remote Examples:
In addition to origin, it is often conveneient to have a connection to your teammate's repositories. For example, if your co-worker, John, maintained a publicly accessible repository on dev.example.com/john.git you could add a connection as follows:
git remote add john http://dev.example.com/john.git 
Having this kind of access to invidividual developer's repositories makes it possible ot collaborate outside of the central repository 

Origin I believe referes to the remote orginig in this case Github
We use cloen to import the rmeote repository locally 


Adding Remote Repositories
The git remote add command will create a new connection record to a rmeote repository. 
After adding a remote, you'll be able to use as convenenint shortcut for in other Git commands.

Inspecting a Remote. 
The show subcommand can be appeneded to git remote to give detailed output on the configuration remote. 
git remote show 

GIT FETCH AND GIT PULL
Both gitfetch and gitpull can be used to read from a rmeote repository. Both commands have different operations that are explained in further depth on ther respective links. 

Git push- the git push command is used to write to a rmeote repository. 
git push remote-name branch-name
This example will upload the local state of branch-name to the remote reposiotry specifided by remote name. 

git remote rename <old-name> <new-name>
The command git remote rename is self-explanatory. 
When executed 
git remote rm name -will remove that file  



GIT FETCH 

the git fetch command simply updates or pulls the updates from our remote tracking branches.
Basically we are getting the updates that have been pushed to our remote  branches to our local machine. 
So it pulls down the updates that have been pushed 
In review, git fetch is a primary command used to dowload contents from a remote repository. Git fetch is used in conjuction with git remote, git branch. git chekcout, and git reset to update a local repository to the state of a remote. 
Thi git fetch command is a critical piece of collaborative git work flows. 


Branches are a variation of our repositories main code so remote tracking branches are branches that have been set up to push and pull from the remote repositoris like github
Zremote branches are just like local braches, except they map to commits from somebody else's repository. 



Git Pull- 
the git pull command basically runs two commands in one, inittially it runs a git fetch and then a git merge 
git pull will download the chnages made to oyur current branch 
updating the code within your repository the merge command is where the actual udpates to the files come in. 


The following example walks through the typical workflow for synchronizing your local repository witht he central repository's main branch. 


To see what commits have been added to the upstream main, you can run a git log using origin/main as a filter:
git log --oneline main..origin/main 




Git push
git push command is used to upload a local repository cotnent to a remote repository.
Pushing is how you transfer commits from your local repository to a remote repo. 
It's the conterpart to git fetch, but whereas fetching imports commits to local branches, pushing exports commits to remote branches. Remote branches are configured using the git remote command. 

git push <remote repository> <local branch>
git push is most commonly used to publish an upload local chnages to a central repository. After a local repository has been modified a push is executed to share the mdoficiations with remote team members.


The syncing commands, operate on remote c=branches which are configured using the git remote command. 
git push can be considered and upload command whereas, git fetch and git pull can be thought of as dowload commands. 

Once chnagesets have been movded via  download or upload a git merge may be performed at the destination to integrate the changes. 





bare repository- is the same as default, but no commits can be made in a bare repository. 
The changes made in projects cannot be tracked by a bare repository as it doesn't have a working tree. 

Force Pushing 
Git prevents you from overwriting the central repository's history by refusing push requests when they result in a non-fast-forward merge. 
So, if the remote history has diverged from your history, you need to pull the remote branche and mege it inti your local one, then try pushing again. 

The --force flag overrides this behavior and makes the rmeote repository's branch match your local one, deleting any upstream changes that may have occured since you last pulled. 
