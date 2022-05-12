# Comandos para git

_This repository is used with the purpose of learning a little about git and github, I will put the commands that I learn and at the same time I will use git to put it into practice (I do not speak English but I am learning it :D)_

---


We will use some bash comamands:

+ To change the directory
+ go back

``` 
cd 
cd ..
```
+ to list the directories (hidden)

~~~
ls
ls -a
ls -la
~~~
+ Clear the terminal
~~~
clear
~~~
+ Delete something
~~~
rm <file_name>
~~~
+ Create a file
~~~
touch <file_name.extension>
~~~
+ Create directory
~~~
mkdir <directory_name>
~~~
+ Open VS code in this directory
~~~
code .
~~~
+ move or rename files
~~~
mv <file> <directory>
mv <newname> <oldname>
~~~
+ view the contents of a file
~~~
cat <fileName>
~~~

---

To initialize a new repository, we first locate ourselves in the directory that we will use, and we type git init to initialize reposritory, this will add the .git directory.
~~~
git init 
~~~
+ remove a git repository
~~~
rm -fr .git
~~~
In git we have 4 sections, the working area is our computer, the stage is the wait zone, and we can commit the files of stage, and finally we can put the commits on a server (gitHUb)

to see the status of the repository
~~~
git status
git status -s             (short version)
~~~
add a file to stage area
~~~
git add <filename> <filename>..  we add file by file
git add *.txt                    we add only the files wit a .txt extension
git add .                        we add all the files   
~~~
commit our work
~~~
git commit -m "message with information about the change"
~~~
To delete files of the commit or stage area we need to delete these files in the repository and then add the changes (deleted files) to the stage area
~~~
rm <filename>
git rm <filename>       with this we make it faster, we add the deleted file to the stage area inmediately
~~~
to restore a change that we have left in stage, we use the following command
~~~
git restore --staged <filename>
~~~
to rename file or move a file
~~~
rm <filename> <newename/directory>
git rm rm <filename> <newename/directory>       with this we inmediately add the changes to staggin
~~~
To ignore files or directories we need to create a .gitignore in this file, we will list the files we need to ignore
~~~
.gitignore
~~~
see the changes in the files
~~~
git diff 
git diff --staged   see teh changes in staged
~~~
to see the history
~~~
git log
git log --oneline       
~~~
we can create a branch to which we add commits. This branch is separate from the main branch, and when we're done, we can request a merge with the main branch.

+ look at which branch we are
~~~
git branch
~~~
+ create a branch
~~~
git checkout -b <branchName>
~~~
+ change of branch
~~~
git checkout <branchName>
~~~
+ to bring a branch to the main branch (we need to locate in the main branh)
~~~
git merge <branchName>
~~~
## Github
first we create a repository, then we use in the terminal the following command
it serves to indicate that we have a remote server in which we can upload the changes, with add origin we indicate where the code is and where we will upload it
~~~
git remote add origin <linkrepository>
~~~
to upload changes, regarding the branch with which we are working. With - u we indicate that we want to create that branch in our gitHub repository
~~~
git push 
git push -u origin <branch>
~~~
to upload another branch, we switch branches, and use the same command as before
~~~
git checkout <branch>
git push -u origin <branch>
~~~
