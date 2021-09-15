# Mémoire du Master "Technologies numériques appliquées à l'histoire"

## Médiation des données de la recherche
### *Élaboration d’une plateforme en ligne pour une base de tables astronomiques anciennes*
Ce mémoire a été réalisé dans le cadre d'un stage à l'Observatoire de Paris du mois d'avril à août 2019, dans le cadre du Master "Technologies numériques appliquées à l'histoire" de l'École des chartes. Il porte sur les procédés de médiation pouvant être mis en œuvre dans la valorisation d'un corpus de recherche numérique.

Il expose les étapes de conception d'une plateforme publique pour le projet de recherche DISHAS, depuis l'analyse du corpus jusqu'à la réalisation technique des interfaces. Le corpus de recherche de DISHAS porte sur les ressources de l'astronomie de tradition ptoléméenne ; il comporte une grande variété de données – ayant trait autant aux mathématiques qu'à la codicologie – pour lesquelles il a fallu concevoir des interfaces et visualisations spécifiques. Ce mémoire vise à apporter une analyse critique des enjeux, méthodes et résultats liés à la conception d'une plateforme publique de recherche.

# Table des matières
### Résumé . . . . . . . . . . . . . . . . . . . . . . . . . . . . . iii
### Remerciements . . . . . . . . . . . . . . . . . . . . . . . . . . . . . v
### Introduction . . . . . . . . . . . . . . . . . . . . . . . . . . . . . xvii
## I Production, nature et méthode d’acquisition de la donnée . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 1
### 1 Le projet DISHAS 3
#### 1.1 Présentation du projet . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 3
##### 1.1.1 Objectifs du projet . . . . . . . . . . . . . . . . . . . . . . . . . . . 3
##### 1.1.2 Collaboration au sein du projet . . . . . . . . . . . . . . . . . . . . 5
#### 1.2 Projets de recherche en histoire de l’astronomie . . . . . . . . . . . . . . . 7
##### 1.2.1 Le projet ALFA . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 7
##### 1.2.2 Autres projets : description des ressources en ligne . . . . . . . . . 9
### 2 Corpus de recherche 13
#### 2.1 Bornes historiques du corpus . . . . . . . . . . . . . . . . . . . . . . . . . . 13
##### 2.1.1 Ptolémée et l’Almageste . . . . . . . . . . . . . . . . . . . . . . . . 13
##### 2.1.2 Propagation du modèle ptoléméen . . . . . . . . . . . . . . . . . . 14
#### 2.2 Nature documentaire du corpus . . . . . . . . . . . . . . . . . . . . . . . . 16
##### 2.2.1 Les sources primaires astronomiques . . . . . . . . . . . . . . . . . 16
##### 2.2.2 Les paramètres . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 18
### 3 Numérisation et accueil de la donnée 21
#### 3.1 Modélisation de la donnée . . . . . . . . . . . . . . . . . . . . . . . . . . . 21
##### 3.1.1 Les sources historiques . . . . . . . . . . . . . . . . . . . . . . . . . 23
##### 3.1.2 Structuration des données d’édition . . . . . . . . . . . . . . . . . . 24
##### 3.1.3 Développements futurs de la base de donnée . . . . . . . . . . . . . 28
#### 3.2 Données de gestion et encodage de l’information . . . . . . . . . . . . . . . 29
##### 3.2.1 Données structurelles . . . . . . . . . . . . . . . . . . . . . . . . . . 29
##### 3.2.2 Encodage et typologie de la donnée . . . . . . . . . . . . . . . . . . 30
#### 3.3 Saisie de la donnée . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 32
##### 3.3.1 Interface administrateur . . . . . . . . . . . . . . . . . . . . . . . . 32
##### 3.3.2 Saisie assistée de tables astronomiques : présentation de DTI . . . . 34
## II Modalités d’exposition de la donnée 37
### 4 Analyse des besoins 39
#### 4.1 Définition des publics . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 39
##### 4.1.1 Chercheurs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 39
##### 4.1.2 Non-spécialistes . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 41
##### 4.1.3 Ingénieurs numériques . . . . . . . . . . . . . . . . . . . . . . . . . 42
#### 4.2 Enjeux liés à la donnée . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 43
##### 4.2.1 Contraintes qualitatives . . . . . . . . . . . . . . . . . . . . . . . . 43
##### 4.2.2 Spécificités des données de DISHAS . . . . . . . . . . . . . . . . . . . . . . . .  44
#### 4.3 Constitution d’une interface publique . . . . . . . . . . . . . . . . . . . . . . . .  46
##### 4.3.1 Objectifs d’une interface publique . . . . . . . . . . . . . . . . . . . . . . . .  46
##### 4.3.2 Notions d’expérience utilisateur . . . . . . . . . . . . . . . . . . . . . . . . .  47
##### 4.3.3 Constitution d’un parcours de navigation . . . . . . . . . . . . . . . . . . . . .  48
### 5 Médiation pour les publics non-spécialistes . . . . . . . . . . . . . . . . . . . . . . . 53
#### 5.1 Garantir l’ouverture à des publics non-spécialistes . . . . . . . . . . . . . . . . .  53
##### 5.1.1 Organisation de l’information comme vecteur de compréhension . . . . . . . . . . .  53
##### 5.1.2 Nécessité du contenu éditorialisé . . . . . . . . . . . . . . . . . . . . . . . . . 55
#### 5.2 Attractivité des contenus . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .  58
##### 5.2.1 Cohérence des interfaces . . . . . . . . . . . . . . . . . . . . . . . . . . . . .  58
##### 5.2.2 Intégration de modules interactifs . . . . . . . . . . . . . . . . . . . . . . . .  60
### 6 Participation au travail de recherche . . . . . . . . . . . . . . . . . . . . . . . . . . 63
#### 6.1 Décloisonnement des corpus spécialisés . . . . . . . . . . . . . . . . . . . . . . . . 64
##### 6.1.1 Enrichir les données par l’interconnexion . . . . . . . . . . . . . . . . . . . . . 64
##### 6.1.2 Constitution d’une interface spécialisée : le cas des éditions de tables . . . . .  66
#### 6.2 Analyse par la visualisation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 68
##### 6.2.1 Des manuscrits composites : montrer l’agencement d’un source primaire . . . . . . . 68
##### 6.2.2 Représenter un milieu intellectuel : le cas de la carte historique . . 70
### 7 Assurer la réutilisation du corpus numérique 75
#### 7.1 Accessibilité des données brutes . . . . . . . . . . . . . . . . . . . . . . . . 75
##### 7.1.1 Modalités d’accès à la donnée . . . . . . . . . . . . . . . . . . . . . 75
##### 7.1.2 Fonctionnalités implémentées dans l’interface publique . . . . . . . 78
#### 7.2 Exposer les méthodes : documentation et maintien de code . . . . . . . . . 78
##### 7.2.1 Lisibilité et documentation . . . . . . . . . . . . . . . . . . . . . . 79
##### 7.2.2 Gestion de bugs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 80
## III Traitement technique de la donnée et management des interactions 83
### 8 Gestion de projet 85
#### 8.1 Dialogue entre recherche et ingénierie . . . . . . . . . . . . . . . . . . . . . 85
##### 8.1.1 Coopération dans le domaine des humanités numériques . . . . . . 85
##### 8.1.2 Processus de conception des interfaces . . . . . . . . . . . . . . . . 87
#### 8.2 Organisation du travail intra-équipe . . . . . . . . . . . . . . . . . . . . . . 89
##### 8.2.1 Instruments de gestion du travail . . . . . . . . . . . . . . . . . . . 89
##### 8.2.2 Méthodes de développement . . . . . . . . . . . . . . . . . . . . . . 91
### 9 Environnement technique 93
#### 9.1 Architecture de l’application Web . . . . . . . . . . . . . . . . . . . . . . . 93
##### 9.1.1 Modèle-Vue-Contrôleur . . . . . . . . . . . . . . . . . . . . . . . . . 93
##### 9.1.2 Le paradigme client/serveur . . . . . . . . . . . . . . . . . . . . . . 96
#### 9.2 Implémentation d’ElasticSearch . . . . . . . . . . . . . . . . . . . . . . . . 98
##### 9.2.1 Présentation d’ElasticSearch . . . . . . . . . . . . . . . . . . . . . . 98
##### 9.2.2 Utilisation dans le front office . . . . . . . . . . . . . . . . . . . . . 99
### 10 De la conception à l’implémentation 103
#### 10.1 Technologies de visualisation de données . . . . . . . . . . . . . . . . . . . 103
##### 10.1.1 Choix du moyen de réalisation . . . . . . . . . . . . . . . . . . . . . 103
##### 10.1.2 Choix d’une bibliothèque JavaScript . . . . . . . . . . . . . . . . . 105
#### 10.2 Constitution d’une visualisation . . . . . . . . . . . . . . . . . . . . . . . . 107
##### 10.2.1 Dialogue entre conception et réalisation . . . . . . . . . . . . . . . 107
##### 10.2.2 Anticiper les obstacles à la visualisation . . . . . . . . . . . . . . . 108
##### 10.2.3 Limites de la visualisation . . . . . . . . . . . . . . . . . . . . . . . 111
### Conclusionn . . . . . . . . . . . . . . . . . . . . . . . 115
