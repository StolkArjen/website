---
title: How can I check whether the grid that I have is aligned to the segmented volume and to the sensor gradiometer?
layout: default
tags: [faq, source, headmodel, seg]
---

## How can I check whether the grid that I have is aligned to the segmented volume and to the sensor gradiometer?

Having 'grid', 'vol', and 'grad', you can use the followin

    Hold on
    plot3(grid.pos(:,1),grid.pos(:,2),grid.pos(:,3),'.');
    ft_plot_vol(vol);
    ft_plot_sens(grad);
