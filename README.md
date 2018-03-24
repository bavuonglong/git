# git

## git commands

| Key/Command | Description |
| ----------- | ----------- |
| git version | checking version |
| git config user.name |  getting username |
| git config user.email |  getting user's email |
| git config --list  | showing all configuration |
| sudo nano ~/.gitconfig  | showing and editing configuration from .gitconfig file |
| git config --global user.name "Cuong Ngo" | setting username |
| git config --global user.emal "vancuongngo.93@gmail.com" | setting user's email |
| git clone "url" | clone remote repository to local |
| git status | showing status of files |
| git add name_of_file | add specific file to staging area (pre-commit holding area) |
| git add . | add all new files, including recursing file to stating area |
| git add -A | combine the action delete and creat new into rename/move action when, in fact, we're doing renaming or moving file |
| git reset HEAD file_name | un-staged file_name, reverse the action of add command |
| git checkout -- file_name | revert file to previous stage, the stage before making change |
| git commit -m "commit content" | commit changes |
| git commit -am "commit content" | combine two commands into one, which are add and commit |
| git pull | pull new things from remote repository |
| git push origin master | push local changes to remote repository |
| git ls-files | listing all files which git is tracking |
| git mv old_file_name new_file_name |  move/rename file and inform git that this is move/rename action |


## bash commands

| Key/Command | Description |
| ----------- | ----------- |
| pwd | showing the current directory |
| mrdir folder_name |  creating foler_name |
| mrdir -p level1/level2/level3 |  creating recursing folder |
| echo "Test git quick start demo" >> start.txt  | creating new file and add content for it |
| cat start.txt | showing content file |
| rm file_name | delete filename |
| rm -rf folder_name | delete folder/directory and its sub folders, files inside those folders, r stands for recursion, f stands for force option |
| mv folder_name new_folder_name | moving/renaming folder |

## Vim editor

| Key/Command | Description |
| ----------- | ----------- |
| vi name_of_file | create new file and open by vim editor |


Hit the Esc key to enter "Command mode". Then you can type : to enter "Command-line mode". A colon (:) will appear at the bottom of the screen and you can type in one of the following commands. To execute a command, press the Enter key.

 
| Key/Command | Description |
| ----------- | ----------- |
| :q | to quit (short for :quit) |
| :q! |  to quit without saving (short for :quit!) |
| :wq |  to write and quit |
| :wq!  | to write and quit even if file has only read permission (if file does not have write permission: force write) |
| :x  | to write and quit (similar to :wq, but only write if there are changes) |
| :exit | to write and exit (same as :x) |
| :qa | to quit all (short for :quitall) |
| :cq | to quit without saving and make Vim return non-zero error (i.e. exit with error) |

You can also exit Vim directly from "Command mode" by typing ZZ to save and quit (same as :x) or ZQ to just quit (same as :q!). (Note that case is important here. ZZ and zz do not mean the same thing.)

Vim has extensive help - that you can access with the :help command - where you can find answers to all your questions and a tutorial for beginners.
