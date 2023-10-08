# Simple bash script to install UMFPACK (only)

This script fetches the `dev` branch of [SuiteSparse](https://github.com/DrTimothyAldenDavis/SuiteSparse), compiles only UMFPACK and its required libraries, and install the resulting files to `/usr/local`.

**Note:** The installation directories are `/usr/local/include/umfpack` and `/usr/local/lib/umfpack`.

First, install some dependencies:

```bash
bash install-deps.bash
```

Then, install umfpack with OpenBLAS:

```bash
bash install-umfpack.bash
```

Or, to use Intel MKL, run:

```bash
bash install-intel-mkl-linux.bash
bash install-umfpack.bash mkl
```

## Installed include files

Output of `tree /usr/local/include/umfpack`

```text
/usr/local/include/umfpack
├── amd.h
├── camd.h
├── ccolamd.h
├── cholmod.h
├── colamd.h
├── SuiteSparse_config.h
└── umfpack.h

1 directory, 7 files
```

## Installed lib files

Output of `tree /usr/local/lib/umfpack`

```text
/usr/local/lib/umfpack
├── cmake
│   ├── AMD
│   │   ├── AMDConfig.cmake
│   │   ├── AMDConfigVersion.cmake
│   │   ├── AMDTargets.cmake
│   │   └── AMDTargets-release.cmake
│   ├── CAMD
│   │   ├── CAMDConfig.cmake
│   │   ├── CAMDConfigVersion.cmake
│   │   ├── CAMDTargets.cmake
│   │   └── CAMDTargets-release.cmake
│   ├── CCOLAMD
│   │   ├── CCOLAMDConfig.cmake
│   │   ├── CCOLAMDConfigVersion.cmake
│   │   ├── CCOLAMDTargets.cmake
│   │   └── CCOLAMDTargets-release.cmake
│   ├── CHOLMOD
│   │   ├── CHOLMODConfig.cmake
│   │   ├── CHOLMODConfigVersion.cmake
│   │   ├── CHOLMODTargets.cmake
│   │   └── CHOLMODTargets-release.cmake
│   ├── COLAMD
│   │   ├── COLAMDConfig.cmake
│   │   ├── COLAMDConfigVersion.cmake
│   │   ├── COLAMDTargets.cmake
│   │   └── COLAMDTargets-release.cmake
│   ├── SuiteSparse
│   │   ├── SuiteSparseBLAS32.cmake
│   │   ├── SuiteSparseBLAS64.cmake
│   │   ├── SuiteSparseBLAS.cmake
│   │   ├── SuiteSparseLAPACK.cmake
│   │   ├── SuiteSparsePolicy.cmake
│   │   ├── SuiteSparseReport.cmake
│   │   └── SuiteSparse__thread.cmake
│   ├── SuiteSparse_config
│   │   ├── SuiteSparse_configConfig.cmake
│   │   ├── SuiteSparse_configConfigVersion.cmake
│   │   ├── SuiteSparse_configTargets.cmake
│   │   └── SuiteSparse_configTargets-release.cmake
│   └── UMFPACK
│       ├── UMFPACKConfig.cmake
│       ├── UMFPACKConfigVersion.cmake
│       ├── UMFPACKTargets.cmake
│       └── UMFPACKTargets-release.cmake
├── libamd.a
├── libamd.so -> libamd.so.3
├── libamd.so.3 -> libamd.so.3.2.1
├── libamd.so.3.2.1
├── libcamd.a
├── libcamd.so -> libcamd.so.3
├── libcamd.so.3 -> libcamd.so.3.2.1
├── libcamd.so.3.2.1
├── libccolamd.a
├── libccolamd.so -> libccolamd.so.3
├── libccolamd.so.3 -> libccolamd.so.3.2.1
├── libccolamd.so.3.2.1
├── libcholmod.a
├── libcholmod.so -> libcholmod.so.4
├── libcholmod.so.4 -> libcholmod.so.4.2.1
├── libcholmod.so.4.2.1
├── libcolamd.a
├── libcolamd.so -> libcolamd.so.3
├── libcolamd.so.3 -> libcolamd.so.3.2.1
├── libcolamd.so.3.2.1
├── libsuitesparseconfig.a
├── libsuitesparseconfig.so -> libsuitesparseconfig.so.7
├── libsuitesparseconfig.so.7 -> libsuitesparseconfig.so.7.2.1
├── libsuitesparseconfig.so.7.2.1
├── libumfpack.a
├── libumfpack.so -> libumfpack.so.6
├── libumfpack.so.6 -> libumfpack.so.6.2.1
├── libumfpack.so.6.2.1
└── pkgconfig
    ├── AMD.pc
    ├── CAMD.pc
    ├── CCOLAMD.pc
    ├── CHOLMOD.pc
    ├── COLAMD.pc
    ├── SuiteSparse_config.pc
    └── UMFPACK.pc

11 directories, 70 files
```
