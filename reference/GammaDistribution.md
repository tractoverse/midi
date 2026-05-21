# Gamma distribution class

This class defines the gamma distribution. It provides methods for
fitting the distribution to data and generating random samples.

## Super class

[`BaseDistribution`](https://tractoverse.github.io/midi/reference/BaseDistribution.md)
-\> `GammaDistribution`

## Methods

### Public methods

- [`GammaDistribution$new()`](#method-GammaDistribution-initialize)

- [`GammaDistribution$get_shape()`](#method-GammaDistribution-get_shape)

- [`GammaDistribution$get_scale()`](#method-GammaDistribution-get_scale)

- [`GammaDistribution$clone()`](#method-GammaDistribution-clone)

Inherited methods

- [`BaseDistribution$fit()`](https://tractoverse.github.io/midi/reference/BaseDistribution.html#method-fit)
- [`BaseDistribution$get_mean()`](https://tractoverse.github.io/midi/reference/BaseDistribution.html#method-get_mean)
- [`BaseDistribution$get_variance()`](https://tractoverse.github.io/midi/reference/BaseDistribution.html#method-get_variance)
- [`BaseDistribution$random()`](https://tractoverse.github.io/midi/reference/BaseDistribution.html#method-random)

------------------------------------------------------------------------

### `GammaDistribution$new()`

Creates a new gamma distribution.

#### Usage

    GammaDistribution$new(shape = 1, scale = 1)

#### Arguments

- `shape`:

  A numeric value specifying the shape parameter of the gamma
  distribution. Defaults to `1.0`.

- `scale`:

  A numeric value specifying the scale parameter of the gamma
  distribution. Defaults to `1.0`.

#### Returns

An instance of the gamma distribution as an object of class
`GammaDistribution`.

------------------------------------------------------------------------

### `GammaDistribution$get_shape()`

Retrieves the shape parameter of the gamma distribution.

#### Usage

    GammaDistribution$get_shape()

#### Returns

A numeric value storing the shape parameter of the gamma distribution.

------------------------------------------------------------------------

### `GammaDistribution$get_scale()`

Retrieves the scale parameter of the gamma distribution.

#### Usage

    GammaDistribution$get_scale()

#### Returns

A numeric value storing the scale parameter of the gamma distribution.

------------------------------------------------------------------------

### `GammaDistribution$clone()`

The objects of this class are cloneable with this method.

#### Usage

    GammaDistribution$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.

## Examples

``` r
gd <- GammaDistribution$new(
  shape = 1,
  scale = 5
)
gd$get_shape()
#> [1] 1
gd$get_scale()
#> [1] 5
gd$get_mean()
#> [1] 5
gd$get_variance()
#> [1] 25
gd$random(10)
#>  [1] 17.8360190  5.8395093  0.2872731  1.7020353 17.3578046  5.2183103
#>  [7] 15.1313753  1.8378476  0.4985022  3.9478935
gd$fit(gd$random(100))
gd$get_shape()
#> [1] 1.001781
gd$get_scale()
#> [1] 5.560486
```
