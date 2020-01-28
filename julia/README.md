The recipes in this folder create images providing the julia language.
- `remote-makie.def` provides a minimal setup for remote OpenGL rendering for Makie.jl
- `julia.def` is my custom image for personal use.

1. `remote-makie.def`: To setup remote OpenGL rendering it is assumed that the client and the host(s)
have VirtualGL installed (and for the host on which the rendering happens,
NVIDIA dirvers and obviously singularity which is required to use the image).
After the setup, connect with `vglconnect -s user@host` to the VirtualGL server.
(If you need to connect through a proxy server, you just need another `vglconnect -s user@proxy` before).
Launch the singularity container using the `--nv` option
(`singularity shell --nv julia.sif` for example) and run julia via VirtualGL (`vglrun julia`).

2. `julia.def`: This recipe sets up julia using the official docker image and adds
- some useful utilities and debug tools (`wget ssh vim gnupg apt-utils gcc gdb strace`)
- NVIDIA CUDA and cuDNN
- other programs including `python`, `hdf5`, `imagemagick`, `xorg-dev` and others (see lines 35-39)
- VirtualGL
- JuptyerLab
- LaTeX (with `luatex` and extra packages)
