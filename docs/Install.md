# Installation

## conda/pip

PyGlider depends on `dask` and `netcdf4`, both of which can be tricky to install using `pip`,
hence we recommend these be installed with [`conda`](https://www.anaconda.com/). To install
PyGlider, create an environment, and do

```
conda create -n gliderwork
conda activate gliderwork
conda install -c conda-forge pyglider
```

### pixi

If you prefer [`pixi`](https://pixi.io/) to conda, you can install PyGlider with

```
pixi init
pixi add pyglider
```



## Editable installation

If you want to be able to edit the files in `pyglider/pyglider` then install
the dependencies as above. Fork of PyGlider on github, and then clone it locally:

```
git clone https://github.com/yourname/pyglider.git
```

Navigate to the new `pyglider` directory and then do `pip install -e .`.
That will re-install pyglider with links to the local directory, so you
can edit the library files. If you do so, consider making a pull-request
with your changes!

### pixi editable installation:

Edit your `pixi.toml` file to include the following:

```
pypi-dependencies:
    pyglider = { path = ".", editable = true }
```

Note that the repo has a `pyproject.toml` with optional pixi tooling that should work just with just

```
pixi install
```

if you execute from the repo root.