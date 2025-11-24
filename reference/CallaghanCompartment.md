# Callaghan's model for restricted diffusion in a cylinder

A class to model restricted diffusion in a cylinder using the
Callaghan's model.

## References

Callaghan, P. T. (1995). Pulsed-gradient spin-echo NMR for planar,
cylindrical, and spherical pores under conditions of wall relaxation.
Journal of magnetic resonance, Series A, 113(1), 53-59.

## Super classes

[`midi::BaseCompartment`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.md)
-\>
[`midi::CircularlyShapedCompartment`](https://lmjl-alea.github.io/midi/reference/CircularlyShapedCompartment.md)
-\> `CallaghanCompartment`

## Methods

### Public methods

- [`CallaghanCompartment$clone()`](#method-CallaghanCompartment-clone)

Inherited methods

- [`midi::BaseCompartment$get_parameter_names()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameter_names)
- [`midi::BaseCompartment$get_parameters()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameters)
- [`midi::BaseCompartment$get_signal()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_signal)
- [`midi::CircularlyShapedCompartment$initialize()`](https://lmjl-alea.github.io/midi/reference/CircularlyShapedCompartment.html#method-initialize)

------------------------------------------------------------------------

### Method `clone()`

The objects of this class are cloneable with this method.

#### Usage

    CallaghanCompartment$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
