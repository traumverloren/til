I use [Laptop](https://github.com/thoughtbot/laptop) to install all required software on a new machine. Like this:

```
$ cd ~
$ curl --remote-name https://raw.githubusercontent.com/thoughtbot/laptop/master/mac
$ sh mac 2>&1 | tee ~/laptop.log
```

* Additionally, I add a laptop.local script to install other packages that I need for projects I work on.  Create a file called `~/.laptop.local`:

```
#!/bin/sh

brew_install_or_upgrade 'mongodb'
brew_install_or_upgrade 'phantomjs'
```

FYI, you can run Laptop again and again, it will keep your machine up to date.

* I also needed to install POW in the terminal:
```
$ curl get.pow.cx | sh
$ cd ~/.pow
$ ln -s ~/Path/to/project/ project-name
```

* Install [Atom](https://atom.io/) as main text editor.
* Install [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) for the terminal.  Seriously, I <3 it!  Easily shows what git branch I'm on, and if I have unsaved git edits.
