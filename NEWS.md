# rstpm2 1.4.2
    - Belatedly started the NEWS.md file
    - Update to bbmle (>= 1.0.20) required due to new export from that package
    - Possible breaking change: for the `predict()` functions for `stpm2` and `pstpm2`, the `keep.attributes` default has changed from `TRUE` to `FALSE`. Any code that used `predict()` and needs the `newdata` attributes should now add the `keep.attributes=TRUE` argument. The previous default was noisy.
    - To this point, the following models are available: 
      + `stpm2`: parametric generalised survival models, possibly with clustered data (Gamma frailties and normal random effects), relative survival, robust standard errors, rich post-estimation and plots.
      + `pstpm2`: penalised generalised survival models, possibly with clustered data (Gamma frailties and normal random effects), relative survival, robust standard errors, rich post-estimation and plots.
      + `aft`: parametric accelerated failure time models, with more limited post-estimation and plots.
	- Links for the generalised survival models include log-log, -logit, -probit, -log and Aranda-Ordaz.
    - Post-estimation for `stpm2` and `pstpm2` includes:
	  + Conditional survival ("surv"), linear predictor ("link"), cumulative hazard ("cumhaz"), hazard ("hazard"), log hazard ("loghazard"), probability density function ("density"), failure ("fail"), hazard ratio ("hr"), survival difference ("sdiff"), hazard difference ("hdiff"), mean survival ("meansurv"), mean survival differences ("meansurvdiff"), mean hazard ratio ("meanhr"), odds ("odds"), odds ratio ("or"), restricted mean survival time ("rmst"), attributable fractions ("af")
	  + Marginal survival ("margsurv"), marginal hazard ("marghaz"), attributable fractions ("af"), mean survival ("meanmargsurv")