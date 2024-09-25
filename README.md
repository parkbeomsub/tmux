vi tmax.conf
# tmux
# sysnchronize-pane 을  y로
bind-key y set-window-option synchronize-panes
# remap prefix from 'C-b' to 'C-a'
unbind C-b
set-option -g prefix C-a
bind-key C-a send-prefix

# 생성하기  - : 가로  \ 세로
# split panes using | and -
bind | split-window -h
bind - split-window -v
unbind '"'
unbind %

## alt누른뒤 방향키  패널변경
bind -n M-Left select-pane -L
bind -n M-Right select-pane -R
bind -n M-Up select-pane -U
bind -n M-Down select-pane -D

## 마우스 모드   컨트롤 a [
set -g mouse on


-----
tmux source-file tmux.conf
