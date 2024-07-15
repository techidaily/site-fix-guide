---
title: How to Undo Git Pull
date: 2024-07-14T06:35:52.957Z
tags: 
  - git pull
  - undo
categories: 
  - git
description: TThis tutorial demonstrates undoing a git pull to bring a git repository to a previous state using git hard reset.
keywords: git pull, undo git pull, git hard reset, git reset, git reset hard, git reset to previous commit, git reset to previous state
---

This tutorial demonstrates undoing a git pull to bring a git repository to a previous state using git hard reset.

## Introduction

When you accidentally pull the wrong changes from a remote repository, you can use the following process to undo the git pull and bring the repository to a previous state.

<!-- affiliate ads begin -->
<a href="https://ukaidot.sjv.io/c/5597632/1793237/19578" target="_top" id="1793237"><img src="//a.impactradius-go.com/display-ad/19578-1793237" border="0" alt="" width="1200" height="1200"/></a><img height="0" width="0" src="https://imp.pxf.io/i/5597632/1793237/19578" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->
## Prerequisites

1. Git installed on your system.
2. A terminal to run the commands.
3. A basic understanding of Git.
4. A remote repository to pull the changes from.
5. A local repository to undo the git pull.
6. A text editor to edit the files.
7. A backup of the files before the git pull.
8. A backup of the files after the git pull.
9. A backup of the files after the git pull and the changes you want to keep.
10. A backup of the files after the git pull and the changes you want to discard.
11. A backup of the files after the git pull and the changes you want to discard and the changes you want to keep.

<!-- affiliate ads begin -->
<a href="https://sentrypc.7eer.net/c/5597632/398457/3022" target="_top" id="398457"><img src="//a.impactradius-go.com/display-ad/3022-398457" border="0" alt="www.sentrypc.com" width="980" height="120"/></a><img height="0" width="0" src="https://sentrypc.7eer.net/i/5597632/398457/3022" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->
## Steps to Undo Git Pull

1. Open the terminal on your system.
2. Navigate to the directory where your local repository is located.
3. Run the following command to check the status of your local repository.

```bash
git status
```

4. Run the following command to check the list of commits in your local repository.

```bash
git log
```

5. Run the following command to check the list of changes in your local repository.

```bash
git diff
```

6. Run the following command to check the list of changes in your local repository after the git pull.

```bash
git diff HEAD..FETCH_HEAD
```

7. Run the following command to undo the git pull and bring the repository to a previous state.

```bash
git reset --hard <commit_id>
```

8. Run the following command to check the status of your local repository after the git reset.

```bash
git status
```

9. Run the following command to check the list of commits in your local repository after the git reset.

```bash
git log
```

10. Run the following command to check the list of changes in your local repository after the git reset.

```bash
git diff
```

11. Run the following command to check the list of changes in your local repository after the git reset and the changes you want to keep.

```bash
git diff HEAD..FETCH_HEAD
```

12. Run the following command to check the list of changes in your local repository after the git reset and the changes you want to discard.

```bash
git diff HEAD..FETCH_HEAD
```

13. Run the following command to check the list of changes in your local repository after the git reset and the changes you want to discard and the changes you want to keep.

```bash
git diff HEAD..FETCH_HEAD
```

<ins class="adsbygoogle"
    style="display:block"
    data-ad-format="autorelaxed"
    data-ad-client="ca-pub-7571918770474297"
    data-ad-slot="1223367746"></ins>





