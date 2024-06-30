# General configuration helper

Quick references for general configurations

## Manjaro

### NVidia

- to work with wayland some kernel parameters must be set. The easyest permanent way is a config file
    - drop the [kernel module settings file](../src/conf/manjaro/nvidia.conf) inside `/etc/modprobe.d` and restart
    - further references:
        - [NVIDIA on Arch](https://wiki.archlinux.org/title/NVIDIA)
        - [Kernel mode settings via files](https://web.whatsapp.com/)
