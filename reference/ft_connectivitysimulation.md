---
layout: default
---

##  FT_CONNECTIVITYSIMULATION

Note that this reference documentation is identical to the help that is displayed in MATLAB when you type "help ft_connectivitysimulation".

`<html>``<pre>`
    `<a href=/reference/ft_connectivitysimulation>``<font color=green>`FT_CONNECTIVITYSIMULATION`</font>``</a>` simulates channel-level time-series data with a
    specified connectivity structure. This function returns an output data
    structure that resembles the output of `<a href=/reference/ft_preprocessing>``<font color=green>`FT_PREPROCESSING`</font>``</a>`.
 
    Use as
    [data] = ft_connectivitysimulation(cfg)
 
    where the configuration structure should contai
    cfg.method      = string, can be 'linear_mix', 'mvnrnd', 'ar', 'ar_reverse' (see below)
    cfg.nsignal     = scalar, number of signals
    cfg.ntrials     = scalar, number of trials
    cfg.triallength = in seconds
    cfg.fsample     = in Hz
 
    Depending on the specific method that is selected, the configuration
    may also contai
 
    Method 'linear_mix' implements a linear mixing with optional time shifts
    where the number of unobserved signals can be different from the number
    of observed signals
 
    Required cfg option
    cfg.mix    = matrix, [nsignal x number of unobserved signals]
                 specifying the mixing from the unobserved signals to
                 the observed signals, or
               = matrix, [nsignal x number of unobserved signals x number of
                 samples] specifying the mixing from the
                 unobserved signals to the observed signals which
                 changes as a function of time within the trial
               = cell-arry, [1 x ntrials] with each cell a matrix as
                 specified above, when a trial-specific mixing is
                 required
    cfg.delay  = matrix, [nsignal x number of unobserved signals]
                 specifying the time shift (in samples) between the
                 unobserved signals and the observed signals
 
    Optional cfg option
    cfg.bpfilter  = 'yes' (or 'no')
    cfg.bpfreq    = [bplow bphigh] (default: [15 25])
    cfg.demean    = 'yes' (or 'no')
    cfg.baselinewindow = [begin end] in seconds, the default is the complete trial
    cfg.absnoise  = scalar (default: 1), specifying the standard deviation of
                    white noise superimposed on top of the simulated signals
    cfg.randomseed = 'yes' or a number or vector with the seed value (default = 'yes')
 
    Method 'mvnrnd' implements a linear mixing with optional timeshifts in
    where the number of unobserved signals is equal to the number of observed
    signals. This method used the MATLAB function mvnrnd. The implementation
    is a bit ad-hoc and experimental, so users are discouraged to apply it.
    The time shift occurs only after the linear mixing, so the effect of the
    parameters on the simulation is not really clear. This method will be
    disabled in the future.
 
    Required cfg option
    cfg.covmat    = covariance matrix between the signals
    cfg.delay     = delay vector between the signals in samples
 
    Optional cfg option
    cfg.bpfilter  = 'yes' (or 'no')
    cfg.bpfreq    = [bplow bphigh] (default: [15 25])
    cfg.demean    = 'yes' (or 'no')
    cfg.baselinewindow = [begin end] in seconds, the default is the complete trial
    cfg.absnoise  = scalar (default: 1), specifying the standard
                    deviation of white noise superimposed on top
                    of the simulated signals
 
    Method 'ar' implements a multivariate autoregressive model to generate
    the data.
 
    Required cfg option
    cfg.params   = matrix, [nsignal x nsignal x number of lags] specifying the
                   autoregressive coefficient parameters. A non-zero
                   element at cfg.params(i,j,k) means a
                   directional influence from signal j onto
                   signal i (at lag k).
    cfg.noisecov = matrix, [nsignal x nsignal] specifying the covariance
                   matrix of the innovation process
 
    Method 'ar_reverse' implements a multivariate autoregressive
    autoregressive model to generate the data, where the model coefficients
    are reverse-computed, based on the interaction pattern specified.
 
    Required cfg option
    cfg.coupling = nxn matrix, specifying coupling strength, rows causing
                    column
    cfg.delay    = nxn matrix, specifying the delay, in seconds, from one
                    signal's spectral component to the other signal, rows
                    causing column
    cfg.ampl     = nxn matrix, specifying the amplitude 
    cfg.bpfreq   = nxnx2 matrix, specifying the lower and upper frequencies
                    of the bands that are transmitted, rows causing column
 
    The generated signals will have a spectrum that is 1/f + additional
    band-limited components, as specified in the cfg.
 
    See also `<a href=/reference/ft_freqsimulation>``<font color=green>`FT_FREQSIMULATION`</font>``</a>`, `<a href=/reference/ft_dipolesimulation>``<font color=green>`FT_DIPOLESIMULATION`</font>``</a>`, `<a href=/reference/ft_spikesimulation>``<font color=green>`FT_SPIKESIMULATION`</font>``</a>`,
    `<a href=/reference/ft_connectivityanalysis>``<font color=green>`FT_CONNECTIVITYANALYSIS`</font>``</a>`
`</pre>``</html>`

