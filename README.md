# git

## git commands basic

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
| git log |  showing history |
| git log --abbrev-commit|  showing history with concise commit hash value|
| git log --oneline --graph --decorate|  showing history with more option|
| git log -- file_name|  showing history of specific file|
| git show commitId|  showing detail of a commit by commit id|


### git commit

| Key/Command | Description |
| ----------- | ----------- |
| git commit --amend | changing the commit message of last commit|
| git rebase -i HEAD~n | using rebase in interactive mode to pick, reword, edit, squash, fixup commits; then we have to use force push|


### git comparison

| Key/Command | Description |
| ----------- | ----------- |
| git diff | compare the difference between working directory and staging area |
| git diff file_name| compare the difference between working directory and staging area for specific file |
| git diff commitId1 commitId2| compare the difference between working directory and staging area between two commits |
| git diff HEAD HEAD^| compare the difference between working directory and staging area between last commit and the previous commit of last commit |
| git difftool | compare the difference between working directory and staging area by using external diff tool|
| git diff HEAD | compare the difference between working directory and local repository |
| git difftool HEAD | compare the difference between working directory and local repository by using external diff tool|
| git diff --staged HEAD | compare the difference between staging area and local repository|
| git difftool --staged HEAD | compare the difference between staging area and local repository by using external diff tool|
| git diff master origin/master | compare the difference between local repository and remote repository|


### git branch

| Key/Command | Description |
| ----------- | ----------- |
| git branch -a | show all branch |
| git branch branch_name | create new branch |
| git checkout branch_name | switch to a branch |
| git branch -m old_branch_name new_branch_name | rename a branch |
| git branch -d branch_name | delete a branch |
| git checkout -b branch_name | switch to a new branch |

### git merge

| Key/Command | Description |
| ----------- | ----------- |
| git merge branch_name | merge branch_name into the branch we're being on with fast-forward default option|
| git merge branch_name --no-ff| merge branch_name into the branch we're being on with out fast-forward|
| git merge branch_name -m "merge message"| automatic merge |
| git branch branch_name | create new branch |
| git checkout branch_name | switch to a branch |
| git branch -m old_branch_name new_branch_name | rename a branch |
| git branch -d branch_name | delete a branch |
| git checkout -b branch_name | switch to a new branch |

* fast-forward is posible if it has no chances in master branch during the time when we switch and work on feature branch.

### git merge conflict

After switch to master branch and execute `git merge feature_branch`, in case it has conflict, it will inform we have conflict, and are being on merging stage, we need to resolve conflict by:
1. git mergetool
2. git commit -m "merge conflict message"

### git rebase

When we do rebase, it will rewind the changes happen on feature branch, playback the changes on master (source branch) on feature branch, and then apply the changes happen on feature branch. Rebase also allow us to do fast-forward merge when we're done making change on feature branch.

`git rebase master`

In conflict case when doing rebase, if we want to abort the rebase process, use: `git rebase --abort`

To resolve conflict, we use `git mergetool`

To continue rebase, we use `git rebase --continue`

Pull with rebase: when we have some changes in remote repository, and we want to rebase those change into local repository, we use: `git pull --rebase origin master`, before that, we can fetch the changes before pull to verify the status, by using `git fetch origin master`

### git stash

| Key/Command | Description |
| ----------- | ----------- |
| git stash | Saving the changes in working directory without inform git there are modified files |
| git stash apply | Un-stash |
| git stash list | Showing all stashes |
| git stash drop | Dropping last stash |
| git stash -u | Stash any changes, include un-tracked files |
| git stash pop | Apply stash and drop that stash, combination of `apply` and `drop` |
| git stash save "message" | Stash with specific message |
| git stash show stash@{1} | Showing detail of stash number 1 |
| git stash apply stash@{1} | Applying specific stash |
| git stash drop stash@{1} | Dropping specific stash |
| git stash clear | Clearing all stashes |
| git stash branch branch_name | Popping stash to new branch |


### git tag

| Key/Command | Description |
| ----------- | ----------- |
| git tag tag_name | Putting a tag with tag_name |
| git tag tag_name -m "tag message"| Putting a tag with tag_name and tag_message|
| git tag --list | Showing all tags |
| git show tag_name | Showing commit that adds that tag |
| git tag --delete tag_name | Deleting specific tag |
| git tag -a tag_name | Creating an annotated tag, which contains more information via commit message when tagging |
| git diff tag1 tag2 | Comparing the difference between two tags |
| git tag -a tag_name commit_id | Tagging specific commit |
| git tag -a tag_name -f commit_id | Moving tag to specific commit |
| git push tag_name | Pushing specific tag_name to remote repo |
| git push origin branch_name --tags | Pushing all the tags to remote repo |
| git push origin :tag_name | Deleting specific tag on remote repo |

### git alias

| Key/Command | Description |
| ----------- | ----------- |
| git config --global alias.hist "log --all --graph --decorate --oneline" | creat alias command, long to short |


### git ignore pattern

| Key/Command | Description |
| ----------- | ----------- |
| MyFile.txt | specific type |
| *.txt | file pattern |
| my-folder/ | folder |

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
