# B-Value Calculation

A function to calculate the b-value for a given set of experimental
parameters.

## Usage

``` r
bvalue(small_delta, big_delta, G)
```

## Arguments

- small_delta:

  A numeric value specifying the duration of the gradient pulse in ms.

- big_delta:

  A numeric value specifying the duration between the gradient pulses in
  ms.

- G:

  A numeric value specifying the strength of the gradient in
  \\\mu\\T/\\\mu\\m.

## Value

A numeric value storing the predicted b-value in ms/\\\mu\\m\\^2\\.

## Examples

``` r
bvalue(small_delta = 30, big_delta = 30, G = 0.040)
#> [1] 2.061162
```
