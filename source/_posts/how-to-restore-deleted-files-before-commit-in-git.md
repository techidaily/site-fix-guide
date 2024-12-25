---
title: How to Restore Deleted Files Before Commit in Git
date: 2024-12-20T09:02:08.880Z
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

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/jf0JvOqiAXc?si=kHEHQGC_PhBv4xij" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

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

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/AQn0MYjIfyI?si=rIdjT-qMRpjpJXXa" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

## 3. Restore a Batch of Deleted Files Before Commit in Git

What if we deleted a bunch of files and did not commit? Suppose we deleted 1000 files, and we now want to restore all of them.

![Delete several files](/images/git/how-to-restore-deleted-files-before-commit-in-git/delete-several-files.webp)

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/gMS5pm0SQlQ?si=gasOo6p2agrVlIb7" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

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

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/9sk53d1bBhY?si=yaTeDogLb3D4dYu1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

![All deleted files restored](/images/git/how-to-restore-deleted-files-before-commit-in-git/all-deleted-files-restored.webp)

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/H2cXnI9oOvM?si=3nz2sBB124ln-83T" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

<ins class="adsbygoogle"
    style="display:block"
    data-ad-format="autorelaxed"
    data-ad-client="ca-pub-7571918770474297"
    data-ad-slot="1223367746"></ins>

<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://article-helps.techidaily.com/new-join-the-meme-revolution-expert-tips-for-the-metaverse-for-2024/"><u>[New] Join the Meme Revolution Expert Tips for the Metaverse for 2024</u></a></li>
<li><a href="https://youtube-lab.techidaily.com/ransforming-life-experiences-into-engaging-yt-videos/"><u>[New] Transforming Life Experiences Into Engaging YT Videos</u></a></li>
<li><a href="https://extra-support.techidaily.com/updated-premier-silent-sound-converters/"><u>[Updated] Premier Silent Sound Converters</u></a></li>
<li><a href="https://instagram-clips.techidaily.com/updated-rapidly-rise-with-smart-instagram-reel-techniques-for-2024/"><u>[Updated] Rapidly Rise with Smart Instagram Reel Techniques for 2024</u></a></li>
<li><a href="https://win-blog.techidaily.com/cracking-the-code-resolve-error-80070057-in-call-of-duty-black-ops-cold-war-easily/"><u>Cracking the Code: Resolve Error 80070057 in Call of Duty: Black Ops Cold War Easily</u></a></li>
<li><a href="https://article-posts.techidaily.com/enhancing-game-experience-with-voice-alteration-on-ps45/"><u>Enhancing Game Experience with Voice Alteration on PS4/5</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-part-of-the-touch-screen-not-working-on-meizu-21-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Part of the Touch Screen Not Working on Meizu 21 Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unfortunately-contacts-has-stopped-error-on-tecno-spark-20-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How to Fix Unfortunately, Contacts Has Stopped Error on Tecno Spark 20 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-phone-touchscreen-of-lava-yuva-2-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Phone Touchscreen Of Lava Yuva 2 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-restore-a-bricked-oneplus-nord-n30-5g-back-to-operation-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Restore a Bricked OnePlus Nord N30 5G Back to Operation | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-sony-xperia-5-v-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Sony Xperia 5 V | Dr.fone</u></a></li>
<li><a href="https://mondly-stories.techidaily.com/mastering-french-salutations-the-ultimate-guide-to-bonjour/"><u>Mastering French Salutations: The Ultimate Guide to 'Bonjour'</u></a></li>
<li><a href="https://fix-guide.techidaily.com/proven-ways-to-fix-there-was-a-problem-parsing-the-package-on-itel-p55-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Proven Ways to Fix There Was A Problem Parsing the Package on Itel P55 5G | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/reasons-for-xiaomi-redmi-12-5g-stuck-on-boot-screen-and-ways-to-fix-them-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Reasons for Xiaomi Redmi 12 5G Stuck on Boot Screen and Ways To Fix Them | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/simple-solutions-to-fix-android-systemui-has-stopped-error-for-google-pixel-7a-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Simple Solutions to Fix Android SystemUI Has Stopped Error For Google Pixel 7a | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/solved-warning-camera-failed-on-samsung-galaxy-f34-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Solved Warning Camera Failed on Samsung Galaxy F34 5G | Dr.fone</u></a></li>
<li><a href="https://video-capture.techidaily.com/steps-to-record-voice-memo-on-iphone/"><u>Steps to Record Voice Memo on iPhone</u></a></li>
<li><a href="https://bypass-frp.techidaily.com/the-updated-method-to-bypass-vivo-y78plus-t1-edition-frp-by-drfone-android/"><u>The Updated Method to Bypass Vivo Y78+ (T1) Edition FRP</u></a></li>
<li><a href="https://win11-tips.techidaily.com/unlock-cmd-capabilities-with-these-top-5-hacks/"><u>Unlock Cmd Capabilities with These Top 5 Hacks</u></a></li>
</ul></div>

