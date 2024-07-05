# Software

- [General confis quick guide](config.md)
- [Personal confis quick guide](personal/config.md)

## Basic pack

### Boot + OS utilities

- [Ventoy](https://www.ventoy.net/en/index.html)
    -  Single boot thumbdrive creation for multiple ISOs


### Distro specific

#### Arch

- [rua](https://github.com/vn971/rua)
    - great AUR helper made in rust

### Terminal tools

- [oh my zsh](https://ohmyz.sh/)
    - Config quickref:
        - best way to add variables to PATH
            ```zsh
            # INSIDE ~/.zshrc #########
            # # ADD TO path examples
            #
            # # append
            # path+=('/home/david/pear/bin')
            #
            # #or prepend
            # path=('/home/david/pear/bin' $path)
            #
            # #export to sub-processes (make it inherited by child processes)
            # export PATH
            ###########################

            > source .zshrc
            ```

    - [zaw plugin](https://github.com/zsh-users/zaw)
        - install + config
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

#### Accessories

- [Solaar](https://github.com/pwr-Solaar/Solaar) 
    - Linux device manager for Logitech devices

#### Gaming

- [MangoHud](https://github.com/flightlessmango/MangoHud)
    - Overlay for hardware data
    - Setup quick ref:
        - TIP: Check if commands (`mangohud`, `mangoapp`) are on PATH
        - [Configuration](https://github.com/ValveSoftware/gamescope?tab=readme-ov-file#options)
        - sanity tests:
            ```zsh
            > mangohud glxgears #OpenGL test
            > MANGOHUD=1 vkcube #Vulkan test
            ```

- [vkBasalt](https://github.com/DadSchoorse/vkBasalt)
    - Vulkan post processing layer for graphical enhancement - integrates with clients

- [GameMode](https://github.com/FeralInteractive/gamemode)
    - Resource optimization manager at OS/Process level to run games
    - References:
        - [Gamemode on Arch](https://wiki.archlinux.org/title/Gamemode)
    - config quick reference:
        - On Steam game launch: `gamemoderun gamescope -H 1440 -r 160 -f --mangoapp %command%`


- [gamescope](https://github.com/ValveSoftware/gamescope)
    - Valve microcompositor for gaming features like:
        - Spoofing resolutions;
        - Upscaling using AMD FidelityFX™ Super Resolution or NVIDIA Image Scaling;
        - Limiting framerates.
    - References:
        -  [Gamescope on Arch](https://wiki.archlinux.org/title/Gamescope)
    - Config quick reference:
        - On Steam game launch [options](https://github.com/ValveSoftware/gamescope?tab=readme-ov-file#options):
            - `gamescope -H 1440 -r 160 -b --mangoapp %command%`

- [Steam Tinker Launch](https://github.com/sonic2kk/steamtinkerlaunch)
    - Auxiliary GUI for Steam where you can configure tools like GameScope, MangoHud, modding tools and more

#### Benchmarking

- [UNIGINE benchmark - Superposition](https://benchmark.unigine.com/superposition)
    - Scored online graphical benchmark, GPU centric
    - Paid
    - Has stress test
    - Bugs on Manjaro with Wayland and NVidia
- [Blender Benchmark](https://opendata.blender.org/)
    - Scored online, cpu and gpu
    - Free
    - Vulkan suport on experimental
    - References:
        - [Blender Benchmark on Arch](https://aur.archlinux.org/packages/blender-benchmark)
- [stress](https://archlinux.org/packages/extra/x86_64/stress) + [s-tui](https://archlinux.org/packages/extra/any/s-tui)
    - CPU stress tests with temp and frequency monitoring
    - procedure:
        ```zsh
        #stress –cpu <number of threads> –timeout <duration in seconds>
        > stress --cpu 12 --timeout 30
        > s-tui #monitoring
        ```
- [gputest](https://www.geeks3d.com/gputest)
    - Stress test & benchmark
    - Example usage: `gputest /width=2560 /height=1440 /test=fur furmark-vk` #furmark vulkan

#### Hardware control

- [GreenWithEnvy (GWE)](https://gitlab.com/leinardi/gwe)
    - Information, control and overclocking fo NVidia GPUs


## Linux distributions reference

### Gaming distros

Distributions with the objective of a game-centric pc simulating console ease of use

- [ChimeraOS](https://chimeraos.org)
    - Arch based
    - AMD Centric
- [Bazzite](https://bazzite.gg/)
    - Fedora based
    - Built-in support for Nvidia
