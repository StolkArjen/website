---
layout: default
---

##  FT_PLOT_ORTHO

Note that this reference documentation is identical to the help that is displayed in MATLAB when you type "help ft_plot_ortho".

`<html>``<pre>`
    `<a href=/reference/ft_plot_ortho>``<font color=green>`FT_PLOT_ORTHO`</font>``</a>` plots 3 orthographic cuts through a 3-D volume and interpolates if needed
 
    Use as
    ft_plot_ortho(dat, ...)
    or
    ft_plot_ortho(dat, mask, ...)
    where dat and mask are equal-sized 3-D arrays.
 
    Additional options should be specified in key-value pairs and can be
    'style'        = string, 'subplot' or 'intersect' (default = 'subplot')
    'orientation'  = 3x3 matrix specifying the directions orthogonal through the planes which will be plotted
    'parents'      = (optional) 3-element vector containing the handles of the axes for the subplots (when style = 'subplot')
    'surfhandle'   = (optional) 3-element vector containing the handles of the surfaces for each of the sublots (when style = 'subplot'). Parents and surfhandle are mutually exclusive
    'update'       = (optional) 3-element boolean vector with the axes that should be updated (default = [true true true])
 
    The following options are supported and passed on to `<a href=/reference/ft_plot_slice>``<font color=green>`FT_PLOT_SLICE`</font>``</a>`
    'clim'                = [min max], lower and upper color limits
    'transform'           = 4x4 homogeneous transformation matrix specifying the mapping from voxel space to the coordinate system in which the data are plotted
    'location'            = 1x3 vector specifying a point on the plane which will be plotted the coordinates are expressed in the coordinate system in which the data will be plotted. location defines the origin of the plane
    'datmask'             = 3D-matrix with the same size as the matrix dat, serving as opacitymap if the second input argument to the function contains a matrix, this will be used as the mask
    'maskstyle'           = string, 'opacity' or 'colormix', defines the rendering
    'background'          = needed when maskstyle is 'colormix', 3D-matrix with
                            the same size as the data matrix, serving as
                            grayscale image that provides the background
    'interpmethod'        = string specifying the method for the interpolation, see INTERPN (default = 'nearest')
    'colormap'            = string, see COLORMAP
    'unit'                = string, can be 'm', 'cm' or 'mm (default is automatic)
    'intersectmesh'       = triangulated mesh, see `<a href=/reference/ft_prepare_mesh>``<font color=green>`FT_PREPARE_MESH`</font>``</a>`
    'intersectcolor'      = string, color specification
    'intersectlinestyle'  = string, line specification 
    'intersectlinewidth'  = number
 
    See also `<a href=/reference/ft_plot_slice>``<font color=green>`FT_PLOT_SLICE`</font>``</a>`, `<a href=/reference/ft_plot_montage>``<font color=green>`FT_PLOT_MONTAGE`</font>``</a>`, `<a href=/reference/ft_sourceplot>``<font color=green>`FT_SOURCEPLOT`</font>``</a>`
`</pre>``</html>`

