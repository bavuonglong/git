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