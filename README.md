# MG-GCN

Created for the MLSYS submission of the MG-GCN, multi-GPU GCN training framework,

Our software depends on a recent CUDA installation, tested on CUDA 11.4

For parallel preprocessing, our software makes use of the parallel standard library, GCC implementation of the standard library depends on TBB.
A recent version of TBB is required, the following is the most recent TBB version that is compatible for our purpose: [tbb release](https://github.com/oneapi-src/oneTBB/archive/v2020.2.zip)

One can use the following command to compile and install TBB, `python3 build/build.py --prefix="<PATH-TO-INSTALL>" --install-libs --install-devel`
If tbb is not found, add environment variable: `export TBB_ROOT=<PATH-TO-INSTALL>`

A recent version of NCCL is also required. You can follow the instructions here to compile and install it: [nccl github](https://github.com/NVIDIA/nccl)

GCC version 9 or above is required to compile our software.

When all prerequisites are installed, one can create a build directory and compile our software as follows:
```
mkdir build
cd build
cmake ..
make -j
```
