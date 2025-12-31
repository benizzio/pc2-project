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

#### Gaming

- [Proton-GE-Custom](https://github.com/GloriousEggroll/proton-ge-custom)
    - Bleeding edge community alternative to proton (to also run with Steam)

- [Heroic Games Launcher](https://heroicgameslauncher.com/) `PROSPECT`
    - Open source client for for Epic Games Store, with proton integration to run games. Very customizable

- [Lutris](https://lutris.net)
    - Open source client for other stores, also with proton integration. Additional focus on emulation and game preservation

#### Distros

- [Distrobox](https://github.com/89luca89/distrobox) `PROSPECT`
    - Docker management layer to seamlessly run other Linux distro inside yours
    - GUI:
        - [DistroShelf](https://github.com/ranfdev/DistroShelf)


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
    - [MangoJuice](https://github.com/radiolamp/mangojuice) `PROSPECT`
        - UI to configure MangoHud

- [vkBasalt](https://github.com/DadSchoorse/vkBasalt) `PROSPECT`
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
    - Auxiliary GUI for Steam where you can configure tools like GameMode, gamescope, MangoHud, modding tools and more
        - When Proton version is not found (e.g. an update), clean directory `/dev/shm/steamtinkerlaunch`

- [ProtonUP-Qt](https://github.com/DavidoTek/ProtonUp-Qt)
    - Axiliary GUI to easily download and install compatibility tools (e.g. Proton GE, Steam Tinker Launch) on Steam and Lutris

- [ProtonPlus](https://github.com/Vysp3r/ProtonPlus) `PROSPECT`
    - Axiliary GUI to easily download and install compatibility tools (e.g. Proton GE, Steam Tinker Launch) on Steam, Lutris, Heroic, etc.

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

#### System & Hardware

#### Monitoring

- [Mission center](https://missioncenter.io)
    - for Arch:
        - [Package](https://archlinux.org/packages/extra/x86_64/mission-center)

##### Config

- [LinuxToys](https://github.com/psygreg/linuxtoys)
    - Easy to use collection installer of a curated collection of linux tools to help beginners.

##### Control & Tuning

- [GreenWithEnvy (GWE)](https://gitlab.com/leinardi/gwe)
    - Information, control and overclocking for NVidia GPUs
- [Linux GPU Control Application](https://github.com/ilya-zlobintsev/LACT) `PROSPECT`
    - Information, control and overclocking for multiple GPUs
- [CoreCTL](https://gitlab.com/corectrl/corectr) `MAINTENANCE`
    - CPU Informantion and control


#### Software development

- [JetBrains Toolbox](https://www.jetbrains.com/toolbox-app)
    - Manager app for all JetBrains tools. Installs, updates, keeps project references
    - for Arch:
        - [AUR package](https://aur.archlinux.org/packages/jetbrains-toolbox)

- [Zed](https://zed.dev/)
    - Rust IDE with Vulkan GPU acceleration
    - for Arch:
        - [AUR package](https://archlinux.org/packages/extra/x86_64/zed)

- [pgModeler](https://pgmodeler.io)
    - PostgreSQL database modeler with code generation
    - for Arch:
        - [AUR package](https://aur.archlinux.org/packages/pgmodeler)

- [lazydocker](https://github.com/jesseduffield/lazydocker)

## Gimmicks

- [Cool Retro Term](https://github.com/Swordfish90/cool-retro-term)


## Linux distributions reference

### Gaming distros

Distributions with the objective of a game-centric pc simulating console ease of use

- [ChimeraOS](https://chimeraos.org)
    - Arch based
    - AMD Centric
- [Bazzite](https://bazzite.gg)
    - Fedora based
    - Built-in support for Nvidia
- [Nobara](https://nobaraproject.org)
    - Fedora based
    - Built-in support for Nvidia
    - From [GloriousEggroll](https://github.com/GloriousEggroll)
- [CachyOS](https://cachyos.org/)
    - Arch based
    - Optimized for performance, including in gaming