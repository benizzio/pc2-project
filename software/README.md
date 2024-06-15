# Software

## Basic pack

### Terminal tools

- [oh my zsh](https://ohmyz.sh/)
    - [zaw plugin](https://github.com/zsh-users/zaw)
        - for Ubuntu
            ```zsh
            > cd ~/.oh-my-zsh/plugins
            > git clone git@github.com:zsh-users/zaw.git
            
            # INSIDE ~/.zshrc #########
            # plugins=(git zaw) #or any others
            # 
            # source $ZSH/oh-my-zsh.sh
            # 
            # bindkey '^r' zaw-history
            ###########################

            # restart terminal session!
            ```