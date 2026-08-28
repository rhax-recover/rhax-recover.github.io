---
title: "STooDs: modèles probabilistes pour les données variant dans le temps, l'espace ou d'autres dimensions"
slug: "stoods"
---

<p style="text-align: center">
<a href="https://baratin-tools.github.io/fr/"> <img src="STooDs_logo.svg" width="30%"> </a>
</p>

**[STooDs](https://github.com/STooDs-tools) (Space, Time or other Dimensions) est un cadre générique pour construire et estimer des modèles probabilistes décrivant des données variant dans le temps, l'espace ou toute autre dimension.**

A titre d'exemple, STooDs permet d'analyser conjointement des aléas comme les vagues de chaleur, les sécheresses pluviométriques et les étiages en rivière au sein d'une région géographique. Cette analyse vise typiquement à estimer la probabilité d'occurrence d'événements extrêmes (séparément pour chaque aléa ou conjointement), comment cette probabilité varie dans l'espace, et comment elle a changé dans le passé ou elle pourrait évoluer dans le futur.

STooDs est basé sur les étapes suivantes :

1. Le jeu de données à analyser contient les valeurs prises par une ou plusieurs variables variant dans une ou plusieurs dimensions (temps, espace ou autre).
2. Pour chaque variable, une distribution doit être spécifiée, et les paramètres de cette distribution peuvent varier dans les mêmes dimensions que les données.
3. La variabilité des paramètres est décrire par des formules de régression qui peuvent faire intervenir des paramètres, des covariables ou des processus cachés.
4. Le modèle probabiliste ainsi construit est estimé par inférence Bayesienne et peut être utilisé pour estimer, par exemple, des niveaux de risque. 


En termes de code, STooDs se compose de deux briques logicielles : le coeur de calcul [STooDs](https://github.com/STooDs-tools/STooDs), un exécutable Fortran qui implémente les principales étapes de l'inférence Bayesienne, et le package R [RSTooDs](https://github.com/STooDs-tools/RSTooDs) qui permet de contrôler ce coeur de calcul depuis [R](https://www.r-project.org/), facilitant ainsi la définition du modèle, la manipulation des données, et l'exploitation des résultats de l’inférence Bayesienne pour produire des estimations et quantifier les incertitudes associées. Le code inclut des fonctionnalités telles qu'un large choix de distributions (dont des distributions non gaussiennes, discrètes ou continues, etc.), la possibilité d'intégrer des données incertaines et incomplètes (par exemple des crues historiques), et la possibilité d'utiliser des modèles à covariables cachées (aussi connus sous le nom 'modèles à variables/facteurs latents'). Grace à cette flexibilité, STooDs a été appliqué à un éventail de cas assez varié : [occurrence de crues](https://doi.org/10.1029/2019WR024951) en France, étés [chauds et secs](https://doi.org/10.1029/2021WR030007) en Australie, [crues et précipitations intenses](https://doi.org/10.1029/2022JD037908) à l'échelle globale, ou l'utilisation conjointe de [repères de crues et de données hydrométriques](https://doi.org/10.1080/02626667.2023.2212165) pour estimer des probabilités de crues anciennes en France, comme illustré dans la vidéo ci-dessous (plus de détails [ici](https://globxblog.github.io/blog/reperes-de-crues/)).

<p style="text-align: center;color: gray;">
<iframe src="https://player.vimeo.com/video/815008124" frameborder="0" width="100%" height="440" allowfullscreen="allowfullscreen"></iframe> </br>
Estimation de probabilités de crues anciennes en utilisant STooDs.
</p>

