+++
Categories = ["Programming"]
Tags = ["noturno", "Firefox", "Proxy"]
date = "2016-02-02T16:31:35-03:00"
title = "noturno: a Firefox Add-on to turn proxy configurations on/off"

+++



Sometimes I need to download some scientific papers, but I can only download them from the University. That's one of the reasons why Universities should provide internet proxies for the staff/students. Fortunately, University of São Paulo (I am a graduate student there) does provide one.

While setting proxy configurations in Firefox is pretty straight forward, switching these configurations on/off may get a little boring if you need to constantly do it.

Since I could not find an add-on which could provide me a button or hotkey to perform that task, I wrote **noturno**: an add-on to turn your proxy configurations on/off.

**noturno** just adds a button on the top right corner of your browser: whenever the button is **grey**, the proxy configurations are **off** (Firefox default), if it is **green**, the proxy configurations are **on**.

**noturno** is Free Software, licensed under the GPLv3.

https://addons.mozilla.org/en-US/firefox/addon/noturno/

source code: http://github.com/athos-ribeiro/noturno

Note that this is just a simple script written in JS, in the future I intend to give better support to android and handle multiple proxy configurations. For now, it is enough to help me download my papers :)

