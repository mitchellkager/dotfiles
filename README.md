My personal configuration files.

## Setup

    git clone git@github.com:dbrgn/dotfiles.git ~/.dotfiles


## Vim

Contains many tools for Python development.

### Requirements

 * vim compiled with Python and Ruby support
 * C compiler and Ruby (to build command-t extensions)
 * C++ compiler and Python headers
 * Jedi (https://github.com/davidhalter/jedi)

### Setup

Create symlinks

    ln -s ~/.dotfiles/.vim ~
    ln -s ~/.dotfiles/.vimrc ~

Copy and install powerline fonts

    mkdir -p ~/.fonts/truetype/
    cp ~/.dotfiles/fonts/*.ttf ~/.fonts/truetype/
    fc-cache -fv ~/.fonts

Setup vundle

    git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
    vim +BundleInstall +qall

Update vundle

    vim +BundleInstall! +qall

Configure command-t

    cd ~/.vim/bundle/Command-T/ruby/command-t/
    ruby extconf.rb
    make

Configure YCM

    cd ~/.vim/bundle/YouCompleteMe/
    ./install.sh --clang-comp


## Bash

To use `.bashrc.local`, source it in your regular `.bashrc`:

    source ~/.dotfiles/.bashrc.local


## Other config files

    # screen
    ln -s ~/.dotfiles/.screenrc ~

    # xresources
    ln -s ~/.dotfiles/.Xresources ~

    # xbindkeys
    ln -s ~/.dotfiles/.xbindkeysrc ~

    # xmodmap
    ln -s ~/.dotfiles/.Xmodmap ~
