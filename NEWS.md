# midi (development version)

# midi 0.2.0

## Breaking changes

* The unit system has changed from SI units (m, s, T/m) to μm, ms, and μT/μm
  throughout all compartment classes and helper functions.

* `CylinderBundleCompartment$new()` no longer accepts `axis`, `radius`,
  `diffusivity`, `n_cylinders`, `axis_concentration`, `radius_sd`,
  `radial_model`, and `seed` arguments. It now accepts
  `cylinder_compartments`, a list of `CylinderCompartment` objects (typically
  produced by `rcylinders()`), and infers axis, radius, and diffusivity
  statistics by fitting Watson and Gamma distributions to the provided
  compartments.

* `CylinderCompartment$new()` no longer accepts `radius`, `diffusivity`, and
  `radial_model` arguments. It now accepts a `restricted_compartment` argument,
  an instance of a circularly-shaped compartment class (e.g.,
  `VanGelderenCompartment$new()`).

## New features

* New `bvalue()` function to compute the b-value from gradient pulse parameters.

* New `FreeCompartment` class to model free unconstrained diffusion.

* New `GammaDistribution` class providing `fit()`, `random()`, `get_mean()`,
  `get_variance()`, `get_shape()`, and `get_scale()` methods.

* New `rcylinders()` function to sample a list of `CylinderCompartment` objects
  from Watson (axis) and Gamma (radius, diffusivity) distributions.

* New `SphereCompartment` class to model restricted diffusion in a sphere.

* New `WatsonDistribution` class providing `fit()`, `random()`, `get_axis()`,
  and `get_concentration()` methods.

* All compartment classes now expose `get_parameters()` and
  `get_parameter_names()` methods inherited from the new `BaseCompartment`
  base class.

# midi 0.1.0

* Initial CRAN submission.
