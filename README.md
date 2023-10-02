Ö1 Downloader
==============

This is a program to download broadcasts of the Austrian
public radio program Ö1. The radio offers an amazing collection
of its own productions, hence this program.

I hope that the program is very intuitive and that the random user
will find it easy to use. In fact, usability has always been my
primary goal.

Portability
-----------

This program is implemented in POSIX shell and will work on any
POSIX platform. It has been, however, only tested on Linux, but
should work without problems on a Mac for instance. Please report
any issues and I will do my best to fix them. The Windows users
should have a POSIX shell program installed (there used to be
some, but I'm not sure what is the current situation).

The program depends on the following external programs:

    jq curl id3v2

They are available on a typical Linux platform such as Debian
Linux. Otherwise, YMMV.

NB: I challenge you to implement this in Python or Perl or AWK
or whatever programming language. Note that the usage have to
remain the same!

Implementation details
-----------

The technicalities are plenty and I will leave that out.
`man(1)` is your friend. To run the program in the so-called dry
mode, just use `-n`.

Usage
-----

    usage: /home/dejan/bin/oe1 [-ldqnh] [<day>] [<search>]

    day: day of the week, such as Tue or 20180115 [default: . (whole week)]
    search: what to look for (regular expression or id) [default: .]

    -l: only list features found
    -d: download features
    -h: print this help message
    -q: be quiet
    -n: dry-run, show what would be done, but don't do it

    Examples

    List all features:
        $ oe1
    List today's schedule:
        $ oe1 today
    List last Sunday's features about culture:
        $ oe1 sun kultur
    Download the "Im Gespräch" from last Thursday:
        $ oe1 thu im.gespr.ch

