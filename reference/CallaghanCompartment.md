# Callaghan's model for restricted diffusion in a cylinder

A class to model restricted diffusion in a cylinder using the
Callaghan's model.

## References

Callaghan, P. T. (1995). Pulsed-gradient spin-echo NMR for planar,
cylindrical, and spherical pores under conditions of wall relaxation.
Journal of magnetic resonance, Series A, 113(1), 53-59.

## Super classes

[`BaseCompartment`](https://tractoverse.github.io/midi/reference/BaseCompartment.md)
-\>
[`CircularlyShapedCompartment`](https://tractoverse.github.io/midi/reference/CircularlyShapedCompartment.md)
-\> `CallaghanCompartment`

## Methods

### Public methods

- [`CallaghanCompartment$clone()`](#method-CallaghanCompartment-clone)

Inherited methods

- [`BaseCompartment$get_parameter_names()`](https://tractoverse.github.io/midi/reference/BaseCompartment.html#method-get_parameter_names)
- [`BaseCompartment$get_parameters()`](https://tractoverse.github.io/midi/reference/BaseCompartment.html#method-get_parameters)
- [`BaseCompartment$get_signal()`](https://tractoverse.github.io/midi/reference/BaseCompartment.html#method-get_signal)
- [`CircularlyShapedCompartment$initialize()`](https://tractoverse.github.io/midi/reference/CircularlyShapedCompartment.html#method-initialize)

------------------------------------------------------------------------

### `CallaghanCompartment$clone()`

The objects of this class are cloneable with this method.

#### Usage

    CallaghanCompartment$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
