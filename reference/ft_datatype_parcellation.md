---
layout: default
---

##  FT_DATATYPE_PARCELLATION

Note that this reference documentation is identical to the help that is displayed in MATLAB when you type "help ft_datatype_parcellation".

`<html>``<pre>`
    `<a href=/reference/ft_datatype_parcellation>``<font color=green>`FT_DATATYPE_PARCELLATION`</font>``</a>` describes the FieldTrip MATLAB structure for parcellated
    cortex-based data and atlases. A parcellation can either be indexed or probabilistic
    (see below).
 
    A parcellation describes the tissue types for each of the surface elements.
    Parcellations are often, but not always labeled. A parcellatoin can be used to
    estimate the activity from MEG data in a known region of interest. A surface-based
    atlas is basically a very detailled parcellation with an anatomical label for each
    vertex.
 
    An example of a surface based Brodmann parcellation looks like this
 
               pos: [8192x3]         positions of the vertices forming the cortical sheet
               tri: [16382x3]        triangles of the cortical sheet
          coordsys: 'ctf'            the (head) coordinate system in which the vertex positions are expressed
              unit: 'mm'             the units in which the coordinate system is expressed
          brodmann: [8192x1 uint8]   values from 1 to N, the value 0 means unknown
     brodmannlabel: {Nx1 cell}
 
    An alternative representation of this parcellation is
 
               pos: [8192x3]           positions of the vertices forming the cortical sheet
               tri: [16382x3]          triangles of the cortical sheet
          coordsys: 'ctf'              the (head) coordinate system in which the vertex positions are expressed
              unit: 'mm'               the units in which the coordinate system is expressed
   Brodmann_Area_1: [8192x1 logical]   binary map representing the voxels belonging to the specific area
   Brodmann_Area_2: [8192x1 logical]   binary map representing the voxels belonging to the specific area
   Brodmann_Area_3: [8192x1 logical]   binary map representing the voxels belonging to the specific area
   ...
 
    The examples above demonstrate that a parcellation can be indexed, i.e. consisting of
    subsequent integer numbers (1, 2, ...) or probabilistic, consisting of real numbers
    ranging from 0 to 1 that represent probabilities between 0% and 100%. An extreme case
    is one where the probability is either 0 or 1, in which case the probability can be
    represented as a binary or logical array.
 
    The only difference to the source data structure is that the parcellation structure
    contains the additional fields xxx and xxxlabel. See `<a href=/reference/ft_datatype_source>``<font color=green>`FT_DATATYPE_SOURCE`</font>``</a>` for further
    details.
 
    Required field
    - pos
 
    Optional field
    - tri, coordsys, unit
 
    Deprecated field
    - none
 
    Obsoleted field
    - none
 
    Revision histor
    (2012/latest) The initial version was defined in accordance with the representation of
    a voxel-based segmentation.
 
    See also `<a href=/reference/ft_datatype>``<font color=green>`FT_DATATYPE`</font>``</a>`, `<a href=/reference/ft_datatype_source>``<font color=green>`FT_DATATYPE_SOURCE`</font>``</a>`, `<a href=/reference/ft_datatype_segmentation>``<font color=green>`FT_DATATYPE_SEGMENTATION`</font>``</a>`
`</pre>``</html>`

