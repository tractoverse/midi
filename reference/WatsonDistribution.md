# Watson distribution class

This class defines the Watson distribution. It provides methods for
fitting the distribution to data and generating random samples.

## Super class

[`midi::BaseDistribution`](https://lmjl-alea.github.io/midi/reference/BaseDistribution.md)
-\> `WatsonDistribution`

## Methods

### Public methods

- [`WatsonDistribution$new()`](#method-WatsonDistribution-new)

- [`WatsonDistribution$get_axis()`](#method-WatsonDistribution-get_axis)

- [`WatsonDistribution$get_concentration()`](#method-WatsonDistribution-get_concentration)

- [`WatsonDistribution$clone()`](#method-WatsonDistribution-clone)

Inherited methods

- [`midi::BaseDistribution$fit()`](https://lmjl-alea.github.io/midi/reference/BaseDistribution.html#method-fit)
- [`midi::BaseDistribution$get_mean()`](https://lmjl-alea.github.io/midi/reference/BaseDistribution.html#method-get_mean)
- [`midi::BaseDistribution$get_variance()`](https://lmjl-alea.github.io/midi/reference/BaseDistribution.html#method-get_variance)
- [`midi::BaseDistribution$random()`](https://lmjl-alea.github.io/midi/reference/BaseDistribution.html#method-random)

------------------------------------------------------------------------

### Method `new()`

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

### Method `get_axis()`

Retrieves the mean axis of the Watson distribution.

#### Usage

    WatsonDistribution$get_axis()

#### Returns

A numeric vector of length 3 storing the mean axis of the Watson
distribution.

------------------------------------------------------------------------

### Method `get_concentration()`

Retrieves the concentration parameter of the Watson distribution.

#### Usage

    WatsonDistribution$get_concentration()

#### Returns

A numeric value storing the concentration parameter of the Watson
distribution.

------------------------------------------------------------------------

### Method `clone()`

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
#> [1] -0.1305185  0.1437479  0.9809697
#> 
#> [[2]]
#> [1] 0.2882047 0.2054522 0.9352686
#> 
#> [[3]]
#> [1] -0.3405410 -0.1093761  0.9338462
#> 
#> [[4]]
#> [1] -0.07887883  0.27967791  0.95684816
#> 
#> [[5]]
#> [1] -0.1012958 -0.1123559  0.9884914
#> 
#> [[6]]
#> [1] -0.0726425  0.8331471  0.5482600
#> 
#> [[7]]
#> [1] 0.2639347 0.1784568 0.9478880
#> 
#> [[8]]
#> [1]  0.0006495886 -0.4170701965  0.9088740447
#> 
#> [[9]]
#> [1] -0.02479583  0.35059414  0.93619919
#> 
#> [[10]]
#> [1] -0.2105415 -0.2716214  0.9390922
#> 
wd$fit(wd$random(100))
wd$get_axis()
#> [1]  0.02163945  0.03845331 -0.99902606
wd$get_concentration()
#> [1] 10.15158
```
