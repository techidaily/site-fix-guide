---
title: How to Restore Deleted Files Before Commit in Git
date: 2024-02-26 12:00:00
tags: 
  - git restore
  - undo
  - restore deleted files
categories: 
  - git
description: Learn how to restore deleted files before commit in Git using the reset and checkout commands. We also show how to batch restore deleted files in Git.
keywords: git restore, undo, restore deleted files, git reset, git checkout
---

This tutorial demonstrates restoring deleted files before commit in Git.

- Restore Deleted Files Before Commit Using the reset and checkout Commands in Git
- Restore Deleted Files Before Commit Using the git checkout Command in Git
- Restore a Batch of Deleted Files Before Commit in Git

We use the git checkout and git reset commands to restore deleted files before committing. Git provides us with powerful options to do complex tasks with these commands.

We can either unstage deleted file first and then restore it in the working tree in a separate step. Alternatively, we can combine the two operations into one step.

This tutorial shows a clever trick to batch undelete multiple files with a single command.

## 1. Restore Deleted Files Before Commit Using the `reset` and `checkout` Commands in Git

First, let us set up a repository and add a few files. It looks like this:

![Initial Repo Before Deletes](/images/git/how-to-restore-deleted-files-before-commit-in-git/initial-repo-before-deletes.webp)

Our first couple of commits look like this in the log:

![Initial Repo Commits](/images/git/how-to-restore-deleted-files-before-commit-in-git/initial-repo-commits.webp)

We now delete a file with the `rm` command.

The deleted file **file7.txt** is no longer present in our repository.

![Delete file](/images/git/how-to-restore-deleted-files-before-commit-in-git/delete-file.webp)

The default behavior of `rm` is to stage the delete changes automatically.

![Rm-Autostages-Deletion](/images/git/how-to-restore-deleted-files-before-commit-in-git/rm-autostages-deletion.webp)

We now proceed to restore deleted file before committing.

First, we unstage the deletion with the `reset` command.

```bash
git reset <commit_hash> [--] <path_to_file>
```

This command restores the index to the state of the c`ommit_hash` for all files that match the `path_to_file` parameter.

```bash
git reset HEAD --file7.txt
```

This restores the index to `HEAD` for `file7.txt`. HEAD points to our last commit.

Remember, we have not committed the deletion, so our last commit does not have the deletion entry.

In essence, we use this command to unstage deleted files.

![Git reset unstage change](/images/git/how-to-restore-deleted-files-before-commit-in-git/git-reset-unstage-change.webp)

![Unstage deleted file](/images/git/how-to-restore-deleted-files-before-commit-in-git/unstage-deleted-file.webp)

Next, we restore the deleted file in the working area with the `git checkout` command.

``` bash
git checkout [--] <path_to_file>
```

`checkout` overwrites content in the working tree with the index in this form.

``` bash
git checkout -- file7.txt
```

![Git restore deleted file 2 steps](/images/git/how-to-restore-deleted-files-before-commit-in-git/git-restore-deleted-file-2-steps.webp)

## 2. Restore Deleted Files Before Commit Using the `git checkout` Command in Git

The `git checkout` command provides us with a form where we can combine the two steps above into one.

``` bash
git checkout <commit> [--] <path_to_file>
```

In this form, `git checkout` overwrites content in both the index and working areas with commit.

``` bash
git checkout HEAD -- file7.txt
```

`HEAD` points to our last commit. We did not commit the deletion, so our last commit does not know the delete operation.

![Git undelete single step checkout](/images/git/how-to-restore-deleted-files-before-commit-in-git/git-undelete-single-step-checkout.webp)


## 3. Restore a Batch of Deleted Files Before Commit in Git

What if we deleted a bunch of files and did not commit? Suppose we deleted 1000 files, and we now want to restore all of them.

![Delete several files](/images/git/how-to-restore-deleted-files-before-commit-in-git/delete-several-files.webp)

Typing the above commands 1000 times isn’t a programmer’s way to do stuff. Instead, we can use wildcards in the path specifiers to match many files and undelete them with a single command.

``` bash
git reset HEAD .
```

This is the same command as above, except we replaced `file7.txt` with the `.` wildcard. The `.` tells git to match all files.

So, this command unstages all of our deleted files. We then restore them in the working area.

``` bash
git checkout .
``` 

The same command with `file7.txt` is again replaced with the `.` wildcard. It restores all the unstaged deletions in one go.

![Batch restore deletions](/images/git/how-to-restore-deleted-files-before-commit-in-git/batch-restore-deletions.webp)

![All deleted files restored](/images/git/how-to-restore-deleted-files-before-commit-in-git/all-deleted-files-restored.webp)
