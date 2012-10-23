My personal configuration files.

## Setup

 1. git clone git://github.com/gwrtheyrn/dotfiles.git ~/.dotfiles
 2. git submodule init
 3. git submodule update
 4. git submodule foreach git submodule init
 5. git submodule foreach git submodule update

## Vim

Contains many tools for Python development.

### Setup

 1. ln -s ~/.dotfiles/.vim ~
 2. ln -s ~/.dotfiles/.vimrc ~
 3. vim +BundleInstall +
 4. cd ~/.dotfiles/.vim/bundle/Command-T/ruby/command-t/
 5. ruby extconf.rb
 6. make

### Requirements

 * vim compiled with Python and Ruby support
 * C compiler (to build command-t extensions)

## Bash

To use `.bashrc.local`, source it in your regular `.bashrc`:

    source ~/.dotfiles/.bashrc.local

## Screen

 1. ln -s ~/.dotfiles/.screenrc ~
