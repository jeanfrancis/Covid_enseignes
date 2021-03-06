# Covid Enseignes

Quelles sont les enseignes de magasins ouverts ou fermés durant le confinement ? [La réponse est ici !](regles.csv)

L'objectif de ce dépôt est de renseigner les règles applicables aux enseignes en France concernant leur ouverture durant la période de confinement suite à l'épidément COVID-19. Ceci permettra la réalisation de cartes sur les commerces accessibles pendant le confinement.

Exemples :

* les boulangeries "Le Bon Pain" sont ouvertes de 9h à 18h30 dans toute la France
* les magasins de bricolage "L'outil pro" sont fermés partout en France


## Comment participer ?

### Signaler une information

Pour signaler une information concernant une chaîne de magasins, vous pouvez [créer un ticket](https://github.com/PanierAvide/Covid_enseignes/issues) sur ce dépot.

Le ticket devra avoir la forme suivante :

```

* __Magasins concernés__ : nom de l'enseigne
* __Règle d'ouverture__ : magasins fermés / magasins ouverts aux horaires habituels / magasins ouverts à des horaires spéciales (précisez : sur RDV, horaires d'ouvertures...)
* __Wikipédia/Wikidata__ : (optionel) lien URL vers l'enseigne sur Wikipédia (ou idéalement [Wikidata](https://www.wikidata.org/))
* __Horaires__ : (optionel) lien URL vers la page recensant les horaires actualisés
* __Source__ : l'adresse où vous avez constaté l'info
```

__Avant de créer un ticket__, vérifiez que les informations n'ont pas déjà été répertoriées dans [la liste](regles.csv) ou [dans les tickets ouverts](https://github.com/PanierAvide/Covid_enseignes/issues?q=is%3Aissue).

Les catégories de magasins/services concernés sont les suivantes :

* Pharmacies
* Supermarché
* Supérette
* Vente de surgelés
* Marché
* Vente de fruits et légumes
* Boucher
* Charcutier
* Vente de fruits de mer
* Fromager
* Boulangeries
* Magasin de vente et de réparation de vélos
* Magasin de téléphonie
* Magasin de bricolage
* Papeterie
* Opticien
* Location de voiture
* Banque
* Assureur
* Agence de travail temporaire
* Caviste
* Laverie
* Vente de tabac
* Vente de cigarettes électroniques
* Stations essence
* Services funéraires

### Intégrer les informations

Sur la base des tickets ouverts, et si vous êtes à l'aise avec GitHub et l'outil informatique, intégrez les informations reçues dans le fichier CSV `regles.csv`, sur la base du format décrit ci-dessous. Proposez une pull request vers la branche master, et pensez à lier au ticket correspondant.


## Le résultat

L'objectif est de produire sur l'ensemble du territoire national une carte présentant les commerces ouverts, ainsi que les horaires associées. Plusieurs raisons à cela :
* Limiter au strict nécessaire les déplacements et donc éviter des détours vers des commerces fermés
* Répartir la charge sur plusieurs commerces au lieu d'un seul dans une zone et éviter les cohues/bousculades/pénuries
* Réaliser un suivi régulier de l'évolution de la situation pendant le confinement

L'ensemble des informations compilées sont [réunies dans un fichier tableur](regles.csv) `regles.csv`, définissant les règles reçues pour être exploitées en lien avec OpenStreetMap et Wikidata. Son format est le suivant (encodage UTF-8, séparateur `,`) :

* `nom_enseigne` : nom de l'enseigne
* `categorie` : type de commerce (en Anglais, selon la description OpenStreetMap : `supermarket`, `bakery`...)
* `id_wikidata` : identifiant Wikidata de cette enseigne
* `url_source` : lien URL où les infos d'ouveture/fermeture sont renseignées
* `url_horaires` : en cas d'horaires adaptées, lien URL recensant les horaires
* `regle_ouverture` : statut d'ouverture des magasins (valeurs possibles : `ouvert` = pas de changement, `ouvert_adapté` = ouvert avec horaires adaptés, `partiel` = certains magasins fermés, `fermé` = tous les magasins fermés)
* `horaires` : horaires au format `opening_hours` OpenStreetMap __si valables pour tous les commerces__ de l'enseigne
* `infos` : champ texte libre d'informations supplémentaires
