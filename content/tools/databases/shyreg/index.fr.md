---
title: "SHYREG : quantiles de pluies et de débits en tout point du territoire"
slug: "shyreg"
---

**SHYREG désigne une méthode d'estimation des pluies et des crues de forte période de retour, et les deux bases de données qui en sont issues : [SHYREG Pluie](https://shyreg.pluie.recover.inrae.fr/), qui donne des quantiles de pluies sur une grille régulière, et [SHYREG Débit](https://shyreg.recover.inrae.fr/), qui donne des quantiles de débits aux exutoires de bassins versants, y compris non jaugés.**

On peut par exemple y lire la pluie centennale en 1 heure sur n'importe quel kilomètre carré de la métropole, ou le débit de pointe décennal d'un petit cours d'eau sans station hydrométrique. Ces valeurs servent notamment au dimensionnement d'ouvrages, à la cartographie de l'aléa inondation et aux études de risque.

Les bases de données sont créées à partir de sorties du générateur SHYPRE au pas de temps horaire, elles sont régionalisées pour être projetées sur des mailles d'une grille régulière. Les quantiles de pluies, pour une gamme de durées allant de 5 minutes à 72 heures, sont calculés sur ces chroniques simulées : c'est le contenu de SHYREG Pluie. Les pluies simulées passent ensuite dans un modèle pluie-débit, et les débits obtenus sont agrégés à l'échelle du bassin versant : c'est le contenu de SHYREG Débit.

Les deux bases sont accessibles via des applications web développées avec [Shiny](https://shiny.posit.co/) en collaboration avec [Hydris hydrologie](https://www.hydris-hydrologie.fr/), qui partagent la même organisation. L'onglet **Interactive Map** affiche une carte sur laquelle un clic sur un pixel ou un exutoire fait apparaître ses quantiles, sous forme de tableau et de courbe Intensité-Durée-Fréquence. L'onglet **Data Explorer** permet de retrouver des pixels ou des bassins versants à partir d'un département, d'une commune ou d'un nom de cours d'eau. L'onglet **Data Export**, dont l'accès dépend des droits de l'utilisateur, sert à extraire les quantiles d'un ensemble de points (issus d'une recherche, d'un polygone tracé sur la carte, ou d'un exutoire et de ceux situés dans son bassin) au format .csv ou excel.

<p style="text-align: center;color: gray;">
<img src="SHYREG_debit_screenshot.png" width="100%"> </br>
Onglet Interactive Map de l'application SHYREG Débit.
</p>

| | SHYREG Pluie | SHYREG Débit |
|---|---|---|
| Support | Pixels d'une grille régulière (500 m ou 1 km selon la zone) | Exutoires des bases HYDRO, BNBV et CVH |
| Variables | Cumuls de pluie de 5 min à 72 h | Débit de pointe (QP), débit moyen sur 6 h (LM6) et sur 1 jour (L1J) |
| Périodes de retour | 2 à 1000 ans | Plusieurs périodes de retour |
| Zones couvertes | Métropole, La Réunion, Antilles, Nouvelle-Calédonie | Métropole, Martinique |
| Incertitude | Bornes de l'intervalle de confiance à 70 % | — |

Dans les fichiers exportés, les colonnes de pluie sont nommées `PM[durée].[période]` (`PM01.0010` : pluie maximale en 1 h, période de retour 10 ans) et les colonnes de débit `[durée]_[période]` (`QP_2` : débit de pointe biennal ; `LM6_10` : débit moyen sur 6 h décennal).

La méthode est décrite en détail dans la [notice SHYREG](https://shyreg.recover.inrae.fr/Notice_SHYREG.pdf).

Contact : [Patrick Arnaud](mailto:patrick.arnaud@inrae.fr)
