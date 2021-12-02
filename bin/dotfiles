#! /bin/bash

if ! which rcup >/dev/null; then 
	echo "Fatal: rcm is not installed on this machine"
	exit 1
fi

os_type=$(uname -s)

rm -rf ~/.oh-my-zsh

if [[ -d ~/.dotfiles ]]; then 
	cd ~/.dotfiles
	git pull
else 
	git clone [git@github.com:MarkusAJacobsen/dotfiles.git](git@github.com:MarkusAJacobsen/dotfiles.git) ~/.dotfiles
fi

rcup -f -t $os_type -d ~/.dotfiles
