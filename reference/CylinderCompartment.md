# Cylinder compartment class

A class to model restricted diffusion in a cylinder.

## Super classes

[`BaseCompartment`](https://tractoverse.github.io/midi/reference/BaseCompartment.md)
-\>
[`CircularlyShapedCompartment`](https://tractoverse.github.io/midi/reference/CircularlyShapedCompartment.md)
-\> `CylinderCompartment`

## Methods

### Public methods

- [`CylinderCompartment$new()`](#method-CylinderCompartment-initialize)

- [`CylinderCompartment$clone()`](#method-CylinderCompartment-clone)

Inherited methods

- [`BaseCompartment$get_parameter_names()`](https://tractoverse.github.io/midi/reference/BaseCompartment.html#method-get_parameter_names)
- [`BaseCompartment$get_parameters()`](https://tractoverse.github.io/midi/reference/BaseCompartment.html#method-get_parameters)
- [`BaseCompartment$get_signal()`](https://tractoverse.github.io/midi/reference/BaseCompartment.html#method-get_signal)

------------------------------------------------------------------------

### `CylinderCompartment$new()`

Instantiates a new cylinder compartment.

#### Usage

    CylinderCompartment$new(
      axis = c(0, 0, 1),
      restricted_compartment = VanGelderenCompartment$new()
    )

#### Arguments

- `axis`:

  A length-3 numeric vector specifying the axis of the cylinder.

- `restricted_compartment`:

  An instance of the
  [`CircularlyShapedCompartment`](https://tractoverse.github.io/midi/reference/CircularlyShapedCompartment.md)
  class specifying the restricted compartment within the sphere.
  Defaults to a Van Gelderen compartment.

#### Returns

An instance of the `CylinderCompartment` class.

------------------------------------------------------------------------

### `CylinderCompartment$clone()`

The objects of this class are cloneable with this method.

#### Usage

    CylinderCompartment$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.

## Examples

``` r
cylComp <- CylinderCompartment$new()
cylComp$get_signal(small_delta = 30, big_delta = 30, G = 0.040)
#> [1] 0.002063224
cylComp$get_parameter_names()
#> [1] "CylinderAxis"        "CylinderRadius"      "CylinderDiffusivity"
cylComp$get_parameters()
#> $CylinderAxis
#> [1] 0 0 1
#> 
#> $CylinderRadius
#> [1] 15
#> 
#> $CylinderDiffusivity
#> [1] 3
#> 
```
