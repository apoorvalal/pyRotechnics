# `pyRotechnics`

## conda environment for R-Python interoperability powered by [ryp](https://github.com/Wainberg/ryp)

Create an environment using

```
conda env create -f environment.yml
```

which should install a (relatively lightweight) R in a self-contained conda environment. Can be used as stand-alone replicable R environment powered by conda-forge, or as a base for R-Python interoperability. Install new `R` packages using `mamba install -c conda-forge r-<package>`.

### python interoperability

`ryp` lets you operate it from python and has much better usability than `rpy2`. see `pyRotechnics.ipynb` for an example.

generated using `conda env export --no-builds --from-history > environment.yml`, which should be OS-agnostic. Tested on ubuntu 24.04LTS; please report issues if you encounter issues on other systems.
