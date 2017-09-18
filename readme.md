![Skylab Coders Academy](http://www.skylabcoders.com/images/403/default.png "Skylab Coders Academy")

Skylab FullStack WebDevelopment Bootcamp 201709
===============================================

# Basic Tools

## Console

*Emulators*:

[Commander](http://cmder.net)
[Cygwin](http://cygwin.com)

### Useful how-to's

- see path to working directory

```bash
$ pwd
```

- list files in directory

```bash
$ ls
```

- list files in list mode

```bash
$ ls -l
```

- list hidden files

```bash
$ ls -a
```

- combine listing modes (ex: hidden and list mode)

```bash
$ ls -la
```

- create an empty file

```bash
$ touch <file>
```

- create a file with content in one command

```bash
$ echo "<content with spaces>" > <file>
```

- see the content of a text file

```bash
$ cat <file>
```

vim-like

```bash
$ less <file>
```

- create a directory

```bash
$ mkdir <directory>
```

- copy a file

```bash
$ cp <from-file> <to-file>
```

- copy a directory

```bash
$ cp -r <from-directory> <to-directory>
```

- move or rename a file or directory

```bash
$ mv <from-file-or-directory> <to-file-or-directory>
```

- move a directory with content

```bash
$ mv -r <from-directory> <to-directory>
```

- remove a file

```bash
$ rm <file>
```

- remove a directory

```bash
$ rm -d <directory>
```

- remove a directory recursively

```bash
$ rm -r <directory>
```

## Markdown

### Links

[Google](http://www.google.com "Google!")

### References

This is [an example][id] reference-style link.
This is [an example][id] reference-style link.

[id]: http://example.com/  "Optional Title Here"

### Tables

<table>
    <tr>
        <td>Hellow</td><td>World</td>
    </tr>
</table>

### Code block

<code>
    This is a code block.
</code>

### Lists

* One
* Two
* Three

- A
- B
- C

<ul>
    <li>a</li>
    <li>b</li>
    <li>c</li>
</ul>

1.  Bird
1.  McHale
3.  Parish

<ol>
    <li>a</li>
    <li>b</li>
    <li>c</li>
</ol>


a. 1
b. 2
c. 3

### Emphazises

*single asterisks*

_single underscores_

**double asterisks**

__double underscores__

### Blockquotes

> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.

> ## This is a header.
> 
> 1.   This is the first list item.
> 2.   This is the second list item.
> 
> Here's some example code:
> 
>     return shell_exec("echo $input | $markdown_script");

### Comments

```html
<!-- this is a comment -->
```

## Git

* Init a bare repo ("remote")

```bash
$ git init --bare
```

* Init a local repo (to be connected to remote repo)

```bash
$ git init
```

* Add file or directory to stage

```bash
$ git add <file-or-directory>
```

* Remove file or directory from stage

```bash
$ git rm --cached <file-or-directory>
```

* Commit a the changes in stage

```bash
$ git commit -m '<a short message that describes  the commit>'
```

* Push changes from local to remote repo

```bash
$ git push
```

* Pull changes from remote to local repo

```bash
$ git pull
```

##GIT
```bash
Git, es un software de control de versiones
Rapidez en la gestión de ramas, debido a que Git nos dice que un cambio será fusionado mucho más frecuentemente de lo que se escribe originalmente.

Gestión distribuida; Los cambios se importan como ramas adicionales y pueden ser fusionados de la misma manera como se hace en la rama local.

Gestión eficiente de proyectos grandes.

Realmacenamiento periódico en paquetes.
##CREAR UN REPOSITORIO NUEVO
git init --bare
```

```bash
To tell Git to start tracking changes made to octocat.txt, we first need to add it to the staging area by using git add.

git add octocat.txt
```

```bash
o store our staged changes we run the commit command with a message describing what we've changed. Let's do that now by typing:

git commit -m "Add cute octocat story"
```

```bash
Adding All Changes
Great! You also can use wildcards if you want to add many files of the same type. Notice that I've added a bunch of .txt files into your directory below.

I put some in a directory named "octofamily" and some others ended up in the root of our "octobox" directory. Luckily, we can add all the new files using a wildcard with git add. Don't forget the quotes!
git add '*.txt'
``` 
```bash
We can check for changes on our GitHub repository and pull down any new changes by running:

git pull origin master

In this case we want the diff of our most recent commit, which we can refer to using the HEAD pointer.

git diff HEAD
```

```bash
You can unstage files by using the git reset command. Go ahead and remove octofamily/octodog.txt.

git reset octofamily/octodog.txt
```
```bash
Files can be changed back to how they were at the last commit by using the command: git checkout -- <target>. Go ahead and get rid of all the changes since the last commit for octocat.txt

git checkout -- octocat.txt
```
```bash
We want to remove all these pesky octocats, so let's create a branch called clean_up, where we'll do all the work:

git branch clean_up
```
```bash
Great! Now if you type git branch you'll see two local branches: a main branch named master and your new branch named  clean_up.

You can switch branches using the git checkout <branch> command. Try it now to switch to the clean_up branch:

git checkout clean_up
```

```bash
You are going to want to use a wildcard again to get all the octocats in one sweep, go ahead and run:

git rm '*.txt'
```

```bash
Now that you've removed all the cats you'll need to commit your changes.

Feel free to run git status to check the changes you're about to commit.

git commit -m "Remove all the cats"
```
```bash
Switching Back to master
Great, you're almost finished with the cat... er the bug fix, you just need to switch back to the master branch so you can copy (or merge) your changes from the clean_up branch back into the master branch.

Go ahead and checkout the master branch:

git checkout master
```
```bash
Alrighty, the moment has come when you have to merge your changes from the clean_up branch into the master branch. Take a deep breath, it's not that scary.

We're already on the master branch, so we just need to tell Git to merge the clean_up branch into it:

git merge clean_up
```
```bash
You can use git branch -d <branch name> to delete a branch. Go ahead and delete the clean_up branch now:

git branch -d clean_up
```
```bash
Here we are, at the last step. I'm proud that you've made it this far, and it's been great learning Git with you. All that's left for you to do now is to push everything you've been working on to your remote repository, and you're done!

git push
```