---
layout: default
---

##  FT_WARP_OPTIM

Note that this reference documentation is identical to the help that is displayed in MATLAB when you type "help ft_warp_optim".

`<html>``<pre>`
    `<a href=/reference/ft_warp_optim>``<font color=green>`FT_WARP_OPTIM`</font>``</a>` determine intermediate positions using warping (deformation)
    the input cloud of points is warped to match the target.
    The strategy is to start with simpelest linear warp, followed by a more
    elaborate linear warp, which then is followed by the nonlinear warps up
    to the desired order.
 
    [result, M] = ft_warp_pnt(input, target, method)
      input          contains the Nx3 measured 3D positions
      target         contains the Nx3 template 3D positions
      method         should be any of 
                      'rigidbody'
                      'globalrescale'
                      'traditional' (default)
                      'nonlin1'
                      'nonlin2'
                      'nonlin3'
                      'nonlin4'
                      'nonlin5'
 
    The default warping method is a traditional linear warp with individual
    rescaling in each dimension. Optionally you can select a nonlinear warp
    of the 1st (affine) up to the 5th order.
 
    When available, this function will use the MATLAB optimization toolbox.
 
    See also `<a href=/reference/ft_warp_apply>``<font color=green>`FT_WARP_APPLY`</font>``</a>`, FT_WARP_ERRROR
`</pre>``</html>`

