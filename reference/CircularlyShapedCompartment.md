# Circularly-shaped compartment class

A class to model restricted diffusion in a bounded medium described by a
circular shape with a given radius.

## Super class

[`BaseCompartment`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.md)
-\> `CircularlyShapedCompartment`

## Methods

### Public methods

- [`CircularlyShapedCompartment$new()`](#method-CircularlyShapedCompartment-initialize)

- [`CircularlyShapedCompartment$clone()`](#method-CircularlyShapedCompartment-clone)

Inherited methods

- [`BaseCompartment$get_parameter_names()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameter_names)
- [`BaseCompartment$get_parameters()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameters)
- [`BaseCompartment$get_signal()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_signal)

------------------------------------------------------------------------

### `CircularlyShapedCompartment$new()`

Instantiates a new circular compartment.

#### Usage

    CircularlyShapedCompartment$new(radius = NULL, diffusivity = NULL)

#### Arguments

- `radius`:

  A numeric value specifying the radius of the sphere in \\\mu\\m.

- `diffusivity`:

  A numeric value specifying the diffusivity within the sphere in
  \\\mu\\m\\^2\\.ms\\^{-1}\\.

#### Returns

An instance of the `CircularlyShapedCompartment` class.

------------------------------------------------------------------------

### `CircularlyShapedCompartment$clone()`

The objects of this class are cloneable with this method.

#### Usage

    CircularlyShapedCompartment$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
