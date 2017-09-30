+++
title = "Porting noturno to WebExtensions"
date = "2017-09-25T15:48:31-03:00"
tags = [ "noturno", "Firefox", "Proxy" ]
Categories = [ "Programming" ]
+++

About a year ago, I decided to write
[noturno](https://addons.mozilla.org/en-US/firefox/addon/noturno/) a Firefox
extension to toggle proxy configurations on/off, since it used to be really
boring to do that on Firefox (too many clicks needed) and I knew no other
extensions to do that.

Now, over a year later, I have heard that there are a couple extensions that
can do that (and many other things), meaning that noturno is a little behind
compared to these other extensions.

By the time I started writing noturno, [Mozilla was announcing its plans for
supporting
WebExtensions](https://blog.mozilla.org/addons/2015/08/21/the-future-of-developing-firefox-add-ons/),
which would allow us write portable browser extensions. At that time, there was
no support for a proxy API in Mozilla's WebExtensions implementation, so I
decided to use their old SDK, which was not that old back then.

A few months later, Mozilla announced its plans to drop support for the SDK
after Firefox 57, so I needed to either drop noturno, or port it to
WebExtensions. Since it is a simple (and very small) extension and there is (a
small) user base, I decided to re-write noturno using the new API.

It is important to note that the WebExtensions proxy API is completely
different from the SDK proxy API: the former uses [Proxy Auto-Configuration
files](https://developer.mozilla.org/en-US/docs/Web/HTTP/Proxy_servers_and_tunneling),
while, with the latter, we could actually access Firefox internal
configurations. This means that noturno >= 1.0, the versions using
WebExtensions, deprecated noturno former feature, which would toggle between
using custom proxy configurations or no configurations at all, for a new
feature: It asks the user for a proxy host, port and protocol and the user can
switch between using that one proxy or not using a proxy at all.

My future plans for noturno are:

* Improving android support
* Supporting multiple proxy configurations
* Porting noturno to other browsers

noturno is Free Software, licensed under GPLv3, and its development is hosted
in github, at
[github.com/athos-ribeiro/noturno](https://github.com/athos-ribeiro/noturno)

