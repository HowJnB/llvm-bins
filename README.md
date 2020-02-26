# Pre-Built Binaries for LLD and LLVM Tools

This repository is a collection of pre-built binaries for the 
LLD linker and various LLVM tools and utilities.

### Overview

The list of tools in this collection includes:

`bugpoint, dsymutil, ld64.lld, ld.lld, llc, lld, lld-link, lli, llvm-addr2line, llvm-ar,
llvm-as, llvm-bcanalyzer, llvm-cat, llvm-cfi-verify, llvm-config, llvm-cov, llvm-c-test, 
llvm-cvtres, llvm-cxxdump, llvm-cxxfilt, llvm-cxxmap, llvm-diff, llvm-dis, llvm-dlltool, 
llvm-dwarfdump, llvm-dwp, llvm-elfabi, llvm-exegesis, llvm-extract, llvm-ifs, llvm-install-name-tool, 
llvm-jitlink, llvm-lib, llvm-link, llvm-lipo, llvm-lto, llvm-lto2, llvm-mc, llvm-mca, llvm-ml, 
llvm-modextract, llvm-mt, llvm-nm, llvm-objcopy, llvm-objdump, llvm-opt-report, llvm-pdbutil,
llvm-profdata, llvm-ranlib, llvm-rc, llvm-readelf, llvm-readobj, llvm-reduce, llvm-rtdyld, 
llvm-size, llvm-split, llvm-stress, llvm-strings, llvm-strip, llvm-symbolizer, llvm-tblgen, 
llvm-undname, llvm-xray, obj2yaml, opt, sancov, sanstats, verify-uselistorder, wasm-ld, yaml2obj`

### Platforms/Architectures

These binaries have been cross-compiled for the most popular combinations of platforms
(`Linux, Windows, macOS`) and architectures (`x86-64, i686, Aarch64, ARM and PowerPC`).
More will be added in the future. The binaries are also built statically so they will
run without dependencies.

Each branch of the repository points to the latest version of the binaries for a particular
platform/architecture pair. The branch `x64pc-linux` for example, points to the latest version 
of the binaries (11.0.f60de4cdf at time of writing) for a x86-64 linux pc.

The various tags allow you to download more specific versions of the binaries. Every release
has a corresponding tag in the form of llvm-[version]-[target] (e.g. llvm-11.0.0-x64pc-linux
).

### Storage

This repository makes use of Large File Storage (LFS) git extension, for more efficient handling
and downloading of binary files. Therefore, you will need to make sure the git-lfs package
is installed on your system before cloning.

### Obtaining the Files

You can download the binaries by cloning the repository and checking-out either
a branch for the latest version, or a tag for a specific release.

- Checkout the binaries (e.g. x64pc-linux):
  ```` bash
     git lfs clone -b x64pc-linux https://github.com/howjnb/llvm-bins.git
  ````
- Switching to a different target (e.g. x86pc-linux):
  ```` bash
     cd llvm-dir
     git checkout x86pc-linux
  ````

