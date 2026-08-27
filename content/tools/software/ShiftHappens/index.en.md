---
title: "ShiftHappens, a package for shift detection"
slug: "shifthappens"
---

[ShiftHappens](https://github.com/benRenard/ShiftHappens) is an R package for detecting, visualizing and estimating shifts, with a specific focus on hydrometric applications and stage-discharge rating shifts. The package builds on the work of [Mansanarez et al.](https://doi.org/10.1029/2018WR023389) (2019) and [Darienzo et al.](https://doi.org/10.1029/2020WR028607) (2021). 

As illustrated below, the package provides a segmentation procedure to split a data series into homogeneous subperiods. The method has been developed with the aim of accounting for data uncertainties, and providing the uncertainty around the estimated shift dates.

<p style="text-align: center;color: gray;">
<img src="Segmentation_Recursive.png" width="70%"> </br>
Segmentation of a data series into homogeneous subperiods (top), and uncertainty around the estimated shift dates, represented as probability density functions (bottom). 
</p>

The segmentation procedure can also be used to detect changes affecting the relation between two variables. When this relation is a rating curve linking the water level and the discharge in a river, this leads to a tool to detect rating shifts based on the (stage, discharge) gaugings, as illustrated below.

<p style="text-align: center;color: gray;">
<img src="Recursive_BaRatin.png" width="70%"> </br>
Identification of homogeneous rating curves (top), and uncertainty around the estimated shift dates, represented as probability density functions (bottom). 
</p>

The package also proposes a method to detect rating shifts based on the analysis of recessions. The key idea is the following: during long recession periods, the water level tends to the elevation of the riverbed. A shift in the lowest stage values reached during such recessions may hence suggest a change in the riverbed elevation (scouring or filling caused by a flood for instance), inducing a rating shift.

<p style="text-align: center;color: gray;">
<img src="recModel.png" width="45%"> <img src="recModel2.png" width="45%"></br>
Analysis of recessions for rating shift detection. The figure on the left illustrates the extraction of recessions periods (plotted from the start of the recession in the top panel and in absolute time in the bottom panel), the figure on the right illustrates the application of the segmentation procedure to the lowest stage values reached during each recession. 
</p>




