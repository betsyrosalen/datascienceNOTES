# datasciencecoursera - NOTES

## Git Vocabulary

**Command Line:** The computer program we use to input Git commands. On a Mac, it’s called Terminal. On a PC, it’s a non-native program that you download when you download Git for the first time (we’ll do that in the next section). In both cases, you type text-based commands, known as prompts, into the screen, instead of using a mouse.

**Repository:** A directory or storage space where your projects can live. Sometimes GitHub users shorten this to “repo.” It can be local to a folder on your computer, or it can be a storage space on GitHub or another online host. You can keep code files, text files, image files, you name it, inside a repository.

**Version Control:** Basically, the purpose Git was designed to serve. When you have a Microsoft Word file, you either overwrite every saved file with a new save, or you save multiple versions. With Git, you don’t have to. It keeps “snapshots” of every point in time in the project’s history, so you can never lose or overwrite it.

**Commit:** This is the command that gives Git its power. When you commit, you are taking a “snapshot” of your repository at that point in time, giving you a checkpoint to which you can reevaluate or restore your project to any previous state.

**Branch:** How do multiple people work on a project at the same time without Git getting them confused? Usually, they “branch off” of the main project with their own versions full of changes they themselves have made. After they’re done, it’s time to “merge” that branch back with the “master,” the main directory of the project.

## Git-Specific Terminal Commands

`git init`: Initializes a new Git repository _IN THE CURRENT DIRECTORY_. Make sure you create a directory and navigate to it before this step.  Until you run this command inside a repository or directory, it’s just a regular folder. Only after you input this does it accept further Git commands.

`git config`: Short for “configure,” this is most useful when you’re setting up Git for the first time.  

Examples: 

- `git config --global user.name "Betsy"`
- `git config --global user.email betsy@mylittleuniverse.com`
- `git config --global color.ui true` (Pretty command line colors)

`git help`: Forgot a command? Type this into the command line to bring up the 21 most common git commands. You can also be more specific and type “git help init” or another term to figure out how to use and configure a specific git command.  You can add the specific ommand you need help with after the word help.  
Examples: `git help add`, `git help config`, `git help commit`, etc...

`git status`: Check the status of your repository. See which files are inside it, which changes still need to be committed, and which branch of the repository you’re currently working on.

`git add`: This does not add new files to your repository. Instead, it brings new files to Git’s attention. After you add files, they’re included in Git’s “snapshots” of the repository.

Examples: 

- `git add example.txt` adds adds just the one file to the staging area.
- `git add example.txt webpage.html` adds adds both files file to the staging area.
- `git add --all` adds all new or modified files to the to the staging area.
- `git add *.txt` adds all txt files in _the current directory_ to the staging area.
- `git add "*.txt"` adds all txt files _in the whole project_ to the staging area.
- `git add docs/*.txt` adds all txt files _in the docs directory_ to the staging area.
- `git add docs/` adds _all files_ in the docs directory to the staging area.

`git commit -m "Commit Message"`: Git’s most important command. After you make any sort of change, you input this in order to take a “snapshot” of the repository. Usually it goes git commit -m “Message here.” The -m indicates that the following section of the command should be read as a message.

`git branch`: Working with multiple collaborators and want to make changes on your own? This command will let you build a new branch, or timeline of commits, of changes and file additions that are completely your own. Your title goes after the command. If you wanted a new branch called “cats,” you’d type git branch cats.

`git checkout`: Literally allows you to “check out” a repository that you are not currently inside. This is a navigational command that lets you move to the repository you want to check. You can use this command as git checkout master to look at the master branch, or git checkout cats to look at another branch.

`git merge`: When you’re done working on a branch, you can merge your changes back to the master branch, which is visible to all collaborators. git merge cats would take all the changes you made to the “cats” branch and add them to the master.

`git push`: If you’re working on your local computer, and want your commits to be visible online on GitHub as well, you “push” the changes up to GitHub with this command.

`git push -u origin master` tells Git to push our changes to the "master" (or main) branch of the "origin" (or primary) remote.  You only need to include the `-u origin master` once, as Git will remember this configuration for future pushes `git push` then becomes sufficient, assuming you don't want to do anything fancy

