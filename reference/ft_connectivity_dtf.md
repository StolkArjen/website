---
layout: default
---

##  FT_CONNECTIVITY_DTF

Note that this reference documentation is identical to the help that is displayed in MATLAB when you type "help ft_connectivity_dtf".

`<html>``<pre>`
    `<a href=/reference/ft_connectivity_dtf>``<font color=green>`FT_CONNECTIVITY_DTF`</font>``</a>` computes the directed transfer function.
 
    Use as
    [d, v, n] = ft_connectivity_dtf(h, ...)
 
    The input data h should be a spectral transfer matrix organized as
    Nrpt x Nchan x Nchan x Nfreq (x Ntime),
    where Nrpt can be 1.
 
    Additional optional input arguments come as key-value pair
    'hasjack'  = 0 (default) is a boolean specifying whether the input
                 contains leave-one-outs, required for correct variance
                 estimate.
    'feedback' = string, determining verbosity (default = 'none'), see `<a href=/reference/ft_progress>``<font color=green>`FT_PROGRESS`</font>``</a>`
    'crsspctrm' = matrix containing the cross-spectral density. If this
                  matrix is defined, the function
                  returns the ddtf, which requires an estimation of partial
                  coherence from this matrix.
    'invfun'   = 'inv' (default) or 'pinv', the function used to invert the
                 crsspctrm matrix to obtain the partial coherence. Pinv is
                 useful if the data are poorly-conditioned.
 
 
    Output argument
    d = partial directed coherence matrix Nchan x Nchan x Nfreq (x Ntime).
        If multiple observations in the input, the average is returned.
    v = variance of d across observations.
    n = number of observations.
 
    Typically, nrpt should be 1 (where the spectral transfer matrix is computed across
    observations. When nrpt&gt;1 and hasjack is true the input is assumed to contain the
    leave-one-out estimates of H, thus a more reliable estimate of the relevant
    quantities.
 
    See also `<a href=/reference/ft_connectivityanalysis>``<font color=green>`FT_CONNECTIVITYANALYSIS`</font>``</a>`
`</pre>``</html>`

