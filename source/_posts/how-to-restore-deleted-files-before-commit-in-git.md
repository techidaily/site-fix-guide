---
title: How to Restore Deleted Files Before Commit in Git
date: 2024-05-19T03:59:03.217Z
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

<ins class="adsbygoogle"
    style="display:block"
    data-ad-format="autorelaxed"
    data-ad-client="ca-pub-7571918770474297"
    data-ad-slot="1223367746"></ins>

<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://fix-guide.techidaily.com/samsung-galaxy-a05s-not-connecting-to-wi-fi-12-quick-ways-to-fix-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Samsung Galaxy A05s Not Connecting to Wi-Fi? 12 Quick Ways to Fix | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-resolve-vivo-y27-5g-screen-not-working-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How to Resolve Vivo Y27 5G Screen Not Working | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/quick-fixes-for-why-is-my-samsung-galaxy-a15-4g-black-and-white-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Quick Fixes for Why Is My Samsung Galaxy A15 4G Black and White | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-stop-my-spouse-from-spying-on-my-poco-x5-pro-drfone-by-drfone-virtual-android/"><u>How to Stop My Spouse from Spying on My Poco X5 Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-phone-touchscreen-of-motorola-razr-40-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Phone Touchscreen Of Motorola Razr 40 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unfortunately-contacts-has-stopped-error-on-xiaomi-redmi-a2-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How to Fix Unfortunately, Contacts Has Stopped Error on Xiaomi Redmi A2 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/spotify-keeps-crashing-a-complete-list-of-fixes-you-can-use-on-motorola-edge-40-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Spotify Keeps Crashing A Complete List of Fixes You Can Use on Motorola Edge 40 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/strategies-for-apps-that-wont-download-from-play-store-on-samsung-galaxy-s23-ultra-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Strategies for Apps That Wont Download From Play Store On Samsung Galaxy S23 Ultra | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/spotify-keeps-crashing-a-complete-list-of-fixes-you-can-use-on-motorola-razr-40-ultra-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Spotify Keeps Crashing A Complete List of Fixes You Can Use on Motorola Razr 40 Ultra | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-meizu-21-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Meizu 21 Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/solved-warning-camera-failed-on-infinix-hot-40-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Solved Warning Camera Failed on Infinix Hot 40 Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-restore-a-bricked-infinix-note-30-5g-back-to-operation-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Restore a Bricked Infinix Note 30 5G Back to Operation | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-unbrick-a-dead-nubia-z50-ultra-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Unbrick a Dead Nubia Z50 Ultra | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/play-store-stuck-on-downloading-of-xiaomi-redmi-a2-7-ways-to-resolve-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Play Store Stuck on Downloading Of Xiaomi Redmi A2? 7 Ways to Resolve | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-revive-your-bricked-samsung-galaxy-a15-4g-in-minutes-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Revive Your Bricked Samsung Galaxy A15 4G in Minutes | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-oppo-k11-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Oppo K11 5G | Dr.fone</u></a></li>
<li><a href="https://screen-mirror.techidaily.com/in-2024-how-oppo-f23-5g-mirror-screen-to-pc-drfone-by-drfone-android/"><u>In 2024, How Oppo F23 5G Mirror Screen to PC? | Dr.fone</u></a></li>
<li><a href="https://review-topics.techidaily.com/mp4-won-t-play-on-my-htc-u23-pro-by-aiseesoft-video-converter-play-mp4-on-android/"><u>MP4 won't play on my HTC U23 Pro</u></a></li>
<li><a href="https://apple-account.techidaily.com/how-to-remove-the-two-factor-authentication-on-iphone-12-pro-by-drfone-ios/"><u>How To Remove the Two Factor Authentication On iPhone 12 Pro</u></a></li>
<li><a href="https://activate-lock.techidaily.com/bypass-activation-lock-from-apple-iphone-x-4-easy-ways-by-drfone-ios/"><u>Bypass Activation Lock From Apple iPhone X - 4 Easy Ways</u></a></li>
<li><a href="https://techidaily.com/how-to-repair-system-issues-of-apple-iphone-6s-plus-drfone-by-drfone-ios-system-repair-ios-system-repair/"><u>How To Repair System Issues of Apple iPhone 6s Plus? | Dr.fone</u></a></li>
<li><a href="https://howto.techidaily.com/what-to-do-if-your-motorola-moto-g23-auto-does-not-work-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>What To Do if Your Motorola Moto G23 Auto Does Not Work | Dr.fone</u></a></li>
<li><a href="https://iphone-unlock.techidaily.com/in-2024-detailed-review-of-doctorsim-unlock-service-for-apple-iphone-se-drfone-by-drfone-ios/"><u>In 2024, Detailed Review of doctorSIM Unlock Service For Apple iPhone SE | Dr.fone</u></a></li>
<li><a href="https://android-frp.techidaily.com/in-2024-ultimate-guide-on-oneplus-ace-2-frp-bypass-by-drfone-android/"><u>In 2024, Ultimate Guide on OnePlus Ace 2 FRP Bypass</u></a></li>
<li><a href="https://techidaily.com/the-easiest-methods-to-hard-reset-nubia-z50s-pro-drfone-by-drfone-reset-android-reset-android/"><u>The Easiest Methods to Hard Reset Nubia Z50S Pro | Dr.fone</u></a></li>
<li><a href="https://fake-location.techidaily.com/wondering-the-best-alternative-to-hola-on-itel-p40-here-is-the-answer-drfone-by-drfone-virtual-android/"><u>Wondering the Best Alternative to Hola On Itel P40? Here Is the Answer | Dr.fone</u></a></li>
</ul></div>


