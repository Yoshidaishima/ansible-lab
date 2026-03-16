# Things to install and config on rpi
- screen # required by ranger?
- python
- ranger
- dnsutils
- tmux
- vim
- awesomevimrc
- bashrc aliases and functions
- inputrc setup
- kitty
- ranger
- tldr
- ufw


### Python
 git clone https://github.com/pyenv/pyenv.git ~/.pyenv

Add to bash profile:

$ echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile  
$ echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile 

Add pyenv init to your shell to enable shims and autocompletion. Please make sure eval "$(pyenv init -)"is placed toward the end of the shell configuration file since it manipulates PATH during the initialization.

$ echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n eval "$(pyenv init -)"\nfi' >> ~/.bash_profile

Note: There are some systems where the BASH_ENV variable is configured to point to .bashrc. On such systems you should almost certainly put the above mentioned line eval "$(pyenv init -)" into .bash_profile, and not into .bashrc. Otherwise you may observe strange behaviour, such as pyenv getting into an infinite loop. Make sure to check this because of the new ubuntu installation (Jan 2018.)
Restart your shell so the path changes take effect. You can now begin using pyenv.

$ exec "$SHELL"

