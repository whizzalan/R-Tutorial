Title
========================================================


```r
library(mgcv) #provides functions for generalized additive modelling
```

```
## Loading required package: nlme
## This is mgcv 1.7-29. For overview type 'help("mgcv-package")'.
```

```r
dat1 <- readRDS("C:\\Users\\GeorgeChao\\Documents\\study-area-statR\\dat1.rds")
# fit linear model
g1 <- lm(log10(總價)~面積+車位+屋齡+行政區+floor, data=dat1)
```

```
## Error: 找不到物件 '總價'
```

```r
# fit addiive model with two smooth terms
g2 <- gam(log10(總價)~s(面積)+車位+s(屋齡)+行政區+floor, data=dat1)
```

```
## Error: 找不到物件 '總價'
```

```r
# Compare adjusted R-squared, 越趨近1模型配適度越好
data.frame("linear model"=summary(g1)$adj.r.sq, "additive model"=summary(g2)$r.sq)
```

```
## Error: 找不到物件 'g1'
```
