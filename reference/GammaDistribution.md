# Gamma distribution class

This class defines the gamma distribution. It provides methods for
fitting the distribution to data and generating random samples.

## Super class

[`midi::BaseDistribution`](https://lmjl-alea.github.io/midi/reference/BaseDistribution.md)
-\> `GammaDistribution`

## Methods

### Public methods

- [`GammaDistribution$new()`](#method-GammaDistribution-new)

- [`GammaDistribution$get_shape()`](#method-GammaDistribution-get_shape)

- [`GammaDistribution$get_scale()`](#method-GammaDistribution-get_scale)

- [`GammaDistribution$clone()`](#method-GammaDistribution-clone)

Inherited methods

- [`midi::BaseDistribution$fit()`](https://lmjl-alea.github.io/midi/reference/BaseDistribution.html#method-fit)
- [`midi::BaseDistribution$get_mean()`](https://lmjl-alea.github.io/midi/reference/BaseDistribution.html#method-get_mean)
- [`midi::BaseDistribution$get_variance()`](https://lmjl-alea.github.io/midi/reference/BaseDistribution.html#method-get_variance)
- [`midi::BaseDistribution$random()`](https://lmjl-alea.github.io/midi/reference/BaseDistribution.html#method-random)

------------------------------------------------------------------------

### Method `new()`

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

### Method `get_shape()`

Retrieves the shape parameter of the gamma distribution.

#### Usage

    GammaDistribution$get_shape()

#### Returns

A numeric value storing the shape parameter of the gamma distribution.

------------------------------------------------------------------------

### Method `get_scale()`

Retrieves the scale parameter of the gamma distribution.

#### Usage

    GammaDistribution$get_scale()

#### Returns

A numeric value storing the scale parameter of the gamma distribution.

------------------------------------------------------------------------

### Method `clone()`

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
#>  [1]  5.18043045  8.20880969  1.83784759  0.49850219  3.94789349  0.01503439
#>  [7] 17.74877153  1.60394250  0.28604279  5.96272346
gd$fit(gd$random(100))
gd$get_shape()
#> [1] 1.047473
gd$get_scale()
#> [1] 5.274058
```
