This recipe sets up julia using the official docker image and adds
- some useful utilities and debug tools (`wget ssh vim gnupg apt-utils gcc gdb strace`)
- NVIDIA CUDA and cuDNN
- other programs including `python`, `hdf5`, `imagemagick`, `xorg-dev` and others (see lines 35-39)
- VirtualGL
- JuptyerLab
- LaTeX (with `luatex` and extra packages)
