
## R Markdown

``` r
op <- par(mfrow=c(2,3))
time <- 1:500

# p*():累積分布
Ft <- pweibull(time, shape = 2.5, scale = 250)
plot(time, Ft, type = 'l', ylab = 'F(t)', main = 'Cumulative Function')

# S(t) = 1 - F(t)
St <- 1 - Ft
plot(time, St, type = 'l', ylab = 'S(t)', main = 'Survival Function')

# d*():確率密度
ft <- dweibull(time, shape = 2.5, scale = 250)
plot(time, ft, type = 'l', ylab = 'f(t)', main = 'Probability density Function')

# 確率密度関数/生存関数=ハザード関数
ht <- ft/St
plot(time, ht, type = 'l', ylab = 'h(t)', main = 'Hazard Function')

# -Log(生存関数)=累積ハザード関数
Ht <- -1*log(St)
plot(time, Ht, type = 'l', ylab = 'H(t)', main = 'Cumlative Hazard Function')
```

![](test_files/figure-gfm/cars-1.png)<!-- -->

## math

with some more inline Latex
![\\gamma](https://latex.codecogs.com/png.latex?%5Cgamma "\gamma"),
![\\lambda](https://latex.codecogs.com/png.latex?%5Clambda "\lambda"),
![\\theta](https://latex.codecogs.com/png.latex?%5Ctheta "\theta").

![
E = mc^2
](https://latex.codecogs.com/png.latex?%0AE%20%3D%20mc%5E2%0A "
E = mc^2
")
