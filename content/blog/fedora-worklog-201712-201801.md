+++
title = "Fedora December 2017, January 2018 and February 2018 Worklog"
date = "2018-03-01T01:14:53-03:00"
tags = [ "worklog" ]
Categories = [ "Fedora" ]
+++

As I mentioned in my last worklog status post, December and January were slow
months since I have been quite busy working on my master's dissertation +
holidays. Thus, I decided to write this post containing all my Fedora activity
for the past 3 months here.

### Packaging Activities

#### New packages included in Fedora

- python-pyclipper
- golang-github-muesli-smartcrop
- python-booleanoperations
- golang-github-gobuffalo-envy
- godotenv in rawhide

#### Packages that needed some love

Some of the packages I maintain had a few problems either during the Fedora 28 Mass Rebuild or for some other reasons. Also, Igor Gnatenko have been experimenting with removing GCC from Fedora BuildRoot, and some of the packages I maintain were missing BRs. The list is below:

- Added BRs: gcc to rats and fixed failing build
- Added BRs: gcc and gcc-c++ to python-compreffor
- Fixed golang-github-fortytw2-leaktest builds which were breaking in f28 mass rebuild
- Fixed go-i18n builds which were breaking for go 1.10 in rawhide

#### Updates

- Updated Hugo to 0.31.1
- Updated rubygem-pathspec to 0.2.1
- Updated golang-github-fsnotify-fsnotify to 1.4.7
- Updated golang-github-chaseadamsio-goorgeous to 2.0.0
- Updated rubygem-semantic to 1.6.1
- Update rubygem-memfs for post-release due to failing tests on ruby 2.5
- Updated golang-github-spf13-afero to version 1.0.2
- Updated golang-github-eknkc-amber to latest revision
- Updated golang-github-muesli-smartcrop to the latest revision due to ABI incompatibilities with hugo
- Updated revision of golang-github-markmates-inflect
- Updated hugo to 0.36.1
- updated rtv
- updated python-ufo2ft to 1.4.0
- updated python-glyphsLib to 2.2.1
- updated python-cu2qu to 1.4.0
- Updated golang-github-gobuffalo-envy to 1.4.1


#### Other packaging activities

- Became POC of rtv
- Updated python-fontmake review request
- Registered some missing packages in release-monitoring

##### Hugo dependenies

I ofter have problems with Hugo dependencies, since I do not maitain all of them in Fedora. I will dedicate a whole post for this matter soon.

##### Derivative work license discussion

There was an interesting discussion related to python-booleanoperations, where someone questioned the fact that the package used a library which had some restrictions regarding derivative works. We discussed the difference between using a library and performing derivative work on it (these are totally different things). I may dedicate a future post for this topic as well.

### Inftrastructure

I sent a patch to rpkg to change the default .rpmlint on
package repositories to use pkgname.rpmlint instead. This was
totally not my idea though. There was a discussion in the devel
mailing list where some people suggested the change and I
thought it would be a good idea to contribute with the
discussion (by sending the patch).
