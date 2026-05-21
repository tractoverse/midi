# Sphere compartment class

A class to model restricted diffusion in a sphere.

## Super classes

[`BaseCompartment`](https://tractoverse.github.io/midi/reference/BaseCompartment.md)
-\>
[`CircularlyShapedCompartment`](https://tractoverse.github.io/midi/reference/CircularlyShapedCompartment.md)
-\> `SphereCompartment`

## Methods

### Public methods

- [`SphereCompartment$new()`](#method-SphereCompartment-initialize)

- [`SphereCompartment$clone()`](#method-SphereCompartment-clone)

Inherited methods

- [`BaseCompartment$get_parameter_names()`](https://tractoverse.github.io/midi/reference/BaseCompartment.html#method-get_parameter_names)
- [`BaseCompartment$get_parameters()`](https://tractoverse.github.io/midi/reference/BaseCompartment.html#method-get_parameters)
- [`BaseCompartment$get_signal()`](https://tractoverse.github.io/midi/reference/BaseCompartment.html#method-get_signal)

------------------------------------------------------------------------

### `SphereCompartment$new()`

Instantiates a new sphere compartment.

#### Usage

    SphereCompartment$new(restricted_compartment = VanGelderenCompartment$new())

#### Arguments

- `restricted_compartment`:

  An instance of the
  [`CircularlyShapedCompartment`](https://tractoverse.github.io/midi/reference/CircularlyShapedCompartment.md)
  class specifying the restricted compartment within the sphere.
  Defaults to a Van Gelderen compartment.

#### Returns

An instance of the `SphereCompartment` class.

------------------------------------------------------------------------

### `SphereCompartment$clone()`

The objects of this class are cloneable with this method.

#### Usage

    SphereCompartment$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.

## Examples

``` r
sphComp <- SphereCompartment$new()
sphComp$get_signal(small_delta = 30, big_delta = 30, G = 0.040)
#> [1] 0.1205943
sphComp$get_parameter_names()
#> [1] "SphereRadius"      "SphereDiffusivity"
sphComp$get_parameters()
#> $SphereRadius
#> [1] 15
#> 
#> $SphereDiffusivity
#> [1] 3
#> 
```
