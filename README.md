FALFILFA-bundle
===============

Helper to build [FALFILFA](https://github.com/ACCORD-NWP/FALFILFA), including its dependencies.
Everything is done in a `work/` directory.

Dependencies:
-------------

* eccodes
* ecbundle
* ecbuild
* aec
* fiat

Installation
------------

Get the repo:
```
git clone https://githubcom/ACCORD-NWP/FALFILFA-bundle && cd FALFILFA-bundle
```

Build the FA/LFI/LFA library
----------------------------

Edit the `bundle.yml` if you want to specify different versions of packages.

Get packages (in a `source` directory):
```
./download-bundle
```

Build dependencies:
```
./build dependencies
```

Build library:
```
./build falfilfa
```

Build the `falfilfa4py` python package wheel
--------------------------------------------

### Locally.

```
./build dependencies
./build falfilfa4py
```

### In a `manylinux` container, run with `singularity`.

On MF machines, get certificate: `source env_mf`

```
./get_container
./build dependencies --sing
./build falfilfa4py --sing
```

