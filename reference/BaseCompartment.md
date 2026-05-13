# Base compartment class

The base class for compartment models.

## Methods

### Public methods

- [`BaseCompartment$get_signal()`](#method-BaseCompartment-get_signal)

- [`BaseCompartment$get_parameter_names()`](#method-BaseCompartment-get_parameter_names)

- [`BaseCompartment$get_parameters()`](#method-BaseCompartment-get_parameters)

- [`BaseCompartment$clone()`](#method-BaseCompartment-clone)

------------------------------------------------------------------------

### `BaseCompartment$get_signal()`

Computes the signal attenuation predicted by the model.

#### Usage

    BaseCompartment$get_signal(
      small_delta,
      big_delta,
      G,
      direction = c(0, 0, 1),
      echo_time = NULL,
      n_max = 20L,
      m_max = 50L
    )

#### Arguments

- `small_delta`:

  A numeric value specifying the duration of the gradient pulse in
  milliseconds.

- `big_delta`:

  A numeric value specifying the duration between the gradient pulses in
  milliseconds.

- `G`:

  A numeric value specifying the strength of the gradient in
  mT.\\\mu\\m\\^{-1}\\.

- `direction`:

  A numeric vector specifying the direction of the gradient. Defaults to
  `c(0, 0, 1)`.

- `echo_time`:

  A numeric value specifying the echo time in milliseconds.

- `n_max`:

  An integer value specifying the maximum order of the Bessel function.
  Defaults to `20L`.

- `m_max`:

  An integer value specifying the maximum number of extrema for the
  Bessel function. Defaults to `50L`.

#### Returns

A numeric value storing the predicted signal attenuation.

#### Examples

    freeComp <- FreeCompartment$new()
    freeComp$get_signal(small_delta = 30, big_delta = 30, G = 0.040)

    sphereComp <- SphereCompartment$new()
    sphereComp$get_signal(small_delta = 30, big_delta = 30, G = 0.040)

    sodermanComp <- SodermanCompartment$new()
    sodermanComp$get_signal(small_delta = 30, big_delta = 30, G = 0.040)

    staniszComp <- StaniszCompartment$new()
    staniszComp$get_signal(small_delta = 30, big_delta = 30, G = 0.040)

    neumanComp <- NeumanCompartment$new()
    neumanComp$get_signal(
      small_delta = 30, big_delta = 30, G = 0.040,
      echo_time = 40
    )

    callaghanComp <- CallaghanCompartment$new()
    callaghanComp$get_signal(small_delta = 30, big_delta = 30, G = 0.040)

    vanGelderenComp <- VanGelderenCompartment$new()
    vanGelderenComp$get_signal(small_delta = 30, big_delta = 30, G = 0.040)

------------------------------------------------------------------------

### `BaseCompartment$get_parameter_names()`

Returns the names of the compartment parameters

#### Usage

    BaseCompartment$get_parameter_names()

#### Returns

A character vector storing the names of the compartment parameters.

#### Examples

    freeComp <- FreeCompartment$new()
    freeComp$get_parameter_names()

------------------------------------------------------------------------

### `BaseCompartment$get_parameters()`

Returns the values of the compartment parameters

#### Usage

    BaseCompartment$get_parameters()

#### Returns

A numeric vector storing the values of the compartment parameters.

#### Examples

    freeComp <- FreeCompartment$new()
    freeComp$get_parameters()

------------------------------------------------------------------------

### `BaseCompartment$clone()`

The objects of this class are cloneable with this method.

#### Usage

    BaseCompartment$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.

## Examples

``` r

## ------------------------------------------------
## Method `BaseCompartment$get_signal()`
## ------------------------------------------------

freeComp <- FreeCompartment$new()
freeComp$get_signal(small_delta = 30, big_delta = 30, G = 0.040)
#> [1] 0.002063224

sphereComp <- SphereCompartment$new()
sphereComp$get_signal(small_delta = 30, big_delta = 30, G = 0.040)
#> [1] 0.1205943

sodermanComp <- SodermanCompartment$new()
sodermanComp$get_signal(small_delta = 30, big_delta = 30, G = 0.040)
#> [1] 0.01565033

staniszComp <- StaniszCompartment$new()
staniszComp$get_signal(small_delta = 30, big_delta = 30, G = 0.040)
#> [1] 0.08850973

neumanComp <- NeumanCompartment$new()
neumanComp$get_signal(
  small_delta = 30, big_delta = 30, G = 0.040,
  echo_time = 40
)
#> [1] 1

callaghanComp <- CallaghanCompartment$new()
callaghanComp$get_signal(small_delta = 30, big_delta = 30, G = 0.040)
#> [1] 0.02624805

vanGelderenComp <- VanGelderenCompartment$new()
vanGelderenComp$get_signal(small_delta = 30, big_delta = 30, G = 0.040)
#> [1] 0.1205943

## ------------------------------------------------
## Method `BaseCompartment$get_parameter_names()`
## ------------------------------------------------

freeComp <- FreeCompartment$new()
freeComp$get_parameter_names()
#> [1] "FreeDiffusivity"

## ------------------------------------------------
## Method `BaseCompartment$get_parameters()`
## ------------------------------------------------

freeComp <- FreeCompartment$new()
freeComp$get_parameters()
#> $FreeDiffusivity
#> [1] 3
#> 
```
