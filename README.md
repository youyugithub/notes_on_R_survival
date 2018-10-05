# notes_on_R_survival
notes on R survival

```
f <- rexp(1000, rate = 2)
c <- rexp(1000)
t <- pmin(f, c)
d <- ifelse(c < f, 0, 1)
sdat <- data.frame(time = t, delta = d)


# weibull: rweibull(n, shape, scale)

hist(calculate_AR_vector(mat1,ll3[1]),breaks=0:300+0.5)
calculate_AR_vector(mat2,ll3[2])
calculate_AR_vector(mat3,ll3[3])

range(calculate_AR_vector(mat1,ll3[1]))

> expfit <- survreg(Surv(time, delta) ~ 1, data = sdat, dist = "exponential")
> weibfit <- survreg(Surv(time, delta) ~ 1, data = sdat, dist = "weibull")
> llogfit <- survreg(Surv(time, delta) ~ 1, data = sdat, dist = "loglogistic")
```
