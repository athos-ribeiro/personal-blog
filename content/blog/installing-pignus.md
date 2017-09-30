+++
title = "Installing Pignus On a Raspberry Pi 1 Model B"
date = "2017-09-30T13:38:41-03:00"
tags = [ "Raspberry Pi", "Pignus" ]
Categories = [ "Fedora" ]
+++

I have an "old" Raspberry Pi at home which I bought a few years ago and I
decided to use it to backup some of my files, since my laptop is qute old at
the moment and I am afraid its hard drive will fail at any moment now.

Since I run Fedora in all my machines, I wanted to run Fedora in the raspberry
Pi as well. Unfortunately, as per the [Fedora ARM support wiki
page](https://fedoraproject.org/wiki/Architectures/ARM/Raspberry_Pi?rd=Raspberry_Pi),
older Raspberry Pi models are not supported. Fortunately, the wiki page points old
Raspberry owners to the [Pignus](https://pignus.computer) homepage. Pignus is
an attempt to continue the work from the Pidora guys, which tries to run Fedora in
a Raspberry Pi. Let's say Pignus is a Fedora based distro for old raspberries.

All I needed to do was to insert my old (2GB) SD card in my laptop, unmount it

```
# umount /dev/mmcblk1p1
```

and decompress the pignus image in it

```
# wget 'https://pignus.computer/pub/linux/pignus/releases/23/images/pignus-minimal-23a.xz'
# xzcat pignus-minimal-23a.xz >/dev/mmcblk1
```

While decompressing the image in my SD card, I got the following error message

```
# xzcat: (stdout): Write error: No space left on device
```

Because the partition size created for the image was larger than my SD card. We
don't have to worry about that, sice the real size of the decompressed image is
less than 1GB. All we have to do is resize the partition in the SD card.


```
# e2fsck -f /dev/mmcblk1p2
e2fsck 1.43.4 (31-Jan-2017)
The filesystem size (according to the superblock) is 499968 blocks
The physical size of the device is 419072 blocks
Either the superblock or the partition table is likely to be corrupt!
Abort<y>? no
Pass 1: Checking inodes, blocks, and sizes
Pass 2: Checking directory structure
Pass 3: Checking directory connectivity
Pass 4: Checking reference counts
Pass 5: Checking group summary information
_/: 25585/125184 files (0.1% non-contiguous), 204080/499968 blocks
# resize2fs /dev/mmcblk1p2
resize2fs 1.43.4 (31-Jan-2017)
Resizing the filesystem on /dev/mmcblk1p2 to 419072 (4k) blocks.
The filesystem on /dev/mmcblk1p2 is now 419072 (4k) blocks long.
```
Ii is also nice to copy your ssh credentials to the Raspberry, as pointed in
Pignus website

```
# mkdir /mnt/root/.ssh
# cat /home/YOUR_USERNAME/.ssh/id_rsa.pub > /mnt/root/.ssh/authorized_keys
# sync
# umount /mnt
```

Note that you need to run the commands above as root.

Next, I will check if I can run [syncthing](https://syncthing.net/) in this
Raspberry so I can keep my backups in an external hard drive pluged in it.
