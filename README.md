# Sclass
Syntactic Sugar for S3 Classes in R

```r
> microbenchmark::microbenchmark(1:10, times = 10000)
Unit: nanoseconds
 expr min   lq    mean median   uq   max neval
 1:10 769 1676 1773.75   1677 1747 16693 10000
> `:` = function(a, b) UseMethod(":")
> `:.default` = .Primitive(":")
> 1:10
 [1]  1  2  3  4  5  6  7  8  9 10
> library("magrittr")
> `:.xk` = function(a, b) eval.parent(substitute(a %>% b))
> x:length()
[1] 1
> x:c(list(n = 99))
$a
[1] 100
$n
[1] 99
> microbenchmark::microbenchmark(1:10, times = 10000)
Unit: microseconds
 expr   min    lq     mean median    uq   max neval
 1:10 6.076 6.425 6.780402  6.564 6.704 61.32 10000
 ```
 
 Watch this space!
