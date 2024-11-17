# General configuration helper

Quick references for general configurations

## Manjaro

### Packages

- [Branch compare for Manjaro (Package search)](https://manjaristas.org/branch_compare)

### Kernel

- [Manjaro kernels](https://wiki.manjaro.org/index.php/Manjaro_Kernels)

### NVidia

- [Configure graphics cards on Manjaro](https://wiki.manjaro.org/index.php/Configure_Graphics_Cards)
- to work with wayland some kernel parameters must be set. The easyest permanent way is a config file
    - drop the [kernel module settings file](../src/conf/manjaro/nvidia.conf) inside `/etc/modprobe.d` and restart
    - further references:
        - [NVIDIA on Arch](https://wiki.archlinux.org/title/NVIDIA)
        - [Kernel mode settings via files](https://wiki.archlinux.org/title/Kernel_module#Using_files_in_/etc/modprobe.d/)
