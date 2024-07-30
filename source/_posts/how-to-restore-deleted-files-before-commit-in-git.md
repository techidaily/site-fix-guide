---
title: How to Restore Deleted Files Before Commit in Git
date: 2024-07-14T06:25:59.856Z
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

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2082538/7443" target="_top" id="2082538"><img src="//a.impactradius-go.com/display-ad/7443-2082538" border="0" alt="" width="1200" height="600"/></a><img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2082538/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->
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

<!-- affiliate ads begin -->
<a href="https://newchic.sjv.io/c/5597632/1659704/14420" target="_top" id="1659704"><img src="//a.impactradius-go.com/display-ad/14420-1659704" border="0" alt="" width="728" height="90"/></a><img height="0" width="0" src="https://imp.pxf.io/i/5597632/1659704/14420" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->
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

<!-- affiliate ads begin -->
<a href="https://arkmc.pxf.io/c/5597632/427477/5172" target="_top" id="427477"><img src="//a.impactradius-go.com/display-ad/5172-427477" border="0" alt="" width="728" height="90"/></a><img height="0" width="0" src="https://arkmc.pxf.io/i/5597632/427477/5172" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->
![Git undelete single step checkout](/images/git/how-to-restore-deleted-files-before-commit-in-git/git-undelete-single-step-checkout.webp)


## 3. Restore a Batch of Deleted Files Before Commit in Git

What if we deleted a bunch of files and did not commit? Suppose we deleted 1000 files, and we now want to restore all of them.

<!-- affiliate ads begin -->
<a href="https://ship7com.pxf.io/c/5597632/1509856/17634" target="_top" id="1509856"><img src="//a.impactradius-go.com/display-ad/17634-1509856" border="0" alt="" width="730" height="383"/></a>
<!-- affiliate ads end -->
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

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2075461/7443" target="_top" id="2075461"><img src="//a.impactradius-go.com/display-ad/7443-2075461" border="0" alt="" width="1200" height="600"/></a><img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2075461/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->
![Batch restore deletions](/images/git/how-to-restore-deleted-files-before-commit-in-git/batch-restore-deletions.webp)

![All deleted files restored](/images/git/how-to-restore-deleted-files-before-commit-in-git/all-deleted-files-restored.webp)

<ins class="adsbygoogle"
    style="display:block"
    data-ad-format="autorelaxed"
    data-ad-client="ca-pub-7571918770474297"
    data-ad-slot="1223367746"></ins>






