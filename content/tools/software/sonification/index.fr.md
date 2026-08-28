---
title: "Des packages R pour la sonification"
slug: "sonification"
---

**La sonification est un procédé qui permet de transformer des données en sons, de la même façon que la visualisation transforme des données en images. Ceci permet de raconter l'histoire portée par les données en musique.**

L'équipe a développé deux packages R pour faciliter le processus de sonification et encourager la [mise en musique des données](https://hal.science/hal-03710340v1). Le package [musicXML](https://github.com/benRenard/musicXML) permet d'écrire une partition au [format musicXML](https://fr.wikipedia.org/wiki/MusicXML) en définissant une association entre les valeurs prises par les données et les propriétés des notes (en particulier leur hauteur, volume et durée). La vidéo ci-dessous est [un exemple](https://globxblog.github.io/blog/hydrology-basics-1/) d'utilisation de ce package, dans lequel les trois principaux flux hydrologiques impliqués dans la bilan en eau des bassins versants (précipitation, évapotranspiration et débit) contrôlent trois instruments de musique.

<p style="text-align: center;color: gray;">
<iframe src="https://player.vimeo.com/video/481648928" frameborder="0" width="100%" height="440" allowfullscreen="allowfullscreen"></iframe>
</p>

Le package [sequenceR](https://github.com/benRenard/sequenceR) permet quant à lui de déclencher des sons prédéfinis (à la manière d'un [séquenceur musical](https://fr.wikipedia.org/wiki/S%C3%A9quenceur_musical)) sur la base de critères définis à partir des données. La vidéo ci-dessous [explore ainsi l'évolution](https://globxblog.github.io/blog/fetedelascience2022/) des trois flux hydrologiques précédents au cours des dernières décénnies pour quelques bassins situés en France.

<p style="text-align: center;color: gray;">
<iframe src="https://player.vimeo.com/video/746451180" frameborder="0" width="100%" height="440" allowfullscreen="allowfullscreen"></iframe>
</p>

Pour plus d'exemples de sonification basés sur ces packages, vous pouvez consulter [ce blog](https://globxblog.github.io/) ou le site interactif [Hydrological Soundscapes](https://hydrologicalsoundscapes.github.io/).
