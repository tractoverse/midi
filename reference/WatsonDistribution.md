# Watson distribution class

This class defines the Watson distribution. It provides methods for
fitting the distribution to data and generating random samples.

## Super class

[`BaseDistribution`](https://tractoverse.github.io/midi/reference/BaseDistribution.md)
-\> `WatsonDistribution`

## Methods

### Public methods

- [`WatsonDistribution$new()`](#method-WatsonDistribution-initialize)

- [`WatsonDistribution$get_axis()`](#method-WatsonDistribution-get_axis)

- [`WatsonDistribution$get_concentration()`](#method-WatsonDistribution-get_concentration)

- [`WatsonDistribution$clone()`](#method-WatsonDistribution-clone)

Inherited methods

- [`BaseDistribution$fit()`](https://tractoverse.github.io/midi/reference/BaseDistribution.html#method-fit)
- [`BaseDistribution$get_mean()`](https://tractoverse.github.io/midi/reference/BaseDistribution.html#method-get_mean)
- [`BaseDistribution$get_variance()`](https://tractoverse.github.io/midi/reference/BaseDistribution.html#method-get_variance)
- [`BaseDistribution$random()`](https://tractoverse.github.io/midi/reference/BaseDistribution.html#method-random)

------------------------------------------------------------------------

### `WatsonDistribution$new()`

Creates a new Watson distribution.

#### Usage

    WatsonDistribution$new(mu = c(0, 0, 1), kappa = 10)

#### Arguments

- `mu`:

  A numeric vector of length 3 specifying the mean direction of the
  Watson distribution. Defaults to `(0, 0, 1)`.

- `kappa`:

  A numeric value specifying the concentration parameter of the Watson
  distribution. Defaults to `10.0`.

#### Returns

An instance of the Watson distribution as an object of class
`WatsonDistribution`.

------------------------------------------------------------------------

### `WatsonDistribution$get_axis()`

Retrieves the mean axis of the Watson distribution.

#### Usage

    WatsonDistribution$get_axis()

#### Returns

A numeric vector of length 3 storing the mean axis of the Watson
distribution.

------------------------------------------------------------------------

### `WatsonDistribution$get_concentration()`

Retrieves the concentration parameter of the Watson distribution.

#### Usage

    WatsonDistribution$get_concentration()

#### Returns

A numeric value storing the concentration parameter of the Watson
distribution.

------------------------------------------------------------------------

### `WatsonDistribution$clone()`

The objects of this class are cloneable with this method.

#### Usage

    WatsonDistribution$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.

## Examples

``` r
wd <- WatsonDistribution$new(
  mu = c(0, 0, 1),
  kappa = 10
)
wd$get_axis()
#> [1] 0 0 1
wd$get_concentration()
#> [1] 10
wd$random(10)
#> [[1]]
#> [1] -0.13237162  0.02374105  0.99091580
#> 
#> [[2]]
#> [1] 0.08423882 0.41784704 0.90460360
#> 
#> [[3]]
#> [1]  0.7947338 -0.0201646  0.6066230
#> 
#> [[4]]
#> [1] 0.08169297 0.07219491 0.99403931
#> 
#> [[5]]
#> [1] 0.1757129 0.1309836 0.9756886
#> 
#> [[6]]
#> [1] -0.107719805 -0.001532592  0.994180112
#> 
#> [[7]]
#> [1] -0.08345784 -0.34058075  0.93650389
#> 
#> [[8]]
#> [1]  0.02291961 -0.07663694  0.99679560
#> 
#> [[9]]
#> [1] -0.1305185  0.1437479  0.9809697
#> 
#> [[10]]
#> [1] 0.2882047 0.2054522 0.9352686
#> 
wd$fit(wd$random(100))
wd$get_axis()
#> [1]  0.03407031  0.04412166 -0.99844504
wd$get_concentration()
#> [1] 9.508437
```
