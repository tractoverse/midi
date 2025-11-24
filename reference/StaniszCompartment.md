# Stanisz's model for restricted diffusion in a cylinder

A class to model restricted diffusion in a cylinder using the Stanisz's
model.

## References

Stanisz, G. J., Wright, G. A., Henkelman, R. M., & Szafer, A. (1997). An
analytical model of restricted diffusion in bovine optic nerve. Magnetic
Resonance in Medicine, 37(1), 103-111.

## Super classes

[`midi::BaseCompartment`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.md)
-\>
[`midi::CircularlyShapedCompartment`](https://lmjl-alea.github.io/midi/reference/CircularlyShapedCompartment.md)
-\> `StaniszCompartment`

## Methods

### Public methods

- [`StaniszCompartment$clone()`](#method-StaniszCompartment-clone)

Inherited methods

- [`midi::BaseCompartment$get_parameter_names()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameter_names)
- [`midi::BaseCompartment$get_parameters()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameters)
- [`midi::BaseCompartment$get_signal()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_signal)
- [`midi::CircularlyShapedCompartment$initialize()`](https://lmjl-alea.github.io/midi/reference/CircularlyShapedCompartment.html#method-initialize)

------------------------------------------------------------------------

### Method `clone()`

The objects of this class are cloneable with this method.

#### Usage

    StaniszCompartment$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
