# Separable homological optimization for intravoxel incoherent motion: TopoPro

This repo demonstrates a framework (TopoPro) for estimating the IVIM model via data Diffusion MRI,
as described in the paper: `Separable homological optimization for intravoxel incoherent motion`. It is a topological method for solving the bi-exponential IVIM microstructural model through the lens of a separable inverse problem formulation.

<img src="https://github.com/ShreyasFadnavis/topopro/blob/master/figs/comparison_bar_chart.PNG" width="450" height="512" title="TopoPro Comparison">

**

## Images

The notebook [IVIM TopoPro Example](notebooks/ivim_topopro_example.ipynb) shows how `TopoPro` can be used to fit the data with a simple interface. We use the [DIPY](www.dipy.org) API for implementations which are self-contained, efficient, unit-tested, and have submitted a PR to incorporate TopoPro directly into the package.

### Fitting with TopoPro
```
topopro = IvimModelTopoPro(gtab)
topopro_fit = topopro.fit(data=data, mask=mask)
```

Dependencies are in the `environment.yml` file.
