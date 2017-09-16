+++
Categories = ["Programming"]
Tags = ["cpanpr", "Perl", "github"]
date = "2015-01-08T16:24:11-03:00"
title = "#cpanpr - January: Vimana"

+++

So my first dist assigned in the [CPAN Pull Request Challenge](http://neilb.org/2014/11/29/pr-challenge-2015.html) is [Vimana](https://github.com/c9s/Vimana).

Vimana is a system for searching and installing vim scripts, both from [vim.org](http://www.vim.org/) and git repositories.

I must confess that I really liked my first distribution, given that I do use Vim every day.

I usually use Pathogen or Vundle to manage my plugins, but since I am working with Vimana this month, I am willing to switch to it.

I still didn't put a lot of work on my assingnment, and am actually thinking about how I can contribute to the project (note that the last commit in there is from 2012).

Trying to follow an [old post](http://darkmattermatters.com/2009/07/16/red-hat-culture-tip-default-to-open/) I read one of these days, I am attaching the first message I sent to the main dist developer. If you are also in the #cpanpr, happy hacking! :)

From: Athos Ribeiro [athoscribeiro@gmail.com](mailto:athoscribeiro@gmail.com)</br>
To: yoanlin93@gmail.com</br>
Subject: Vimana on CPAN PR-Challenge

```
Hello,

Last week Neil Bowers started the CPAN Pull Request Challenge (links in the end of the message). The challenge consists in attributing a random distribution from CPAN (that also must be on github) to each contestant in the beginning of every month of 2015, and each contestant must submit at least one pull request to the project assigned to him/her by the end of the month.

I was assigned to work on Vimana this month and I am contacting you so I can have your opinion on possible contributions I may come up with along the month. I already cloned the repository and ran the test suite provided.

For now I removed the Data::Util dependency from the test suite (does that sound reasonable?), given I could not find the module on Fedora (packaging a rpm later is in my plans) and added some of the files that make crates to the .gitignore.

I was thinking about solving one of the issues in github, updating it's online documentation: https://github.com/c9s/Vimana/issues/14

And maybe adding an info option to the tool, to get detailed information on the scripts as well as the karma for each of them. Do you have any comments on that?

Also, if I do package it to the fedora project (it would be my first package) I would quit Vundle for Vimana, in this sense, do you still use Vimana yourself or have you switched to Pathogen/Vundle approach? The reason I am asking that is because I saw one of your comments in an issue on github where you mention Vundle to one of the users.

You can read more about the Pull Request Challenge at:

http://neilb.org/2014/11/29/pr-challenge-2015.html

and

http://blogs.perl.org/users/neilb/2014/12/take-the-2015-cpan-pull-request-challenge.html

Thank you for your attention,

-- 

Athos Ribeiro
```
