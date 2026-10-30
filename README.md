# Guide d'accueil et circuits de visite a Lyon

Application web legere et bilingue concue pour les voyageurs accueillis au 141 avenue Marechal de Saxe (Lyon 3e), particulierement lors de la fete des Lumieres et des sejours d'hiver. Le projet propose une alternative aux brochures touristiques standardisees en partageant les itineraires reels et les adresses locales testees par les hotes.

## Demarche et vision du projet

L'objectif principal est d'offrir aux invites une autonomie complete des leur arrivee, avec un acces immediat aux reperes essentiels du quartier et a quatre journees de decouverte optimisees a pied et en transports.

### Conception centree sur le voyageur

Plutot qu'un long document textuel difficile a consulter en deplacement, le guide adopte le format d'une application web responsive accessible sur smartphone et ordinateur. L'interface bascule instantanement entre francais et anglais pour servir aussi bien les visiteurs francophones qu'internationaux.

Le point d'ancrage fixe reste en permanence l'appartement (Saxe-Gambetta), permettant a chaque voyageur de mesurer les temps de marche reels et de localiser les stations de metro ou tramway utiles (lignes B et D a 3 minutes).

### Selection rigoureuse des adresses

Le referentiel cartographie 26 points d'interet selectionnes sans complaisance commerciale :

- 11 etapes culturelles et patrimoniales comprenant les traboules de la Renaissance, les points de vue sur la ville, les cloitres de l'Hotel-Dieu et les berges fluviales.
- 15 tables lyonnaises verifiees, du bouchon patrimonial aux bistrots marins de la Guillotiere, en passant par les institutions des Halles Paul Bocuse.

Chaque fiche associe une photographie reelle, une synthese pratique, un bouton d'itineraire Google Maps direct et des liens vers les sites officiels ou profils Instagram des etablissements.

## Architecture des quatre circuits

Les quatre parcours ont ete traces pour eviter les allers-retours inutiles et tirer parti de la topographie lyonnaise.

### Circuit 1 : Fourviere et descente vers le Vieux Lyon

Montee directe en metro D et funiculaire vers l'esplanade de Fourviere pour embrasser la vue panoramique a 360 degres, puis descente pedestre a travers les jardins du Rosaire et traversee des traboules medievales et Renaissance de la rue Saint-Jean.

### Circuit 2 : Presqu'ile Nord et Croix-Rousse

Traversee du pont de la Guillotiere vers le grand dome du Grand Hotel-Dieu, passage par la place des Jacobins et la place des Terreaux, puis ascension des pentes historiques des canuts jusqu'au plateau de la Croix-Rousse par la montee de la Grande Cote.

### Circuit 3 : Presqu'ile Sud, antiquaires et patrimoine

Parcours artistique au sud de Bellecour le long des galeries de la rue Auguste Comte, traversee du quartier d'Ainay et visite des expositions gratuites aux Archives de Lyon (1 place des Archives, Lyon 2e), avant une etape gourmande dans les bouchons historiques.

### Circuit 4 : Tete d'Or et Confluences

Itineraire reliant les deux grands poumons fluviaux et contemporains de la metropole : le parc de la Tete d'Or au nord avec ses serres tropicales et le MAC Lyon, puis descente en tramway T1 vers la pointe sud et l'architecture moderne du musee des Confluences.

## Choix techniques

L'application repose sur une philosophie minimaliste zero dependance lourde :

- Fichier unique HTML5 / CSS3 / JavaScript natif pour simplifier le deploiement et garantir une compatibilite totale sans compilation.
- Moteur cartographique Leaflet integre en local (`leaflet.js` et `leaflet.css`) pour resister aux problemes de reseau.
- Tuiles OpenStreetMap France (`tile.openstreetmap.fr`) fournissant un rendu precis du tissu urbain lyonnais (noms des rues, icones de metro, fleuves) sans cle d'API payante ni blocage de referer. Un mecanisme de secours dynamique bascule automatiquement vers Esri World Street Map ou CartoDB en cas d'indisponibilite reseau.
- Schemas SVG vectoriels integres pour resumer chaque circuit sous forme de frise d'etapes claire et lisible sur petit ecran.
- Traces vectoriels des circuits activables a la demande pour visualiser le trajet global et ajuster la carte sur la zone parcourue.

## Consultation et hebergement

Le site peut etre consulte directement en local en ouvrant `index.html` dans n'importe quel navigateur, ou heberge publiquement via GitHub Pages en branchant la branche `main` dans les parametres du depot.
