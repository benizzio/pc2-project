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


### Compatibility

- [Proton-GE-Custom](https://github.com/GloriousEggroll/proton-ge-custom)
    - Bleeding edge community alternative to proton (to also run with Steam)
- [Heroic Games Launcher](https://heroicgameslauncher.com/)
    - Open source client for for Epic Games Store, with proton integration to run games. Very customizable
- [Lutris](https://lutris.net)
    - Open source client for other stores, also with proton integration. Additional focus on emulation and game preservation


### Editors

- [Xournal++](https://xournalpp.github.io/)
    - PDF editing
- [PDF Arranger](https://github.com/pdfarranger/pdfarranger)
    - PDF merging, splitting and rearranging


### Utilities

#### General

- [Ferdium](https://ferdium.org/)
    - Service aggregation. Can integrate mail services, messaging services, social networks, calendar, AI chatbots, etc. all in one app

#### Accessories

- [Solaar](https://github.com/pwr-Solaar/Solaar) 
    - Linux device manager for Logitech devices

#### Gaming

- [MangoHud](https://github.com/flightlessmango/MangoHud)
    - Overlay for hardware data
- [vkBasalt](https://github.com/DadSchoorse/vkBasalt)
    - Vulkan post processing layer for graphical enhancement - integrates with clients
- [GameMode](https://github.com/FeralInteractive/gamemode)
    - Resource optimization manager at OS/Process level to run games
- [gamescope](https://github.com/ValveSoftware/gamescope)
    - Valve microcompositor for gaming features like:
        - Spoofing resolutions;
        - Upscaling using AMD FidelityFX™ Super Resolution or NVIDIA Image Scaling;
        - Limiting framerates.


## Linux distributions reference

### Gaming distros

Distributions with the objective of a game-centric pc simulating console ease of use

- [ChimeraOS](https://chimeraos.org)
    - Arch based
    - AMD Centric
- [Bazzite](https://bazzite.gg/)
    - Fedora based
    - Built-in support for Nvidia