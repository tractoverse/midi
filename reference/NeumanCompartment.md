# Neuman's model for restricted diffusion in a cylinder

A class to model restricted diffusion in a cylinder using the Neuman's
model.

## References

Neuman, C. H. (1974). Spin echo of spins diffusing in a bounded medium.
The Journal of Chemical Physics, 60(11), 4508-4511.

## Super classes

[`midi::BaseCompartment`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.md)
-\>
[`midi::CircularlyShapedCompartment`](https://lmjl-alea.github.io/midi/reference/CircularlyShapedCompartment.md)
-\> `NeumanCompartment`

## Methods

### Public methods

- [`NeumanCompartment$clone()`](#method-NeumanCompartment-clone)

Inherited methods

- [`midi::BaseCompartment$get_parameter_names()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameter_names)
- [`midi::BaseCompartment$get_parameters()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameters)
- [`midi::BaseCompartment$get_signal()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_signal)
- [`midi::CircularlyShapedCompartment$initialize()`](https://lmjl-alea.github.io/midi/reference/CircularlyShapedCompartment.html#method-initialize)

------------------------------------------------------------------------

### Method `clone()`

The objects of this class are cloneable with this method.

#### Usage

    NeumanCompartment$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
