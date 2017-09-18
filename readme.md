<[Skylab]!http://www.skylabcoders.com/images/403/default.png
#Skylab Bootcamp 2017-Sep
------------------------
###Basic tools
------------
##Markdown
---------
##Para comentar en Markdown
```bash
$ pwd

```
##How to list a directory
```bash
$ ls

```
##Links
---------
##My favourite search engine
[Google](http://www.google.com "Google!")
##Comandos consola
mkdir (crar directorio)
mv (mover o renombrar ficheros (carpetas)

#How to copy a file 
```
$ cp <from-file> <to file>
```
#How to copy a directory
```
$ cp <from-directory> <to directory>
```
# How to move or rename a directory (si hay path destino o no)
```
$ mv <from-file-or-directory> <to-file-or-directory>
```
#How to move  a directory
```
$ mv -r <from-file-or-directory> <to-file-or-directory>
```
#How to see a content of a text file   
```
&less <file>
```

pwd outputs the name of the current working directory.
ls lists all files and directories in the working directory.
cd switches you into the directory you specify.
mkdir creates a new directory in the working directory.
touch creates a new file inside the working directory.


##BASH
```
Type Ctrl + O to save the file.

Press Enter to write the filename.

Type Ctrl + X to exit.

Finally, type clear to clear the terminal window.

``` 

##GIT
```
Git, es un software de control de versiones
Rapidez en la gestión de ramas, debido a que Git nos dice que un cambio será fusionado mucho más frecuentemente de lo que se escribe originalmente.

Gestión distribuida; Los cambios se importan como ramas adicionales y pueden ser fusionados de la misma manera como se hace en la rama local.

Gestión eficiente de proyectos grandes.

Realmacenamiento periódico en paquetes.
##CREAR UN REPOSITORIO NUEVO
```
git init --bare

```
```
To tell Git to start tracking changes made to octocat.txt, we first need to add it to the staging area by using git add.

git add octocat.txt
```
```
o store our staged changes we run the commit command with a message describing what we've changed. Let's do that now by typing:

git commit -m "Add cute octocat story"
```
```
Adding All Changes
Great! You also can use wildcards if you want to add many files of the same type. Notice that I've added a bunch of .txt files into your directory below.

I put some in a directory named "octofamily" and some others ended up in the root of our "octobox" directory. Luckily, we can add all the new files using a wildcard with git add. Don't forget the quotes!

git add '*.txt'
```
```
We can check for changes on our GitHub repository and pull down any new changes by running:

git pull origin master

In this case we want the diff of our most recent commit, which we can refer to using the HEAD pointer.

git diff HEAD
```
```
You can unstage files by using the git reset command. Go ahead and remove octofamily/octodog.txt.

git reset octofamily/octodog.txt
```
```
Files can be changed back to how they were at the last commit by using the command: git checkout -- <target>. Go ahead and get rid of all the changes since the last commit for octocat.txt

git checkout -- octocat.txt
```
```
We want to remove all these pesky octocats, so let's create a branch called clean_up, where we'll do all the work:

git branch clean_up
```
```
Great! Now if you type git branch you'll see two local branches: a main branch named master and your new branch named  clean_up.

You can switch branches using the git checkout <branch> command. Try it now to switch to the clean_up branch:

git checkout clean_up
```
```
Ok, so you're in the clean_up branch. You can finally remove all those pesky octocats by using the git rm command which will not only remove the actual files from disk, but will also stage the removal of the files for us.

You're going to want to use a wildcard again to get all the octocats in one sweep, go ahead and run:

git rm '*.txt'
```
```
Now that you've removed all the cats you'll need to commit your changes.

Feel free to run git status to check the changes you're about to commit.

git commit -m "Remove all the cats"
```
```
Switching Back to master
Great, you're almost finished with the cat... er the bug fix, you just need to switch back to the master branch so you can copy (or merge) your changes from the clean_up branch back into the master branch.

Go ahead and checkout the master branch:

git checkout master
```
```
Alrighty, the moment has come when you have to merge your changes from the clean_up branch into the master branch. Take a deep breath, it's not that scary.

We're already on the master branch, so we just need to tell Git to merge the clean_up branch into it:

git merge clean_up
```
```
You can use git branch -d <branch name> to delete a branch. Go ahead and delete the clean_up branch now:

git branch -d clean_up
```
```
Here we are, at the last step. I'm proud that you've made it this far, and it's been great learning Git with you. All that's left for you to do now is to push everything you've been working on to your remote repository, and you're done!

git push
```