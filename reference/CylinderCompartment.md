# Cylinder compartment class

A class to model restricted diffusion in a cylinder.

## Super classes

[`midi::BaseCompartment`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.md)
-\>
[`midi::CircularlyShapedCompartment`](https://lmjl-alea.github.io/midi/reference/CircularlyShapedCompartment.md)
-\> `CylinderCompartment`

## Methods

### Public methods

- [`CylinderCompartment$new()`](#method-CylinderCompartment-new)

- [`CylinderCompartment$clone()`](#method-CylinderCompartment-clone)

Inherited methods

- [`midi::BaseCompartment$get_parameter_names()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameter_names)
- [`midi::BaseCompartment$get_parameters()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameters)
- [`midi::BaseCompartment$get_signal()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_signal)

------------------------------------------------------------------------

### Method `new()`

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
  [`CircularlyShapedCompartment`](https://lmjl-alea.github.io/midi/reference/CircularlyShapedCompartment.md)
  class specifying the restricted compartment within the sphere.
  Defaults to a Van Gelderen compartment.

#### Returns

An instance of the `CylinderCompartment` class.

------------------------------------------------------------------------

### Method `clone()`

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
