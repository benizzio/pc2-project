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

- [jpegoptim](https://github.com/tjko/jpegoptim)
    - Optimizations on jpeg images (e.g. compression)
    - for Ubuntu
        ```zsh
        > sudo apt install jpegoptim
        
        # compress example:
        > jpegoptim --max=50 ./*.jpg #50% compression
        ```

- [Miller](https://github.com/johnkerl/miller)
    - File conversion, most importantly, Json <-> CSV

- [gImageReader](https://github.com/manisandro/gImageReader)
    - OCR from Image PDFs
    - for Ubuntu
        ```zsh
        > sudo apt install gimagereader tesseract-ocr
        
        # compress example:
        > jpegoptim --max=50 ./*.jpg #50% compression
        ```
    - [Language packages](https://packages.debian.org/source/sid/tesseract-lang)
        - for Ubuntu
            ```zsh
            # example (portuguese)
            > sudo apt install tesseract-ocr-por
            ```


### Security

- [Cryptomator](https://cryptomator.org/)
    - Filesystem encryption on demand, ideal for cloud

### Editors

- [Xournal++](https://xournalpp.github.io/)
    - PDF editing

- [PDF Arranger](https://github.com/pdfarranger/pdfarranger)
    - PDF merging, splitting and rearranging


### Utilities

- [Ferdium](https://ferdium.org/)
    - Service aggregation. Can integrate mail services, messaging services, social networks, calendar, AI chatbots, etc. all in one app
- [Solaar](https://github.com/pwr-Solaar/Solaar) 
    - Linux device manager for Logitech devices