`git pull`: If you’re working on your local computer and want the most up-to-date version of your repository to work with, you “pull” the changes down from GitHub with this command.

`git log`: Shows Git timeline history

## Useful Terminal Commands

### Show Hidden Files in Finder

`defaults write com.apple.finder AppleShowAllFiles TRUE`

`killall Finder`

### Securely Erase Free Space

When you delete files on your Mac, OS X still leaves fragments of the file all over the free space on your hard disk drive, until these are written over by new files. If you want to securely delete all the remaining fragments on a hard disk drive (for example if you're going to sell your Mac), then execute the following command:

`diskutil secureErase freespace 3 /Volumes/name-of-drive`

Replace /name-of-drive with the drive you want to erase. This command uses a special algorithm to wipe over each free area of space 35 times, far above the US Department of Defense's standard, which only requires 7 passes. Be aware though that this process can take days on larger drives.

On a side note, the command diskutil is a really useful one and allows you to manage local disks and volumes directly from the Terminal (a list of sample commands is given). Be aware, though, that most commands require root access.

## Basic Terminal Commands

`cd`	Home directory

`cd [folder]`	Change directory e.g. cd documents

`cd /`	Root of drive

`cd -`	Previous directory

`ls`	Short listing

`ls -l`	Long listing

`ls -a`	Listing incl. hidden files

`ls -lh`	Long listing with Human readable file sizes

`ls -R`	Entire content of folder recursively

`sudo [command]`	Run command with the security privileges of the superuser (Super User DO)

`open [file]`	Opens a file ( as if you double clicked it )

`top`	Displays active processes. Press q to quit

`nano [file]`	Opens the file using the nano editor

`vim [file]`	Opens the file using the vim editor

`clear`	Clear screen

`reset`	Resets the terminal display

`touch [file]`	Create new file

`pwd`	Full path to working directory

`.`	Current folder, e.g. ls .

`..`	Parent/enclosing directory, e.g. ls ..

`ls -l ..`	Long listing of parent directory

`cd ../../`	Move 2 levels up

`cat`	Concatenate to screen

`rm [file]`	Remove a file, e.g. rm data.tmp

`rm -i [file]`	Remove with confirmation

`rm -r [dir]`	Remove a directory and contents

`rm -f [file]`	Force removal without confirmation

`cp [file] [newfile]`	Copy file to file

`cp [file] [dir]`	Copy file to directory

`mv [file] [new filename]`	Move/Rename, e.g. mv file1.ad /tmp

`pbcopy < [file]`	Copies file contents to clipboard

`pbpaste`	Paste clipboard contents

`pbpaste > [file]`	Past clipboard contents into file, pbpaste > paste-test.txt

`mkdir [dir]`	Create new directory

`mkdir -p [dir]/[dir]`	Create nested directories

`rmdir [dir]`	Remove directory ( only operates on empty directories )

`rm -R [dir]`	Remove directory and contents

`[command] | [command]`	Allows to combine multiple commands that generate output, e.g. cat data.txt | pbcopy

`less`	Output content delivered in screensize chunks

`[command] > [file]`	Push output to file, keep in mind it will get overwritten

`[command] >> [file]`	Append output to existing file

`[command] < [file]`	Tell command to read content from a file

`find [dir] -name [search_pattern]`	Search for files, e.g. find /Users -name "file.txt"

`grep [search_pattern] [file]`	Search for all lines that contain the pattern, e.g. grep "Tom" file.txt

`grep -r [search_pattern] [file]`	Recursively search for all lines that do not contain the pattern

`grep -v [search_pattern] [file]`	Search for all lines that do NOT contain the pattern

`[command] -h`	Offers help

`[command] —help`	Offers help

`info [command]`	Offers help

`man [command]`	Show the help manual for [command]

`whatis [command]`	Gives a one-line description of [command]

`apropos [search-pattern]`	Searches for command with keywords in description

`history n`	Shows the stuff typed – add a number to limit the last n items

`Ctrl + r`	Interactively search through previously typed commands

`![value]`	Execute the last command typed that starts with ‘value’

`!!`	Execute the last command typed
