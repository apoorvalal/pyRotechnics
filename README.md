# `pyRotechnics`

## conda environment for R-Python interoperability powered by [ryp](https://github.com/Wainberg/ryp)

Create an environment using

```
conda env create -f environment.yml
```

which should install a (relatively lightweight) R in a self-contained conda environment. `ryp` lets you operate it from python and has much better usability than `rpy2`. see `pyRotechnics.ipynb` for an example.

generated using `conda env export --no-builds --from-history > environment.yml`, which should be os-agnostic. Tested on ubuntu 24.04LTS; report issues if you encounter issues on other systems.
