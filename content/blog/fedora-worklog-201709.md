+++
title = "Fedora September Work Log"
date = "2017-10-02T16:34:20-03:00"
tags = [ "worklog" ]
Categories = [ "Fedora" ]
+++

- Hugo review is finally over. It is already in rawhide and I will try to push it
to f27 before the final release is out. Thanks for everyone that helped with
all the (never ending) reviews.
- Joined the x86 SIG and built the kernel applying a specific patch on it to
  make sure a specific bug was fixed.

Here are my raw notes:

### 2017-09-06:
- First review on golang-github-golang-sync
- input on https://pagure.io/ambassadors-latam/tasks/issue/424
- rubygem-pathspec updated
- updated review request on python-setuptools_scm_git_archive
- Participated on the first x86 SIG meeting

### 2017-09-07:
- Reviewed golang-github-golang-sync package
- Reviewed golang-github-billziss-gh-cgofuse

### 2017-09-08:
- Joined FESCo meeting to discuss the approval of the x86 SIG

### 2017-09-09:
- Helped the x86 SIG to solve a kernel building problem
  -- Applied an upstream patch and built the kernel in COPR for i686

### 2017-09-10:
- sent an email the x86 SIG about the kernel building problem
- Added my name to the x86 SIG group
- Requested the golang-github-neurosnap-sentences rawhide repository

### 2017-09-11:
- Built golang-github-neurosnap-sentences in rawhide
- fixed issues on golang-github-jdkato-prose review request (sent a patch upstream)

### 2017-09-12:
- Requested golang-github-jdkato-prose repository
- Requested python-setuptools_scm_git_archive repository
- Built golang-github-jdkato-prose in rawhide
- Built python-setuptools_scm_git_archive in rawhide
- Sent a PR to update golang-github-russross-blackfriday package in rawhide for Hugo

### 2017-09-15:
- chaired latam meeting
- Hugo review was approved.
- requested branches for rawhide, f27 and f26
- built hugo for rawhide
- Requested the following repositories in both f27 and f26:
  - golang-github-jdkato-syllables
  - golang-github-shogo82148-go-shuffle
  - golang-github-montanaflynn-stats
  - golang-github-markbates-inflect
  - golang-github-golang-image
  - golang-github-neurosnap-sentences
  - golang-github-jdkato-prose
  - hugo
- Built golang-github-jdkato-syllables for f26 (f27 was already built)
- Sent update for golang-github-jdkato-syllables for f26
- Built golang-github-shogo82148-go-shuffle for f27
- sent update for golang-github-shogo82148-go-shuffle for f27
- Built golang-github-shogo82148-go-shuffle for f26
- sent update for golang-github-shogo82148-go-shuffle for f26
- Built golang-github-montanaflynn-stats for f27
- Built golang-github-montanaflynn-stats for f26
- Built golang-github-markbates-inflect for f27
- Built golang-github-markbates-inflect for f26
- Sent update for golang-github-montanaflynn-stats for f27
- Sent update for golang-github-montanaflynn-stats for f26
- Built golang-github-golang-image for f27
- Sent an update for golang-github-markbates-inflect for f27
- Sent an update for golang-github-markbates-inflect for f26
- Built golang-github-neurosnap-sentences for f27
- Built golang-github-neurosnap-sentences for f26
- Sent an update for golang-github-golang-image for f27
- Sent and update for golang-github-neurosnap-sentences for f27
- Sent and update for golang-github-neurosnap-sentences for f26

### 2017-09-20:
- Updated go-i18n in rawhide
- Built go-i18n for f27
- Updated rubygem-chake in rawhide
- Updated rubygem-chake to comply with new ruby packaging guidelines
- Reverted the changes from chake (above) since it requires a git repo
- Started python-xappy review process
- Started cverna packager sponsoring process

### 2017-09-21:
- pushed golang-github-shogo82148-go-shuffle to f27 stable
- pushed golang-github-montanaflynn-stats to f27 stable
- pushed golang-github-markbates-inflect to f27 stable
- pushed golang-github-golang-image to f27 stable
- pushed golang-github-neurosnap-sentences to f27 stable
- Commented on cverna review request

### 2017-09-22:
- Chaired latam meeting

### 2017-09-24:
- Pushed golang-github-shogo82148-go-shuffle to f26 stable
- Pushed golang-github-montanaflynn-stats to f26 stable
- Pushed golang-github-markbates-inflect to f26 stable
- Pushed golang-github-neurosnap-sentences to f26 stable
- Pushed golang-github-jdkato-syllables to f26 stable
- Requested pushing go-i18n to stable

### 2017-09-25:
- Commented on cverna review request

### 2017-09-29:
- Chaired latam meeting

### 2017-09-30:
- Built golang-github-jdako-prose for f27
- Sent and update for golang-github-jdako-prose for f27
- Built golang-github-jdako-prose for f26
- Sent and update for golang-github-jdako-prose for f26
