[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![Docs](https://img.shields.io/badge/info-documentation-informational)](https://umami-hep.github.io/atlas-ftag-tools/main)
[![PyPI version](https://badge.fury.io/py/atlas-ftag-tools.svg)](https://badge.fury.io/py/atlas-ftag-tools)
[![codecov](https://codecov.io/gh/umami-hep/atlas-ftag-tools/branch/main/graph/badge.svg?token=MBHLIYYQ7I)](https://codecov.io/gh/umami-hep/atlas-ftag-tools)

# ATLAS FTAG Python Tools

This is a collection of Python tools for working with files produced with the FTAG [ntuple dumper](https://gitlab.cern.ch/atlas-flavor-tagging-tools/training-dataset-dumper/).
The code is intended to be used a [library](https://iscinumpy.dev/post/app-vs-library/) for other projects.
Please see the [example notebook](ftag/example.ipynb) for usage.

# Quickstart 

## Installation

If you want to use this package without modification, you can install from [pypi](https://pypi.org/project/atlas-ftag-tools/) using `pip`.

```bash
pip install atlas-ftag-tools
```

To additionally install the development dependencies (for formatting and linting) use
```bash
pip install atlas-ftag-tools[dev]
```

NB: `lsetup xcache` does not setup python module `XRootD` while `lsetup xcache` does. 

```bash
setupATLAS
lsetup xrootd
voms-proxy-init -voms atlas
```
or 
Install xrootd precompiled for upp 
```bash 
mamba activate upp 
mamba install -c conda-forge xrootd
```

Then 
```bash
setupATLAS
lsetup xcache
voms-proxy-init -voms atlas
```

The error otherwise being 
```
File "/auto_home/users/rbouquet/miniforge3/envs/upp/lib/python3.11/site-packages/fsspec_xrootd/xrootd.py", line 18, in <module>
    from XRootD import client
ModuleNotFoundError: No module named 'XRootD'
```



## Usage

Extensive examples are given in the [Examples](https://umami-hep.github.io/atlas-ftag-tools/main/examples/index.html)