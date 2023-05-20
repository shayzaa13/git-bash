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
```
nano file.txt
```

fix the bug here (remove the highlighted line in the file) and add and commit changes.

```
git stash pop
```

this brings back the stacked file you were previously working on.
Again open bug.txt and add the following line- <br>
'Finally, finished it!'

Add and commit changes and verify.

---

<br>

8. the head is at change-branch-history at first.merge it with hot bug-fix.
   now, the head is at hot bug-fix. use git rebase command for the last 2 commits. this changes the order of commits.

```
git merge hot-bugfix
git rebase hot-bugfix
```

---

<br>

9. the file should have been ignored but is being tracked due to its commit.

```
git rm --cached ignored.txt
```

this command untracks the file but doesn't remove it completely (the file still remains in the directory)

Add and commit changes.

---

<br>

10. since Windows doesn't differentiate between uppercase an lowercase letters in filenames, we'll copy the contents of File.txt into a temporary file and then do the same with this temporary file and file.txt

```
git mv File.txt temp.txt
git mv temp.txt file.txt
```

Add and commit changes.

---

<br>

11. First, fix the bug in the file.
    now add that file.

```
git commit --amend
```

this will implement changes on the same previous commit.

---

<br>

12.

```
git commit --amend --date="1987-01-13 00:00:00"
```

this command does the same thing except that you can modify when was it last committed.

---

<br>

13. using rebase in the interactive mode-

```
git rebase -i HEAD~2
```

this command will open an interactive window, replace pick with edit, as we want tpo edit the file at that commit.

by this, we the head comes on the branch whose commit we've to change.
now, open the file and fix the typo error.
add and commit changes using amend, as the file is alraedy committed.

```
git rebase --continue
```

this command allows git to continue with the remainig commits.
but this command will raise a merge conflict.

open file.txt and make required changes.

again do git rebase --continue

Add, commit and verify.

---

Done ;)


