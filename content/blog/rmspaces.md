+++
Tags = [
  "Development",
  "perl",
  "CPAN",
]
Categories = [
  "Development",
]
menu = "main"
title = "rmspaces - Removing spaces from file names"
date = "2017-08-01T15:20:53-03:00"
Description = ""

+++

There are a few things that usually annoy me when working with people with no
technical background:

**HTML emails:** These are almost becoming the default for marketing emails.
Apparently, we cannot go back to the good old plain text emails anymore. It is
OK for marketing campaigns, but people should not assume everyone is always
able to read HTML emails all the time. I like to use [mutt](www.mutt.org) to
read my emails, so This is what I see when you send me an HTML email:

![A HTML email](https://ar.dev.br/images/html_email.png)

Really, if you do not need to send HTML in your message, make sure your email
client is set to send plain text messages. I tend to ignore emails in HTML,
since it takes time for me to read the message. There was even an [ASCII Ribbon
Campaign](https://web.archive.org/web/20111101072615/http://www.asciiribbon.org/)
advocating that email should only be sent in plain text, which later was [shut
down](https://web.archive.org/web/20130725042359/http://www.asciiribbon.org/)
since people does not seem to care about it - most email clients support (the
bigger) HTML emails anyway.

**MS Office files:** People insist in assuming anyone does have a MS Office
suite in their machines, hence they can open .doc, .docx, and all the other MS
Office files formats. This is not true and a MS Office suite is not cheap at
all in developing countries (although a lot of people I know have unofficial
copies of the MS Office suite).

If one needs to share a document, and does not need the other part to edit such
document, one should share it in an open format (if you still believe the MS
format is open, you should visit the [Document Foundation
website](https://www.documentfoundation.org/) and let them know!) like PDF. If
editions are expected, the [Open Document
Format](https://en.wikipedia.org/wiki/OpenDocument) is the way to go: people
can open your document in a wide variety of software programs, including MS
Word (win-win).

**Files with spaces in their names:** This is quite common for people not used
to working in the command line. We cannot blame them: it is natural to add a
space in file names when using a GUI, maybe they even look cleaner this way.
The problem is that this can be annoying if you are working in the command
line.

Let's say you have a directory with 3 files:

* chocolate chip cookies recipe.txt
* master thesis.pdf
* readme

If you are not used to unix systems, you should know that file extensions are
only used to help whoever is looking at the file names to have an idea on what
they are looking at (this is not true in Windows). So, it is common to see a
lot of files without extensions around linux systems (I do taht for plain text
files).

When listing the directory mentioned above in the command line, one would get:

```
$ ls
chocolate chip cookies recipe.txt   master thesis.pdf   readme
```

As you can see, there are extra spaces between file names, but still, it is
hard to know when one file starts and the other ends. It is so much simpler if
instead of spaces, those files were named with dashes or underscores:

```
$ ls
chocolate_chip_cookies_recipe.txt   master_thesis.pdf   readme
```

This way I know for sure that I have 3 files in my directory and I also know
their names.

also, let's say I want to remove one of the files with spaces in their names. I
would have to escape the spaces in the command line, so `rm` will understand
the file name as a single parameter.

```
$ ls
chocolate chip cookies recipe.txt   master thesis.pdf   readme
$ rm chocolate\ chip\ cookies\ recipe.txt
```

So now it is easier to understand why I do not like spaces in file names (and I
have this feeling that other linux users hate it as well).

That is why I wrote a simple script to remove those anoying, lame, awful spaces
from file names.

[rmspaces](https://github.com/athos-ribeiro/rmspaces) is a command line tool
which receives a list of files as parameter and substitutes spaces for
underscores whenever spaces are found, moving the files to a better place :)

rmspaces can also be used to change multiple file names by using the --target
and the --separator arguments. For example, if you have

```
$ ls
march_report  march_status  march_updates
```

`rmspaces -t march -s 032017 *`

would move the files in the current directory to:

```
$ ls
032017_report  032017_status  032017_updates
```

You can check `rmspaces --help` for more information or check the docstrings in
the source code.

rmspaces is licensed under the GNU General Public Licence (GPLv3) and is
published in CPAN under
[App-rmspaces](http://search.cpan.org/~athos/App-rmspaces/). You can check the
README file in the [github
repository](https://github.com/athos-ribeiro/rmspaces) for information on how
to install or contribute to the code.
