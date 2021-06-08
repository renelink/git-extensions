# GIT Extensions

This repository contains my (René Link) extensions for git.

- [git stashes](stashes)

## Extension Installation

Install the extensions by copying the files to a folder that is contained in your `PATH` environment variable.

I usually prepend a bin directory in my user home to the `PATH` in my `~/.bash_profile`. E.g.

    PATH=~/bin:${PATH}

After that I usually install all of my extensions by executing

    find "$(pwd)" -type f -name git-* | while read extension ; do ln -s $extension ~/bin/$(basename $extension); done

in this repositories work tree.