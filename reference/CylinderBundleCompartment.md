# Cylinder bundle compartment class

A class to model restricted diffusion in a bundle of cylinders.

## Super class

[`midi::BaseCompartment`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.md)
-\> `CylinderBundleCompartment`

## Methods

### Public methods

- [`CylinderBundleCompartment$new()`](#method-CylinderBundleCompartment-new)

- [`CylinderBundleCompartment$clone()`](#method-CylinderBundleCompartment-clone)

Inherited methods

- [`midi::BaseCompartment$get_parameter_names()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameter_names)
- [`midi::BaseCompartment$get_parameters()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameters)
- [`midi::BaseCompartment$get_signal()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_signal)

------------------------------------------------------------------------

### Method `new()`

Instantiates a new cylinder bundle compartment.

#### Usage

    CylinderBundleCompartment$new(
      cylinder_density,
      cylinder_compartments,
      axial_diffusivity = NULL,
      radial_diffusivity = NULL
    )

#### Arguments

- `cylinder_density`:

  A numeric value specifying the density of the cylinders in the voxel.
  Must be between 0 and 1.

- `cylinder_compartments`:

  A list of instances of the
  [`CylinderCompartment`](https://lmjl-alea.github.io/midi/reference/CylinderCompartment.md)
  class specifying the compartments within the bundle.

- `axial_diffusivity`:

  A numeric value specifying the axial diffusivity in the space outside
  the cylinders in m\\^2\\.s\\^{-1}\\. If not provided, defaults to a
  tortuosity model reducing the intrinsic diffusivity depending on
  orientation dispersion. Defaults to `NULL` in which case the
  extracellular axial diffusivity is set via a tortuosity model based on
  the dispersion in orientation.

- `radial_diffusivity`:

  A numeric value specifying the radial diffusivity in the space outside
  the cylinders in m\\^2\\.s\\^{-1}\\. Defaults to `NULL` in which case
  the extracellular radial diffusivity is set via a tortuosity model
  based on the intracellular density.

#### Returns

An instance of the `CylinderBundleCompartment` class.

------------------------------------------------------------------------

### Method `clone()`

The objects of this class are cloneable with this method.

#### Usage

    CylinderBundleCompartment$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.

## Examples

``` r
withr::with_seed(1234, {
  cyls <- rcylinders(
    n = 100,
    axis_mean = c(0, 0, 1),
    radius_mean = 5,
    diffusivity_mean = 3,
    axis_concentration = 10,
    radius_sd = 1,
    diffusivity_sd = 0
  )
})

comp <- CylinderBundleCompartment$new(
  cylinder_density = 0.5,
  cylinder_compartments = cyls
)

comp$get_signal(
  small_delta = 30,
  big_delta = 30,
  G = 0.040,
  direction = c(0, 0, 1)
)
#> [1] 0.005344176

comp$get_parameters()
#> $CylinderAxisMean
#> [1] -0.028925430 -0.006517909 -0.999560322
#> 
#> $CylinderAxisConcentration
#> [1] 10.6864
#> 
#> $CylinderRadiusMean
#> [1] 5.082161
#> 
#> $CylinderRadiusStd
#> [1] 0.9930441
#> 
#> $CylinderDiffusivityMean
#> [1] 3
#> 
#> $CylinderDiffusivityStd
#> [1] 0
#> 
#> $CylinderDensity
#> [1] 0.5
#> 
#> $CylinderAxialDiffusivity
#> [1] 2.431526
#> 
#> $CylinderRadialDiffusivity
#> [1] 1.458915
#> 
```
