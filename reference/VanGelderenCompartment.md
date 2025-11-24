# Van Gelderen's model for restricted diffusion in a cylinder

A class to model restricted diffusion in a cylinder using the Van
Gelderen's model.

## References

Vangelderen, P., DesPres, D., Vanzijl, P. C. M., & Moonen, C. T. W.
(1994). Evaluation of restricted diffusion in cylinders. Phosphocreatine
in rabbit leg muscle. Journal of Magnetic Resonance, Series B, 103(3),
255-260.

## Super classes

[`midi::BaseCompartment`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.md)
-\>
[`midi::CircularlyShapedCompartment`](https://lmjl-alea.github.io/midi/reference/CircularlyShapedCompartment.md)
-\> `VanGelderenCompartment`

## Methods

### Public methods

- [`VanGelderenCompartment$clone()`](#method-VanGelderenCompartment-clone)

Inherited methods

- [`midi::BaseCompartment$get_parameter_names()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameter_names)
- [`midi::BaseCompartment$get_parameters()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameters)
- [`midi::BaseCompartment$get_signal()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_signal)
- [`midi::CircularlyShapedCompartment$initialize()`](https://lmjl-alea.github.io/midi/reference/CircularlyShapedCompartment.html#method-initialize)

------------------------------------------------------------------------

### Method `clone()`

The objects of this class are cloneable with this method.

#### Usage

    VanGelderenCompartment$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
