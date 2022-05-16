---
title: "Analyse des brevets liées à l'informatique par ADN"
subtitle: "Analyse de l’Innovation et Intelligence Technologique"
author: "Waris Radji, David Kamgang"
date: "2021-06-20"
---

# Introduction

Dans le cadre du cours d'Analyse de l'Innovation et d'Intelligence Technologique, ce rapport présente le résultat de notre analyse des brevets liées à l'informatique par ADN.

## Contextualisation

<img src="https://upload.wikimedia.org/wikipedia/commons/1/16/DNA_orbit_animated.gif" style="float:right!important; width:200px!important;"></img>

L'informatique par l'ADN est une branche émergente de l'informatique qui utilise l'ADN, la biochimie et le matériel de biologie moléculaire, au lieu de l'informatique électronique traditionnelle. La recherche et le développement dans ce domaine concernent la théorie, les expériences et les applications de l'informatique ADN. Bien que le domaine ait débuté par la démonstration d'une application informatique par Len Adleman en 1994, il s'est maintenant étendu à plusieurs autres voies telles que le développement de technologies de stockage, de modalités d'imagerie à l'échelle nanométrique, de contrôleurs synthétiques et de réseaux de réaction, etc.

### Résolution de problèmes de décision sur ADN

En utilisant des fragments de brins d'[ADN](https://fr.wikipedia.org/wiki/Acide_désoxyribo-nucléique), on peut [coder les contraintes d'une recherche](https://fr.wikipedia.org/wiki/Algorithmique) sous forme d'[enzymes](https://fr.wikipedia.org/wiki/Enzyme). Dans un processus d'assemblage et de duplication de bases désoxyribonucléiques, les fragments ne répondant pas aux contraintes du problème sont éliminés par ces enzymes. En fin de processus, il ne reste plus que des chaînes ADN contenant la solution au problème cherché.

Un système de calcul utilisant de l'ADN s’appuie sur des mécanismes de codage fondamentalement différents de ceux de l’ordinateur conventionnel : dans nos machines classiques, c’est la manipulation de charges électriques portés par des électrons au sein de dispositifs de commutation électroniques (transistors) qui matérialise l’information codée sous une forme binaire. Avec les ordinateurs à base d'ADN, l'information est traduite en termes d'unités chimiques de l'ADN.

Le principe du calcul avec un ordinateur à base d'ADN, consiste à synthétiser des séquences d'ADN particulières et de les laisser réagir dans un tube à essai.

Pour résoudre des problèmes de décision comme le célèbre [chemin hamiltonien](https://fr.wikipedia.org/wiki/Chemin_hamiltonien) (existe-t-il un chemin reliant tous les sommets d'un graphe donné ?), on élabore une solution d’ADN dans laquelle les molécules d’ADN encodent par convention chacun des chemins possibles entre deux points. Par un procédé alternant les étapes de séparation et d’amplification, on élimine alors les brins encodant un chemin qui utilise des arêtes absentes du graphe jusqu’à isoler une solution réalisable (n'empruntant que des arêtes existantes).

### Stockage de données numériques sur ADN

Aujourd'hui ce domaine voit essentiellement ses applications dans le stockage de données numériques sur ADN. Le stockage de données numériques sur ADN désigne le processus de codage et de décodage de données binaires vers et depuis des brins d'[ADN](https://fr.wikipedia.org/wiki/Acide_désoxyribonucléique) de synthèse.

Bien que l'ADN possède un potentiel énorme comme support de stockage en raison de sa grande densité de stockage, son utilisation pratique est pour le moment sévèrement limitée en raison de son coût élevé et de ses vitesses de lecture et d'écriture très lentes (les temps de réponse se comptent en minutes, heures ou jours, et non en microsecondes). Un avantage considérable est qu'il est possible d'encapsuler l'ADN dans des nanobilles de silice. En les stockant dans des capsules en acier inoxydable, on estime pouvoir obtenir une durée de vie de 50.000 ans.

En juin 2019, des scientifiques rapportent que les 16 Go de texte de la version anglaise de [Wikipédia](https://fr.wikipedia.org/wiki/Wikipédia) ont été codés avec succès en [ADN de synthèse](https://fr.wikipedia.org/w/index.php?title=ADN_de_synthèse&action=edit&redlink=1)


## Problématique

Bien que cette technologie soit très prometteuse, nous pouvons nous poser la question suivante : *Comment a évolué le secteur de l'ordinateur par ADN jusqu’aujourd’hui et quel seront ses évolutions à venir?* Afin de répondre à cette problématique, nous nous baserons sur des outils d'exploration de base de données.

# Méthodologie

## Outils

Nous avons principalement utilisé la base de donnée de brevets Orbit qui propose également des outils permettant de fouiller les données relatives aux brevets à travers différents outils statitistiques. Nous extrayons par la suite ces données de la plateforme afin de pouvoir rendre certains graphiques interactifs.

## ^Requête

Les bases de données de brevets permettent la saisie de requête afin de pouvoir filtrer les milliers de brevets qui s'y trouvent. Nous avons choisi de faire la requête à partir de mots clés et de code CPC[^cpc].

Le tableau ci-dessous présente l'évolution de notre réflexion :

| Requête                                                      | Nombre de brevets | Notes                                                        |
| ------------------------------------------------------------ | ----------------- | ------------------------------------------------------------ |
| `(G06N-003/123)/CPC`                                         | 327               | DNA computers, i.e. information processing using biological DNA |
| `(G11C-013/02)/CPC`                                          | 980               | Computer memory using DNA                                    |
| `( (G11C-013/02)/CPC OR (G06N-003/123)/CPC )`                | 1288              |                                                              |
| `( (DNA)/TI/AB AND (computer OR computing)/TI/AB )`          | 1199              | Recherche de mots clés dans le titre et les résumés des brevets |
| `( (DNA)/TI/AB AND (computer OR computing)/TI/AB ) OR ( (G11C-013/02)/CPC OR (G06N-003/123)/CPC )` | 2451              |                                                              |
| `( (DNA)/TI/AB AND (comput+)/TI/AB ) OR ( (G11C-013/02)/CPC OR (G06N-003/123)/CPC )` | 2636              | On remplace les mots clés `computer` et `computing` par tout les mots commençant par `comput` |

La dernière requête nous as permis de récolté 2636 brevets, ce qui semblait suffisant pour analyser ce domaine qui est de niche.

[^cpc]:
  La Classification coopérative des brevets (CPC) est une extension de la Classification internationale de brevets (CIB) et est gérée conjointement par l'OEB et l'Office des brevets et des marques des Etats-Unis. Elle est divisée en neuf sections, A-H et Y, à leur tour subdivisées en classes, sous-classes, groupes et sous-groupes. La CPC comporte environ 250 000 entrées de classification.

# Évolution temporelle du nombre de brevets

Étant donné que le domaine des ordinateurs par ADN à réellement fait son émergence en 1994[^tempo], nous allons essayer de voir, à partir de cette période, les tendances du marché de l'ordinateur par ADN jusqu'aujourd'hui en regardant combien de brevets ont été publiés dans ce domaine chaque année:

<iframe src="fig/couvtempo.html" scrolling="no" style="border:none;" seamless="seamless"  height="525" width="100%"></iframe>

Ce graphique nous montre que le domaine des ordinateurs par ADN à pris de l'ampleur, quelques années après son émergence historique en 1994. Ce pic à débuté en 2000, une époque où notre société à connu un bouleversement profond provoqué par l'essor des techniques numériques telles que l'informatique et le développement du réseau Internet. C'est notamment en l'an 2000 que l'Homme à commencer à coupler le numérique avec d'autres technologies, ce qu'on appelle le **NBIC**[^nbic].

En 2001, dans un rapport qu'ils remettent à la National Science Foundation, les Américains William S. Bainbridge et Mihail Roco créent l'acronyme NBIC pour désigner ce qu'ils considèrent comme la « nécessaire convergence » entre les nanotechnologies, les biotechnologies, l'informatique et les sciences cognitives, c'est-à-dire l’interconnexion entre l'étude de l'infiniment petit, la fabrication du vivant, les recherches en intelligence artificielle et celles menées sur le cerveau humain. Cette convergence exigeant des mises de fonds considérables, des stratégies de développement sont conjointement élaborées par les États et le monde industriel. De même que, chez les individus, les NBIC tendent à briser les frontières traditionnelles entre vie publique et vie privée, dans la sphère économico-politique, elles contribuent à associer de plus en plus étroitement le secteur public et le secteur privé.

Il est également possible d'observer une diminution des brevets publiées entre 2009 et 2015, une période qui correspond à l'avènement du Big data qui est lié au fait que l'ensemble des informations stockées et circulant dans le monde est devenu si volumineux qu'il exige de nouveaux outils. On peut alors que imaginé que les technologies d'ordinateurs par ADN sont devenus un peu obsolete car elles sont assez lentes d'utilisation, ce qui entre en contradiction avec le besoin d'obtenir de la puissance de calcul afin de traité rapidement les gigantesques flux de données.

Cette diminution à pris fin après 2015. La société à recommencer à avoir de l'intérêt pour le domaine des ordinateurs par ADN. Ce qui peut s'expliquer tout simplement que le phénomène de "hype" sur les Big Data à commencé à un peu se calmer à cette période, la société à commencé à réflechir sur l'impact que le Big Data pourrait avoir sur notre société.

Nous pouvons donc conclure que ce marché reste assez imprévisible, mais semble néanmoins être en accord avec les besoins du numérique.


[^tempo]:
  Notre requête trouve quelques brevets un peu avant 1994.

[^nbic]:
  Les nanotechnologies, biotechnologies, informatique et sciences cognitives (NBIC) sont un champ scientifique multidisciplinaire qui se situe au carrefour des nanotechnologies (N), des biotechnologies (B), des technologies de l'Information (I) et des sciences cognitives (C).

# Acteurs et répartition

## Couverture géographique






# Sources:

- [DNA computing](https://en.wikipedia.org/wiki/DNA_computing), From Wikipedia, the free encyclopedia
- [Digital Revolution](https://en.wikipedia.org/wiki/Digital_Revolution), From Wikipedia, the free encyclopedia

<p class="signoff">
  <a href="/">↑ Retour en haut</a>
</p>
