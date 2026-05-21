# Sample cylinder compartments

This function samples \\n\\ cylinder compartments with given axis,
radius and diffusivity distributions.

## Usage

``` r
rcylinders(
  n,
  axis_mean,
  radius_mean,
  diffusivity_mean,
  axis_concentration = Inf,
  radius_sd = 0,
  diffusivity_sd = 0,
  restricted_model = c("Callaghan", "Neuman", "Soderman", "Stanisz", "Van Gelderen")
)
```

## Arguments

- n:

  An integer value specifying the number of compartments to sample.

- axis_mean:

  A numeric value specifying the mean of the axis distribution.

- radius_mean:

  A numeric value specifying the mean of the radius distribution.

- diffusivity_mean:

  A numeric value specifying the mean of the diffusivity distribution.

- axis_concentration:

  A numeric value specifying the concentration of the axis distribution.
  Defaults to `Inf` in which case the axis is fixed to the mean value.

- radius_sd:

  A numeric value specifying the standard deviation of the radius
  distribution. Defaults to `0` in which case the radius is fixed to the
  mean value.

- diffusivity_sd:

  A numeric value specifying the standard deviation of the diffusivity
  distribution. Defaults to `0` in which case the diffusivity is fixed
  to the mean value.

- restricted_model:

  A character vector specifying the restricted diffusion model to use.
  Defaults to `callaghan`. Possible values are `callaghan`, `neuman`,
  `soderman`, `stanisz`, and `vangelderen`.

## Value

A list of \\n\\ cylinder compartments of class
[`CylinderCompartment`](https://tractoverse.github.io/midi/reference/CylinderCompartment.md).

## Details

The axis distribution is given by a mean and a concentration parameter
and the Dimroth-Watson distribution is used to sample values. The radius
and diffusivity distributions are given by a mean and a standard
deviation and the Gamma distribution is used to sample values. If the
concentration parameter is set to `Inf` the axis is fixed to the mean
value. If the standard deviation of the radius and diffusivity
distributions are set to `0` the radius and diffusivity are fixed to the
mean values. If all parameters are fixed, only one compartment is
sampled.

## Examples

``` r
# Sample 10 cylinder compartments with fixed axis, radius and diffusivity
# set.seed(42)
cyl_distr <- rcylinders(
  n = 10L,
  axis_mean = c(0, 0, 1),
  radius_mean = 5,
  diffusivity_mean = 3
)
```
