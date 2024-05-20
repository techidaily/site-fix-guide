---
title: How to Undo Git Pull
date: 2024-05-19T03:59:04.389Z
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
<li><a href="https://fix-guide.techidaily.com/how-to-hidefake-snapchat-location-on-your-tecno-phantom-v-flip-drfone-by-drfone-virtual-android/"><u>How to Hide/Fake Snapchat Location on Your Tecno Phantom V Flip | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/proven-ways-to-fix-there-was-a-problem-parsing-the-package-on-nokia-xr21-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Proven Ways to Fix There Was A Problem Parsing the Package on Nokia XR21 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unfortunately-contacts-has-stopped-error-on-lava-yuva-3-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How to Fix Unfortunately, Contacts Has Stopped Error on Lava Yuva 3 Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/simple-solutions-to-fix-android-systemui-has-stopped-error-for-tecno-camon-20-pro-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Simple Solutions to Fix Android SystemUI Has Stopped Error For Tecno Camon 20 Pro 5G | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/proven-ways-to-fix-there-was-a-problem-parsing-the-package-on-xiaomi-civi-3-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Proven Ways to Fix There Was A Problem Parsing the Package on Xiaomi Civi 3 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-unfortunately-contacts-has-stopped-error-on-lava-blaze-2-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How to Fix Unfortunately, Contacts Has Stopped Error on Lava Blaze 2 5G | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-teleport-your-gps-location-on-tecno-spark-20-proplus-drfone-by-drfone-virtual-android/"><u>How To Teleport Your GPS Location On Tecno Spark 20 Pro+? | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/in-2024-how-to-sharefake-location-on-whatsapp-for-xiaomi-redmi-note-12t-pro-drfone-by-drfone-virtual-android/"><u>In 2024, How to Share/Fake Location on WhatsApp for Xiaomi Redmi Note 12T Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/simple-solutions-to-fix-android-systemui-has-stopped-error-for-oppo-a38-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Simple Solutions to Fix Android SystemUI Has Stopped Error For Oppo A38 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-part-of-the-touch-screen-not-working-on-lava-blaze-2-pro-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Part of the Touch Screen Not Working on Lava Blaze 2 Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/in-2024-how-to-change-tecno-camon-30-pro-5g-location-on-skout-drfone-by-drfone-virtual-android/"><u>In 2024, How to Change Tecno Camon 30 Pro 5G Location on Skout | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/simple-solutions-to-fix-android-systemui-has-stopped-error-for-nokia-c12-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Simple Solutions to Fix Android SystemUI Has Stopped Error For Nokia C12 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-resolve-xiaomi-redmi-note-12-pro-5g-screen-not-working-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How to Resolve Xiaomi Redmi Note 12 Pro 5G Screen Not Working | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/solved-warning-camera-failed-on-nokia-c210-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Solved Warning Camera Failed on Nokia C210 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/nokia-c12-plus-screen-unresponsive-heres-how-to-fix-it-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Nokia C12 Plus Screen Unresponsive? Heres How to Fix It | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-resolve-motorola-moto-g04-screen-not-working-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How to Resolve Motorola Moto G04 Screen Not Working | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/simple-solutions-to-fix-android-systemui-has-stopped-error-for-nokia-c22-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Simple Solutions to Fix Android SystemUI Has Stopped Error For Nokia C22 | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-use-life360-on-windows-pc-for-honor-90-lite-drfone-by-drfone-virtual-android/"><u>How to Use Life360 on Windows PC For Honor 90 Lite? | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/in-2024-top-7-skype-hacker-to-hack-any-skype-account-on-your-infinix-note-30-pro-drfone-by-drfone-virtual-android/"><u>In 2024, Top 7 Skype Hacker to Hack Any Skype Account On your Infinix Note 30 Pro | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/itel-a60s-screen-unresponsive-heres-how-to-fix-it-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Itel A60s Screen Unresponsive? Heres How to Fix It | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/solved-warning-camera-failed-on-motorola-edgeplus-2023-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Solved Warning Camera Failed on Motorola Edge+ (2023) | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-fix-part-of-the-touch-screen-not-working-on-poco-m6-pro-4g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Fix Part of the Touch Screen Not Working on Poco M6 Pro 4G | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-restore-a-bricked-vivo-s18-back-to-operation-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Restore a Bricked Vivo S18 Back to Operation | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/itel-p55-5g-stuck-on-screen-finding-solutions-for-stuck-on-boot-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Itel P55 5G Stuck on Screen – Finding Solutions For Stuck on Boot | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/spotify-keeps-crashing-a-complete-list-of-fixes-you-can-use-on-oppo-reno-8t-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Spotify Keeps Crashing A Complete List of Fixes You Can Use on Oppo Reno 8T 5G | Dr.fone</u></a></li>
<li><a href="https://fix-guide.techidaily.com/how-to-revive-your-bricked-poco-c50-in-minutes-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How To Revive Your Bricked Poco C50 in Minutes | Dr.fone</u></a></li>
<li><a href="https://android-location-track.techidaily.com/in-2024-5-ways-to-track-nokia-c12-without-app-drfone-by-drfone-virtual-android/"><u>In 2024, 5 Ways to Track Nokia C12 without App | Dr.fone</u></a></li>
<li><a href="https://ai-editing-video.techidaily.com/new-top-10-free-whatsapp-video-converter-2023/"><u>New Top 10 Free WhatsApp Video Converter 2023</u></a></li>
<li><a href="https://ai-vdieo-software.techidaily.com/2024-approved-blur-photo-backgrounds-for-free-top-online-editors/"><u>2024 Approved Blur Photo Backgrounds for Free Top Online Editors</u></a></li>
<li><a href="https://review-topics.techidaily.com/in-2024-does-airplane-mode-turn-off-gps-location-on-oneplus-nord-3-5g-drfone-by-drfone-virtual-android/"><u>In 2024, Does Airplane Mode Turn off GPS Location On OnePlus Nord 3 5G? | Dr.fone</u></a></li>
<li><a href="https://location-social.techidaily.com/in-2024-how-to-pause-life360-location-sharing-for-poco-c55-drfone-by-drfone-virtual-android/"><u>In 2024, How To Pause Life360 Location Sharing For Poco C55 | Dr.fone</u></a></li>
<li><a href="https://ai-editing-video.techidaily.com/updated-how-to-edit-text-in-premiere-pro/"><u>Updated How to Edit Text in Premiere Pro</u></a></li>
<li><a href="https://easy-unlock-android.techidaily.com/rootjunky-apk-to-bypass-google-frp-lock-for-poco-f5-pro-5g-by-drfone-android/"><u>Rootjunky APK To Bypass Google FRP Lock For Poco F5 Pro 5G</u></a></li>
<li><a href="https://android-unlock.techidaily.com/in-2024-unlock-your-oppo-reno-11-pro-5g-phone-with-ease-the-3-best-lock-screen-removal-tools-by-drfone-android/"><u>In 2024, Unlock Your Oppo Reno 11 Pro 5G Phone with Ease The 3 Best Lock Screen Removal Tools</u></a></li>
<li><a href="https://change-location.techidaily.com/how-to-fix-error-495-while-downloadupdating-android-apps-on-infinix-note-30-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>How to Fix Error 495 While Download/Updating Android Apps On Infinix Note 30 | Dr.fone</u></a></li>
<li><a href="https://screen-mirror.techidaily.com/in-2024-how-oneplus-ace-2-pro-mirror-screen-to-pc-drfone-by-drfone-android/"><u>In 2024, How OnePlus Ace 2 Pro Mirror Screen to PC? | Dr.fone</u></a></li>
<li><a href="https://ai-video-apps.techidaily.com/updated-top-rated-image-to-video-makers-free-and-paid-solutions/"><u>Updated Top-Rated Image to Video Makers Free and Paid Solutions</u></a></li>
<li><a href="https://ai-vdieo-software.techidaily.com/updated-avi-video-trimming-made-easy-16-best-tools-for-windows-mac-and-android-devices/"><u>Updated AVI Video Trimming Made Easy 16 Best Tools for Windows, MAC, and Android Devices</u></a></li>
<li><a href="https://ai-video-editing.techidaily.com/new-the-actual-discussion-is-regarding-the-splitting-of-the-video-by-using-the-vsdc-also-recommendation-of-using-wondershare-filmora-as-the-better-substitut/"><u>New The Actual Discussion Is Regarding the Splitting of the Video by Using the VSDC. Also, Recommendation of Using Wondershare Filmora as the Better Substitute in Place of VSDC</u></a></li>
<li><a href="https://ios-unlock.techidaily.com/in-2024-what-does-jailbreaking-iphone-15-pro-i-do-get-answers-here-by-drfone-ios/"><u>In 2024, What Does Jailbreaking iPhone 15 Pro i Do? Get Answers here</u></a></li>
<li><a href="https://apple-account.techidaily.com/in-2024-tips-and-tricks-for-apple-id-locked-issue-on-apple-iphone-14-pro-by-drfone-ios/"><u>In 2024, Tips and Tricks for Apple ID Locked Issue On Apple iPhone 14 Pro</u></a></li>
<li><a href="https://iphone-unlock.techidaily.com/in-2024-apple-iphone-13-pro-max-asking-for-passcode-after-ios-1714-update-what-to-do-drfone-by-drfone-ios/"><u>In 2024, Apple iPhone 13 Pro Max Asking for Passcode after iOS 17/14 Update, What to Do? | Dr.fone</u></a></li>
<li><a href="https://android-unlock.techidaily.com/in-2024-how-to-remove-forgotten-pin-of-your-vivo-x90s-by-drfone-android/"><u>In 2024, How to Remove Forgotten PIN Of Your Vivo X90S</u></a></li>
<li><a href="https://animation-videos.techidaily.com/new-ways-you-can-master-to-find-10-best-free-animated-text-generator-for-2024/"><u>New Ways You Can Master to Find 10 Best Free Animated Text Generator for 2024</u></a></li>
<li><a href="https://android-location.techidaily.com/in-2024-10-free-location-spoofers-to-fake-gps-location-on-your-nokia-105-classic-drfone-by-drfone-virtual/"><u>In 2024, 10 Free Location Spoofers to Fake GPS Location on your Nokia 105 Classic | Dr.fone</u></a></li>
<li><a href="https://ai-vdieo-software.techidaily.com/edit-without-limits-the-top-10-free-online-video-editors/"><u>Edit Without Limits The Top 10 Free Online Video Editors</u></a></li>
<li><a href="https://techidaily.com/how-do-i-reset-my-poco-m6-pro-4g-phone-without-technical-knowledge-drfone-by-drfone-reset-android-reset-android/"><u>How do I reset my Poco M6 Pro 4G Phone without technical knowledge? | Dr.fone</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-repair-a-damaged-video-file-of-realme-narzo-n53-using-video-repair-utility-on-mac-by-stellar-video-repair-mobile-video-repair/"><u>How to Repair a Damaged video file of Realme Narzo N53 using Video Repair Utility on Mac?</u></a></li>
<li><a href="https://fake-location.techidaily.com/thinking-about-changing-your-netflix-region-without-a-vpn-on-tecno-spark-go-2023-drfone-by-drfone-virtual-android/"><u>Thinking About Changing Your Netflix Region Without a VPN On Tecno Spark Go (2023)? | Dr.fone</u></a></li>
</ul></div>


