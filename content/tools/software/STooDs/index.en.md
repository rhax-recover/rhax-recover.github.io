---
title: "STooDs: probabilistic models for data varying in space, time or other dimensions"
slug: "stoods"
---

<p style="text-align: center">
<a href="https://baratin-tools.github.io/fr/"> <img src="STooDs_logo.svg" width="30%"> </a>
</p>

**[STooDs](https://github.com/STooDs-tools) is a framework to build and estimate probabilistic models for data varying in Space, Time or other Dimensions.**

For instance, STooDs allows jointly analyzing hazards such as heatwaves, precipitation deficits and river droughts in a region. This analysis typically aims at estimating the probability of occurrence of extreme events (for each hazard separately or jointly for the three of them), how this probability varies in space, and how it changed in the past or it may change in the future.

A STooDs analysis is based on the following steps:

1. The target dataset contains the values taken by one of several predictand variables varying along one or more dimensions.
2. Each variable in the dataset is assumed to follow a distribution whose parameters may vary along the same dimensions as the dataset.
3. This variability is specified by regression formulas that may use parameters, covariates and hidden processes.
4. The resulting probabilistic model is estimated using Bayesian inference and can be used to estimate e.g. hazard levels. 

In terms of code, STooDs includes two main building blocks: the computational engine [STooDs](https://github.com/STooDs-tools/STooDs), a Fortran executable implementing the main steps of Bayesian inference, and the R package [RSTooDs](https://github.com/STooDs-tools/RSTooDs) that allows controlling this computational engine from [R](https://www.r-project.org/), hence facilitating model definition, data manipulation, and the exploitation of Bayesian inference results to compute estimates along with their uncertainties. The code includes functionalities such as large choice of distributions (including non-gaussian, discrete or continuous ones etc.), the possibility to use uncertain and incomplete data (e.g. historical floods), and the possibility to use 'hidden covariates' models (aka 'latent variables' or 'latent factors' models). Thanks to this flexibility, STooDs has been applied to a wide range of case study: [flood occurrences](https://doi.org/10.1029/2019WR024951) in France, [hot-and-dry](https://doi.org/10.1029/2021WR030007) summer conditions in Australia, [floods and intense precipitations](https://doi.org/10.1029/2022JD037908) at the global scale, or the joint use of [flood marks and hydrometric data](https://doi.org/10.1080/02626667.2023.2212165) to estimate ancient flood events in France, as illustrated in the video below (more details [here](https://globxblog.github.io/blog/reperes-de-crues/)).

<p style="text-align: center;color: gray;">
<iframe src="https://player.vimeo.com/video/815008124" frameborder="0" width="100%" height="440" allowfullscreen="allowfullscreen"></iframe> </br>
Estimation of ancient flood probabilities using STooDs.
</p>

