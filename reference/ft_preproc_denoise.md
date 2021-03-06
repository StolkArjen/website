---
layout: default
---

##  FT_PREPROC_DENOISE

Note that this reference documentation is identical to the help that is displayed in MATLAB when you type "help ft_preproc_denoise".

`<html>``<pre>`
    `<a href=/reference/ft_preproc_denoise>``<font color=green>`FT_PREPROC_DENOISE`</font>``</a>` performs a regression of the matrix dat onto
    refdat, and subtracts the projected data. This is for the 
    purpose of removing signals generated by coils during continuous
    head motion tracking, for example.
 
    Use as
    [dat] = ft_preproc_denoise(dat, refdat, hilbertflag)
    where
    dat         data matrix (Nchan1 X Ntime)
    refdat      data matrix (Nchan2 X Ntime)
    hilbertflag specifying to regress out the real and imaginary parts of 
                  the hilbert transformed signal. Only meaningful for narrow
                  band reference data
 
    See also PREPROC
`</pre>``</html>`

