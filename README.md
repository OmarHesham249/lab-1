# Git Lab 1

## Objective

Practice basic Git operations including creating repositories, making commits, modifying commit history, and using revert.

---

## 1. Initialize Local Repository

A new local repository was created using:

```
git init
```

Then a file containing my full name was created:

```
echo "Omar Hesham" > name.txt
```

The file was added and committed:

```
git add .
git commit -m "First commit"
```

---

## 2. Connect to Remote Repository

A remote repository was created on GitHub and connected to the local repository:

```
git remote add origin git@github.com:OmarHesham249/lab-1.git
```

The project was pushed to the remote repository:

```
git branch -M main
git push -u origin main
```

---

## 3. Creating Multiple Commits

Several commits were created by modifying the file:

```
echo "line2" >> name.txt
git add .
git commit -m "commit2"

echo "line3" >> name.txt
git add .
git commit -m "commit3"

echo "line4" >> name.txt
git add .
git commit -m "commit4"
```

---

## 4. Deleting the Last Two Commits

The last two commits were removed using:

```
git reset --hard HEAD~2
```

---

## 5. New Commit After Deletion

A new change was added and committed:

```
echo "new line" >> name.txt
git add .
git commit -m "commit after deletion"
```

---

## 6. Amending the Last Commit

A new line was added to the file:

```
echo "lab Done" >> name.txt
```

Then the last commit was amended with a new message:

```
git add .
git commit --amend -m "finish"
```

---

## 7. Revert Concept

`git revert` is used to undo changes from a previous commit by creating a new commit that reverses its changes.
Unlike `git reset`, it does not remove commits from history.

Example:

```
git revert HEAD
```

---

## 8. Bonus: Revert 3 Commits Back

To revert the last three commits:

```
git revert HEAD~2..HEAD
```

This creates new commits that undo the changes introduced by the last three commits.
* Modifying commits with amend
* Reverting commits
