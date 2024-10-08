# `pyRotechnics`

## miniforge environment for R-Python interoperability powered by [ryp](https://github.com/Wainberg/ryp)

Create an environment using

```
mamba env create -f environment.yml
```
[after setting up your environment to use mamba](https://mamba.readthedocs.io/en/latest/installation/mamba-installation.html#fresh-install-recommended). Avoid using the (commercial) anaconda distribution unless you work somewhere that pays for it.

This should install a (relatively lightweight) R in a self-contained conda (mamba/miniforge) environment. Can be used as stand-alone replicable R environment powered by conda-forge, or as a base for R-Python interoperability. 

- Install new `R` packages using `mamba install -c conda-forge r-<package>`. Most (all?) CRAN packages are hosted on conda-forge prefixed by `r-` , e.g. [`r-grf`](https://github.com/conda-forge/r-grf-feedstock)
- Do *not* use `install.packages`, as this will write to your personal library and will therefore not be versioned or retrievable by env export. 

### python interoperability

`ryp` lets you operate it from python and has much better usability than `rpy2`. see `pyRotechnics.ipynb` for an example.

### keeping env yaml updated

the env file is generated using `mamba env export --no-builds --from-history > environment.yml`, which should be OS-agnostic. Run this again if you install more packages. For more involved projects with dependencies that span system packages managers (apt/yum/...), python, and R, consider `pixi`.

Tested on ubuntu 24.04LTS; please report issues if you encounter issues on other systems.
