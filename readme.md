git: file system

# git init
(master): master branch of git
ls -a: show all files/dir in current dir, including hidden one .git  

# git add <file>
add from working dir to staging area
3 states:
    working dir: area where all our files/dir and changes are living all the time
    staging area: files/dir that we explicitely add to staging area
    repository: .git dir, whre all our snapshots are stored
# git status
red = untracked
green = ready to be commited
            
# git commit -m "message"
reference for us, what it is, start with present tense verb, eg. "Add readme.md"

# git log
show history of all snapshots:
author:
date:
"message"

====================
add multiple fiels of a certain type
# git add *.html

add all files including hidden ones(start with . eg .hidden.txt)
# git add -A 

remove files from staging area
# git reset HEAD <file>

ignore files
# create file: .gitignore
add file name to be ignored

==================== git branches
              /----0----0----0  feature branch
             /              /   
0-----------0----0----0----0    master branch
playing with new features without affacting original master branch
-> potentially merge in future

list branches
# git branch
*green = branch we are in currently

add a branch
# git checkout -b <branch_name>
'checkout' will switch to a new branch

branch checkout
# git checkout <branch_name>

merge a branch;
feature branch
              /----0  feature branch
             /           
0-----------0 master branch
master branch:
0-----------0----0   master branch
they don't know each other->merge
# git merge <branch_name>
make a new commit to tie two branches
eg: (master) git merge feature1
              /----0--\  feature branch
             /         \     
0-----------0----0------0 master branch
->we can continue working on master, or on feature and merge them again
              /----0--\----0----0  feature branch
             /         \     
0-----------0----0------0-------0  master branch
fast forward scenario: no new commits on master after creating feature branch
              /----0  feature branch
             /     |         
0-----------0------0  master branch
=> 0-----------0------0  master branch

remove a branch
# git branch -d <branch_name>

==================== github
copy ssh keys from c9 to github
link github repository to local c9 respository

