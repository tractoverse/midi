# Soderman's model for restricted diffusion in a cylinder

A class to model restricted diffusion in a cylinder using the Soderman's
model.

## References

Söderman, O., & Jönsson, B. (1995). Restricted diffusion in cylindrical
geometry. Journal of Magnetic Resonance, Series A, 117(1), 94-97.

## Super classes

[`midi::BaseCompartment`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.md)
-\>
[`midi::CircularlyShapedCompartment`](https://lmjl-alea.github.io/midi/reference/CircularlyShapedCompartment.md)
-\> `SodermanCompartment`

## Methods

### Public methods

- [`SodermanCompartment$clone()`](#method-SodermanCompartment-clone)

Inherited methods

- [`midi::BaseCompartment$get_parameter_names()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameter_names)
- [`midi::BaseCompartment$get_parameters()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameters)
- [`midi::BaseCompartment$get_signal()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_signal)
- [`midi::CircularlyShapedCompartment$initialize()`](https://lmjl-alea.github.io/midi/reference/CircularlyShapedCompartment.html#method-initialize)

------------------------------------------------------------------------

### Method `clone()`

The objects of this class are cloneable with this method.

#### Usage

    SodermanCompartment$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