<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-y36-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo Y36 | Dr.fone</u></a></li>
<li><a href="https://fake-location.techidaily.com/dose-life360-notify-me-when-someone-checks-my-location-on-oppo-f23-5g-drfone-by-drfone-virtual-android/"><u>Dose Life360 Notify Me When Someone Checks My Location On Oppo F23 5G? | Dr.fone</u></a></li>
<li><a href="https://on-screen-recording.techidaily.com/in-2024-essential-gb-games-selecting-pc-emulators-to-simulate-gba-perfectly/"><u>In 2024, Essential GB Games  Selecting PC Emulators to Simulate GBA Perfectly</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-xiaomi-civi-3-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Xiaomi Civi 3 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-y78plus-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo Y78+ | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-y36i-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo Y36i | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-y17s-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo Y17s | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-xiaomi-14-ultra-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Xiaomi 14 Ultra | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-s17e-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo S17e | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-v29-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo V29 Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-s17t-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo S17t | Dr.fone</u></a></li>
<li><a href="https://discord-videos.techidaily.com/new-top-voip-platforms-face-off-discord-vs-skype-showdown/"><u>[New] Top VoIP Platforms Face-Off  Discord Vs Skype Showdown</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-t2-pro-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo T2 Pro 5G | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-x100-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo X100 Pro | Dr.fone</u></a></li>
<li><a href="https://fox-cloud.techidaily.com/reimagining-photo-presentation-with-top-frame-tools-for-2024/"><u>Reimagining Photo Presentation with Top Frame Tools for 2024</u></a></li>
<li><a href="https://extra-guidance.techidaily.com/red-eye-remover-how-to-remove-red-eye-from-photos-on-iphone-free-for-2024/"><u>Red Eye Remover| How to Remove Red Eye From Photos on iPhone [Free] for 2024</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-s18-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo S18 Pro | Dr.fone</u></a></li>
<li><a href="https://youtube-web.techidaily.com/ed-how-to-find-youtube-collaboration-partners/"><u>[Updated] How to Find YouTube Collaboration Partners?</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-x-flip-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo X Flip | Dr.fone</u></a></li>
<li><a href="https://video-creation-software.techidaily.com/2024-approved-vn-video-editor-for-windows-a-concise-review/"><u>2024 Approved VN Video Editor for Windows A Concise Review</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-y55s-5g-2023-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo Y55s 5G (2023) | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-v30-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo V30 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-v29-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo V29 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-v27-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo V27 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-xiaomi-13t-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Xiaomi 13T Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-x100-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo X100 | Dr.fone</u></a></li>
<li><a href="https://on-screen-recording.techidaily.com/new-premium-screen-recorders-roundup-for-2024/"><u>[New] Premium Screen Recorders Roundup for 2024</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-v27-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo V27 Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-v30-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo V30 Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-y100i-power-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo Y100i Power 5G | Dr.fone</u></a></li>
<li><a href="https://facebook-record-videos.techidaily.com/updated-youtube-shorts-showing-up-after-fix/"><u>[Updated] YouTube Shorts Showing Up After Fix</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-y02t-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo Y02T | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-y27-4g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo Y27 4G | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-xiaomi-13-ultra-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Xiaomi 13 Ultra | Dr.fone</u></a></li>
<li><a href="https://phone-solutions.techidaily.com/free-electronic-signature-for-doc-file-by-ldigisigner-sign-a-word-sign-a-word/"><u>Free electronic signature - For .doc file</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-t2x-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo T2x 5G | Dr.fone</u></a></li>
<li><a href="https://win11-tips.techidaily.com/addressing-inconsistent-thx-sound-on-pcs/"><u>Addressing Inconsistent THX Sound on PCs</u></a></li>
<li><a href="https://smart-video-creator.techidaily.com/updated-2024-approved-fcpx-optimization-tips-and-tricks-to-reclaim-disk-space/"><u>Updated 2024 Approved FCPX Optimization Tips and Tricks to Reclaim Disk Space</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-xiaomi-14-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Xiaomi 14 Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-v30-lite-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo V30 Lite 5G | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-y28-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo Y28 5G | Dr.fone</u></a></li>
<li><a href="https://digital-screen-recording.techidaily.com/updated-2024-approved-videorecordermax-9-in-depth-performance-check/"><u>[Updated] 2024 Approved  VideoRecorderMax 9  In-Depth Performance Check</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-xiaomi-13t-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Xiaomi 13T | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-v27e-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo V27e | Dr.fone</u></a></li>
<li><a href="https://desktop-recording.techidaily.com/updated-in-2024-innovative-practices-for-online-learning-archives/"><u>[Updated] In 2024, Innovative Practices for Online Learning Archives</u></a></li>
<li><a href="https://instagram-video-recordings.techidaily.com/updated-in-2024-enhance-visual-appeal-edit-videos-for-instagram-success/"><u>[Updated] In 2024, Enhance Visual Appeal  Edit Videos for Instagram Success</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-s18-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo S18 | Dr.fone</u></a></li>
<li><a href="https://fox-info.techidaily.com/updated-ultimate-action-camera-guide-exploring-sj-cam-s6s-capabilities/"><u>[Updated] Ultimate Action Camera Guide  Exploring SJ-CAM S6's Capabilities</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-y100i-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo Y100i | Dr.fone</u></a></li>
<li><a href="https://change-location.techidaily.com/in-2024-ultimate-guide-to-get-the-meltan-box-pokemon-go-for-vivo-x-fold-2-drfone-by-drfone-virtual-android/"><u>In 2024, Ultimate guide to get the meltan box pokemon go For Vivo X Fold 2 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-y77t-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo Y77t | Dr.fone</u></a></li>
<li><a href="https://some-approaches.techidaily.com/in-2024-unveiling-mastery-the-ultimate-animoji-guide-for-iphone-x/"><u>In 2024, Unveiling Mastery  The Ultimate Animoji Guide for iPhone X</u></a></li>
<li><a href="https://youtube-videos.techidaily.com/direct-to-device-converting-youtube-tracks-for-idevices/"><u>Direct to Device  Converting YouTube Tracks for iDevices</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unresponsive-touch-screen-on-vivo-t2-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Unresponsive Touch Screen on Vivo T2 5G | Dr.fone</u></a></li>
</ul></div>
