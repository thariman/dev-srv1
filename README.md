# dev-srv1
Install 14.04.2 LTS from USB
change /etc/apt/sources.list
using local mirror kambing.ui.ac.id
sudo apt-get update
sudo apt-get -y upgrade
sudo apt-get -y dist-upgrade
reboot

#update .bashrc  increase the histsize, save all the history from multiple login
HISTCONTROL=ignoreboth:erasedups

PROMPT_COMMAND="history -a;history -c;history -r;$PROMPT_COMMAND"

# for setting history length see HISTSIZE and HISTFILESIZE in bash(1)
HISTSIZE=10000
HISTFILESIZE=20000

# my tmux.conf   using the same esc ke like screen ( I swap caps lock to control in keyboard )
unbind C-b
bind a send-prefix
set -s escape-time 1
set -g base-index 1
setw -g pane-base-index 1
set -g default-terminal "screen-256color"
setw -g mode-keys vi
set -g history-limit 100000
