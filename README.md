# My Tmux Conf

## how the conf is organized

1. put this in ~/.tmux.conf
```

# ~/.tmux.conf
source ~/.config/tmux/base.conf      # 基础配置
source ~/.config/tmux/keybindings.conf  # 快捷键定义
source ~/.config/tmux/plugins.conf
source ~/.config/tmux/theme.conf     # 主题和样式






# keep tpm work, it must be at the very bottom
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'
# Other examples:
# set -g @plugin 'github_username/plugin_name'
# set -g @plugin 'git@github.com/user/plugin'
# set -g @plugin 'git@bitbucket.com/user/plugin'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run '~/.tmux/plugins/tpm/tpm' 
```

2. download this repo to ~/.config/tmux/


##  Dependencies
### Python
#### libtmux
```bash
python3 -m pip install --user libtmux
# or you can just download the whl file, and install.
wget https://files.pythonhosted.org/packages/13/f5/742db15973ee604b6861a8c92df44a900c88fcd1abd041161dd37371764f/libtmux-0.46.1-py3-none-any.whl
```
required by 
1. ofirgall/tmux-window-name
