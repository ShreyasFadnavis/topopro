# Separable homological optimization for intravoxel incoherent motion: TopoPro

This repo demonstrates a framework (TopoPro) for estimating the IVIM model via data Diffusion MRI,
as described in the paper: `Separable homological optimization for intravoxel incoherent motion`. It is a topological method for solving the bi-exponential IVIM microstructural model through the lens of a separable inverse problem formulation.

## Images

The notebook [IVIM TopoPro Example](notebooks/ivim_topopro_example.ipynb) shows how `TopoPro` can be used to fit the data with a simple interface. We use the [DIPY](www.dipy.org) API for implementations which are self-contained, efficient, unit-tested, and have submitted a PR to incorporate TopoPro directly into the package.


The notebook [IVIM hyperct Example](notebooks/gen_obj_surf.ipynb) shows how `hyperct` can be used to visualize subspaces of optimizations problems and their homology. This dependency of TopoPro is used in the algorithm during optimization to allow TopoPro to understand the optimization sub-problem as solver progress is made. 

### Fitting with TopoPro
```
topopro = IvimModelTopoPro(gtab)
topopro_fit = topopro.fit(data=data, mask=mask)
```

Dependencies are in the `environment.yml` file.
