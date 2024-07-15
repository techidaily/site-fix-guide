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





<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://extra-approaches.techidaily.com/2024-approved-samsungs-advanced-2023-bd-j5900-reviewed-here/"><u>2024 Approved  Samsung's Advanced 2023 BD-J5900 Reviewed Here</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-y100a-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo Y100A | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-x-flip-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo X Flip | Dr.fone</u></a></li>
<li><a href="https://iphone-unlock.techidaily.com/how-to-remove-passcode-from-apple-iphone-12-mini-complete-guide-drfone-by-drfone-ios/"><u>How To Remove Passcode From Apple iPhone 12 mini? Complete Guide | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-y100i-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo Y100i | Dr.fone</u></a></li>
<li><a href="https://youtube-zero.techidaily.com/cing-video-success-top-8-yt-thumbnail-strategies-for-2024/"><u>Enhancing Video Success  Top 8 YT Thumbnail Strategies for 2024</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-v27e-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo V27e | Dr.fone</u></a></li>
<li><a href="https://ai-driven-video-production.techidaily.com/updated-2024-approved-looking-beyond-final-cut-pro-x-10-top-video-editing-software-options/"><u>Updated 2024 Approved Looking Beyond Final Cut Pro X 10 Top Video Editing Software Options</u></a></li>
<li><a href="https://tiktok-videos.techidaily.com/updated-mastering-tiktok-step-by-step-caption-techniques/"><u>[Updated] Mastering TikTok  Step-by-Step Caption Techniques</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-t2-pro-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo T2 Pro 5G | Dr.fone</u></a></li>
<li><a href="https://unlock-android.techidaily.com/how-to-show-wi-fi-password-on-honor-magic-6-lite-by-drfone-android/"><u>How to Show Wi-Fi Password on Honor Magic 6 Lite</u></a></li>
<li><a href="https://video-capture.techidaily.com/new-2024-approved-digital-scribes-leading-screen-recorder-software/"><u>[New] 2024 Approved  Digital Scribes  Leading Screen Recorder Software</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-v29-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo V29 Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-v30-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo V30 Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-tecno-spark-10-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Tecno Spark 10 5G | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-v29e-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo V29e | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-v30-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo V30 | Dr.fone</u></a></li>
<li><a href="https://extra-skills.techidaily.com/pathfinders-paradise-the-best-movies-for-a-purposeful-life-for-2024/"><u>Pathfinders' Paradise  The Best Movies for a Purposeful Life for 2024</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-tecno-spark-20-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Tecno Spark 20 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-x-fold-2-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo X Fold 2 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-tecno-spark-10-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Tecno Spark 10 Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-y100-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo Y100 5G | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-s17e-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo S17e | Dr.fone</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/2024-approved-maximize-convenience-with-these-advanced-whatsapp-features/"><u>2024 Approved  Maximize Convenience with These Advanced WhatsApp Features</u></a></li>
<li><a href="https://ai-driven-video-production.techidaily.com/new-user-friendly-video-editing-apps/"><u>New User-Friendly Video Editing Apps</u></a></li>
<li><a href="https://smart-video-editing.techidaily.com/in-2024-powerdirector-vs-the-rest-top-alternative-video-editors-for-mobile/"><u>In 2024, PowerDirector vs The Rest Top Alternative Video Editors for Mobile</u></a></li>
<li><a href="https://review-topics.techidaily.com/in-2024-how-to-change-netflix-location-to-get-more-country-version-on-samsung-galaxy-f34-5g-drfone-by-drfone-virtual-android/"><u>In 2024, How to Change Netflix Location to Get More Country Version On Samsung Galaxy F34 5G | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-v27-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo V27 Pro | Dr.fone</u></a></li>
<li><a href="https://youtube-video-recordings.techidaily.com/new-churning-up-channels-top-gear-list/"><u>[New] Churning Up Channels  Top Gear List</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-y02t-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo Y02T | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-t2-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo T2 5G | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-vivo-t2x-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Vivo T2x 5G | Dr.fone</u></a></li>
</ul></div>
