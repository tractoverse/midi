# Free compartment class

A class to model free unconstrained diffusion.

## Super class

[`BaseCompartment`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.md)
-\> `FreeCompartment`

## Methods

### Public methods

- [`FreeCompartment$new()`](#method-FreeCompartment-initialize)

- [`FreeCompartment$clone()`](#method-FreeCompartment-clone)

Inherited methods

- [`BaseCompartment$get_parameter_names()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameter_names)
- [`BaseCompartment$get_parameters()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_parameters)
- [`BaseCompartment$get_signal()`](https://lmjl-alea.github.io/midi/reference/BaseCompartment.html#method-get_signal)

------------------------------------------------------------------------

### `FreeCompartment$new()`

Instantiates a new free compartment.

#### Usage

    FreeCompartment$new(diffusivity = NULL)

#### Arguments

- `diffusivity`:

  A numeric value specifying the diffusivity within the sphere in
  \\\mu\\m\\^2\\.ms\\^{-1}\\. Defaults to `NULL`, in which case the
  default free diffusivity of 3 \\\mu\\m\\^2\\.ms\\^{-1}\\ is used.

#### Returns

An instance of the `FreeCompartment` class.

------------------------------------------------------------------------

### `FreeCompartment$clone()`

The objects of this class are cloneable with this method.

#### Usage

    FreeCompartment$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
