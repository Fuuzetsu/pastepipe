# A CLI for lpaste.net

Pastepipe reads from stdin, posting to lpaste, and prints out the
resulting url (the last line of output). Parameters control various
hpaste form fields:

```
$ pastepipe --help
PastePipe v1.8, (C) Rogan Creswick 2009-2012, (C) Mateusz Kowalczyk 2014-2015

pastepipe [OPTIONS]

Common flags:
     --user=USER              Your user name
  -l --language=LANGUAGE      The language used for syntax highlighting
  -c --channel=#channel-name  #channel to post your snippet. The lpaste bot
                              will not post the message if you do not set
                              --title=TITLE and --user=<YOUR NICK>
  -t --title=TITLE            The title of the snippet
  -u --uri=URL                The URI of the lpaste instance to post to
  -p --private                Make this a private snippet, off by default
     --test                   Prevents PastePipe from actually posting
                              content, just echos the configuration and input
  -? --help                   Display help message
  -V --version                Print version information
     --numeric-version        Print just the version number
```

It will auto-detect your local username, but --user overrides this detection.

Parameters can come in any order, but only the first of duplicate entries will be used. So, if you have an alias to send to a local hpaste uri, then that alias should effectively disable the --uri switch. It is not possible to "disable" the --test or --help switches in this way, so you can always add --test to a command line to disable the actual sending of content.

# Installation

PastePipe is available on hackage (http://hackage.haskell.org/package/PastePipe) , so you can cabal install it, if you have a working cabal-install.

# Authors / contributors

 - Rogan Creswick
 - Brian Victor
 - Mateusz Kowalczyk
