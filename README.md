# Simple Random

This is a collection of Julia functions to make
random things. Part of the `SimpleWorld` collection.

## Functions

### Random unit vector

`random_unit_vector(d)` returns a random `d`-dimensional unit vector.

### Random subsets

`random_subset` creates a random subset with the following variations:
+ `random_subset(A)`: create a random subset of `A`  with each element
included with probability 0.5.
+ `random_subset(A,k)`: create a random `k`-element
subset of `A`.
+ `random_subset(n)`: create a random subset of `1:n`.
+ `random_subset(n,k)`: create a random `k`-element
subset of `1:n`.

### Random selection

`random_choice` is used to select a number or object at random
according to some (finite, discrete distribution). We provide two
variants:

+ `random_choice(weights)` randomly chooses a value from `1` to `n`,
where `n` is the number of elements in `weights`. The probability
that `k` is chosen is proportional to `weights[k]`. The `weights`
must be nonnegative and not all zero.
+ `random_choice(dict)` choose a random key `k` from `dict` with weight
proportional to `dict[k]`. Thus, `dict` must be of type
`Dict{S, T<:Real}`.
