---
layout: default
---

##  FT_PLOT_TEXT

Note that this reference documentation is identical to the help that is displayed in MATLAB when you type "help ft_plot_text".

`<html>``<pre>`
    `<a href=/reference/ft_plot_text>``<font color=green>`FT_PLOT_TEXT`</font>``</a>` helper function for plotting text, which can also be used in
    combination with the multiple channel layout display in FieldTrip.
 
    Use as
    ft_plot_text(X, Y, str, ...)
 
    Optional arguments should come in key-value pairs and can include
    'fontcolor'           = string, color specification (default = 'k')
    'fontsize'            = number, sets the size of the text (default = 10)
    'fontunits'           =
    'fontname'            =
    'fontweight'          =
    'horizontalalignment' =
    'verticalalignment'   =
    'interpreter'         = string, can be 'none', 'tex' or 'latex' (default = 'none')
    'rotation'            =
    'tag'                 = string, the name assigned to the object. All tags with the same name can be deleted in a figure, without deleting other parts of the figure.
 
    It is possible to plot the object in a local pseudo-axis (c.f. subplot), which is specfied as follows
    'hpos'                = horizontal position of the center of the local axes
    'vpos'                = vertical position of the center of the local axes
    'width'               = width of the local axes
    'height'              = height of the local axes
    'hlim'                = horizontal scaling limits within the local axes
    'vlim'                = vertical scaling limits within the local axes
 
    Example
    figure
    ft_plot_vector(randn(1,10), rand(1,10), 'hpos', 1, 'vpos', 1, 'width', 0.2, 'height', 0.2, 'box', true)
    ft_plot_text(0, 0 , '+',                'hpos', 1, 'vpos', 1, 'width', 0.2, 'height', 0.2)
    axis([0 2 0 2])
 
    See also `<a href=/reference/ft_plot_vector>``<font color=green>`FT_PLOT_VECTOR`</font>``</a>`, `<a href=/reference/ft_plot_matrix>``<font color=green>`FT_PLOT_MATRIX`</font>``</a>`, `<a href=/reference/ft_plot_line>``<font color=green>`FT_PLOT_LINE`</font>``</a>`, `<a href=/reference/ft_plot_box>``<font color=green>`FT_PLOT_BOX`</font>``</a>`
`</pre>``</html>`

