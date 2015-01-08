
[[ -s "$HOME/.profile" ]] && source "$HOME/.profile" # Load the default .profile

[[ -s "$HOME/.rvm/scripts/rvm" ]] && source "$HOME/.rvm/scripts/rvm" # Load RVM into a shell session *as a function*

# export PS1="\W \$ "
source ~/.git-prompt.sh
export PS1='\[\n\e[1;34m\][\W]$(__git_ps1)\$\[\e[0m\] '

bind '"\e[A": history-search-backward'
bind '"\e[B": history-search-forward'
export PATH=/usr/local/bin:$PATH
CDPATH=~/Developer

if [ -f `brew --prefix`/etc/bash_completion ]; then
  . `brew --prefix`/etc/bash_completion
fi