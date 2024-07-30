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






