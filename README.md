# `pyRotechnics`

## conda environment for R-Python interoperability powered by [ryp](https://github.com/Wainberg/ryp?tab=readme-ov-file#to_py)

Create an environment using 

```
conda env create -f environment.yml
```

which should install a (relatively lightweight) R in a self-contained conda environment. `ryp` lets you operate it from python and has much better usability than `rpy2`. see `pyRotechnics.ipynb` for an example.
