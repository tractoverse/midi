# Base distribution class

This class defines the base distribution class from which all other
distributions inherit. It provides a common interface for fitting the
distribution to data and generating random samples.

## Methods

### Public methods

- [`BaseDistribution$fit()`](#method-BaseDistribution-fit)

- [`BaseDistribution$random()`](#method-BaseDistribution-random)

- [`BaseDistribution$get_mean()`](#method-BaseDistribution-get_mean)

- [`BaseDistribution$get_variance()`](#method-BaseDistribution-get_variance)

- [`BaseDistribution$clone()`](#method-BaseDistribution-clone)

------------------------------------------------------------------------

### Method `fit()`

Fit the distribution to the data.

#### Usage

    BaseDistribution$fit(x)

#### Arguments

- `x`:

  A numeric vector of data to fit the distribution to.

#### Returns

Internally sets the parameters of the distribution. Returns nothing.

------------------------------------------------------------------------

### Method `random()`

Generate random samples from the distribution.

#### Usage

    BaseDistribution$random(n)

#### Arguments

- `n`:

  An integer specifying the number of samples to generate.

#### Returns

A numeric vector of size `n` containing the random samples.

------------------------------------------------------------------------

### Method `get_mean()`

Compute the mean of the distribution.

#### Usage

    BaseDistribution$get_mean()

#### Returns

A numeric value storing the mean of the distribution.

------------------------------------------------------------------------

### Method `get_variance()`

Compute the variance of the distribution.

#### Usage

    BaseDistribution$get_variance()

#### Returns

A numeric value storing the variance of the distribution.

------------------------------------------------------------------------

### Method `clone()`

The objects of this class are cloneable with this method.

#### Usage

    BaseDistribution$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
