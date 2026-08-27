---
title: "Sonification R Packages"
slug: "sonification"
---

**Sonification refers to the process of transforming data into sound, in the same way as visualization transforming data into images. This allows telling the story brought by the data in music.**

The team developed two R packages to ease the sonification process and encourage musical data storytelling. The [musicXML](https://github.com/benRenard/musicXML) package allows writing a musical score in [musicXML format](https://en.wikipedia.org/wiki/MusicXML) by defining a mapping between data values and note properties (in particular their pitch, volume and duration). The video below provides [an example](https://globxblog.github.io/blog/hydrology-basics-1/) based on this package, where the three main hydrological fluxes involved in the catchment water balance (precipitation, evapotranspiration and streamflow) control three musical instruments.

<p style="text-align: center;color: gray;">
<iframe src="https://player.vimeo.com/video/481648928" frameborder="0" width="100%" height="440" allowfullscreen="allowfullscreen"></iframe>
</p>

The package [sequenceR](https://github.com/benRenard/sequenceR) allows triggering  predefined sounds (as done by a [musical sequencer](https://en.wikipedia.org/wiki/Music_sequencer)) using data-based rules. The video below uses this principle to [explore the evolution](https://globxblog.github.io/blog/fetedelascience2022/) of the three hydrological fluxes above during the last few decades, for a few catchments in France.

<p style="text-align: center;color: gray;">
<iframe src="https://player.vimeo.com/video/746451180" frameborder="0" width="100%" height="440" allowfullscreen="allowfullscreen"></iframe>
</p>

Check out [this blog](https://globxblog.github.io/) for more sonification examples based on these packages. 

