+++
title = "Fedora October Worklog"
date = "2017-11-06T16:07:38-02:00"
tags = [ "worklog" ]
Categories = [ "Fedora" ]
+++

This is a list of the activities I have performed as a Fedora Project
contributor in October, 2017. The most time consuming task was related to
[hugo](gohugo.io) maintenance: we finally got hugo packaged in Fedora >= 27 on
its latest version. I decided not to package it into Fedora 26 and under, since
Fedora 27 is almost out and providing a f26 package would require a lot of
extra work.

Here is a list with all the activities:

### Packaging Activities

#### New Packages Included in Fedora
- golang-github-danwakefield-fnmatch
- golang-github-dlclark-regexp2
- golang-github-gorilla-css
- golang-github-andybalholm-cascadia
- golang-github-PuerkitoBio-goquery
- douceur
- golang-github-alecthomas-chroma

#### New Package Review Requests Performed:
- golang-github-Jeffail-gabs
- libnitrokey

#### Packages Updated
- hugo-0.30.2 in rawhide and f27
- flawfinder-2.0.4 in rawhide and f27
- python-firehose-0.5 in rawhide and f27
- golang-github-golang-image in f26
- python-fontMath in rawhide and f27
- python-compreffor in rawhide and f27
- python-defcon in rawhide and f27
- python-mutatormath in rawhide
- golang-github-jdako-prose in f27 and f26

#### Adoptions and co-maintainership
- Adopted rats (it was orphan)
- Adopted flawfinder (previous maintainer needed help with it)
- Added as a co-maintainer of python-firehose

#### release-monitoring
I have checked monitoring status for all my packages in
[release-monitoring](release-monitoring.org), they are all being monitored now.
I also included python-firehose to the monitored projects, since I now
co-maintain this package.

#### fortytw2/leaktest issues
golang-github-fortytw2-leaktest FTBFS. I realized there is a test failing in
aarch64 and opened an [issue
upstream](https://github.com/fortytw2/leaktest/issues/17). I still owe them a
follow up (ENOTIME atm).

#### pyclipper issues
[This review request](https://bugzilla.redhat.com/show_bug.cgi?id=1440971) is
still going on. This month I have assessed the bundled libraries issue and sent
a [pull request upstream to update the bundled library
upstream](https://github.com/greginvm/pyclipper/pull/11). I still need to
investigate some warnings thrown by GCC when compiling from sources. Any help
is welcome.

#### hugo
After realizing I would still need to put some effort into getting hugo ready
for Fedora 26, I gave up building it there, since Fedora 27 is almost out. If
anyone still needs hugo in Fedora 26, consider using Fedora 27 packages or
contact me.

### Meetings attended
I chaired all the October LATAM ambassadors meetings. I will try to keep
attending those, since the quorum seems to have declined lately.
