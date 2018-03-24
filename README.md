# git



pwd
mrdir projects

## checking version
git version

## getting
git config user.name

git config user.email

git config --list

sudo nano ~/.gitconfig

## setting
git config --global user.name "Cuong Ngo"

git config --global user.emal "your@email.com"

git clone "url"

git status

## creat and add content to a file
echo "Test git quick start demo" >> start.txt

## see the content of file
cat start.txt


git add name_of_file

git commit -m "commit content"

git push origin master






## Vim editor
vi name_of_file

Hit the Esc key to enter "Command mode". Then you can type : to enter "Command-line mode". A colon (:) will appear at the bottom of the screen and you can type in one of the following commands. To execute a command, press the Enter key.

:q to quit (short for :quit)

:q! to quit without saving (short for :quit!)

:wq to write and quit

:wq! to write and quit even if file has only read permission (if file does not have write permission: force write)

:x to write and quit (similar to :wq, but only write if there are changes)

:exit to write and exit (same as :x)

:qa to quit all (short for :quitall)

:cq to quit without saving and make Vim return non-zero error (i.e. exit with error)

You can also exit Vim directly from "Command mode" by typing ZZ to save and quit (same as :x) or ZQ to just quit (same as :q!). (Note that case is important here. ZZ and zz do not mean the same thing.)

Vim has extensive help - that you can access with the :help command - where you can find answers to all your questions and a tutorial for beginners.
