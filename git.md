# Git Exercises Writeup

1. Here we have to simply push a code which is already committed.

```
git push
git verify 
```

2. We have to add one file to the staging area and commit it. 

```
git add A.txt
git commit -m "one file committed"
```

3. Both files are added to the staging area. we have to commit one of them using the reset command which removes all the files from the staging area.

```
git reset
git add A.txt
git commit -m "only one file committed"
```

4. we'll first create a .gitignore file which is hidden. then we write the rules as to which files to be ignored while committing. 
```
*.exe
*.o
*.jar
 git add .gitignore
 git commit -m "ignored"
 ```

 5. we are on the chase-branch. we have to merge it with the escaped branch.
 ```
 git merge escaped
 git verify
 ```

 6. on merging another-piece-of-work, it will show a merge conflict in a file named equation.txt. we then open this file with the help of nano- a text editor. we modify the text to 2 + 3 = 5. Issue resolved.

 ```
 git merge another-piece-of-work
 nano equation.txt
 git add .
 git commit -m "done"
 ```

 7. we are currently working on a file we don't want to commit, but work on another file temporarily. 
 ```
 git stash
 ```
 this command clears the working area by putting that file into a stack. 

