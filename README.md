# Guide d'accueil et circuits de visite à Lyon

Application web légère et bilingue conçue pour les voyageurs accueillis au 141 avenue Maréchal de Saxe (Lyon 3e), particulièrement lors de la fête des Lumières et des séjours d'hiver. Le projet propose une alternative aux brochures touristiques standardisées en partageant les itinéraires réels et les adresses locales testées par les hôtes.

https://caroheymes.github.io/welcome-at-home/

## Démarche et vision du projet

L'objectif principal est d'offrir aux invités une autonomie complète dès leur arrivée, avec un accès immédiat aux repères essentiels du quartier et à quatre journées de découverte optimisées à pied et en transports.

### Conception centrée sur le voyageur

Plutôt qu'un long document textuel difficile à consulter en déplacement, le guide adopte le format d'une application web responsive accessible sur smartphone et ordinateur. L'interface bascule instantanément entre français et anglais pour servir aussi bien les visiteurs francophones qu'internationaux.

Le point d'ancrage fixe reste en permanence l'appartement (Saxe-Gambetta), permettant à chaque voyageur de mesurer les temps de marche réels et de localiser les stations de métro ou tramway utiles (lignes B et D à 3 minutes à pied).

### Sélection rigoureuse des adresses

Le référentiel cartographie 26 points d'intérêt sélectionnés sans complaisance commerciale :

- 11 étapes culturelles et patrimoniales comprenant les traboules de la Renaissance, les panoramas sur la ville, les cloîtres du Grand Hôtel-Dieu et les berges fluviales.
- 15 tables lyonnaises vérifiées, du bouchon patrimonial aux bistrots marins de la Guillotière, en passant par les institutions des Halles Paul Bocuse.

Chaque fiche associe une photographie réelle, une synthèse pratique, un bouton d'itinéraire Google Maps direct et des liens vers les sites officiels ou profils Instagram des établissements.

## Architecture des quatre circuits

Les quatre parcours ont été tracés pour éviter les allers-retours inutiles et tirer parti de la topographie lyonnaise.

### Circuit 1 : Fourvière et descente vers le Vieux Lyon

Montée directe en métro D et funiculaire vers l'esplanade de Fourvière pour embrasser la vue panoramique à 360 degrés, puis descente pédestre à travers les jardins du Rosaire et traversée des traboules médiévales et Renaissance de la rue Saint-Jean et de la rue du Bœuf.

### Circuit 2 : Presqu'île Nord et Croix-Rousse

Traversée du pont de la Guillotière vers le grand dôme du Grand Hôtel-Dieu, passage par la place des Jacobins et la place des Terreaux, puis ascension des pentes historiques des canuts jusqu'au plateau de la Croix-Rousse par la montée de la Grande Côte.

### Circuit 3 : Presqu'île Sud, antiquaires et patrimoine

Parcours artistique au sud de Bellecour le long des galeries de la rue Auguste Comte, traversée du quartier d'Ainay et visite des expositions gratuites aux Archives de Lyon (1 place des Archives, Lyon 2e), avant une étape gourmande dans les bouchons historiques.

### Circuit 4 : Tête d'Or et Confluences

Itinéraire reliant les deux grands poumons fluviaux et contemporains de la métropole : le parc de la Tête d'Or au nord avec ses serres tropicales et le MAC Lyon, puis descente en tramway T1 vers la pointe sud et l'architecture moderne du musée des Confluences.

## Choix techniques

L'application repose sur une philosophie minimaliste zéro dépendance lourde :

- Fichier unique HTML5 / CSS3 / JavaScript natif pour simplifier le déploiement et garantir une compatibilité totale sans compilation.
- Moteur cartographique Leaflet intégré en local (`leaflet.js` et `leaflet.css`) pour garantir le fonctionnement même hors connexion.
- Tuiles OpenStreetMap France (`tile.openstreetmap.fr`) fournissant un rendu précis du tissu urbain lyonnais (noms des rues, stations de métro, fleuves) sans clé d'API payante ni blocage de referer. Un mécanisme de secours dynamique bascule automatiquement vers Esri World Street Map ou CartoDB en cas d'indisponibilité réseau.
- Schémas SVG vectoriels intégrés pour résumer chaque circuit sous forme de frise d'étapes claire et lisible sur petit écran.
- Tracés vectoriels des circuits activables à la demande pour visualiser le trajet global et ajuster la carte sur la zone parcourue.

## Consultation et hébergement

Le site peut être consulté directement en local en ouvrant `index.html` dans n'importe quel navigateur, ou hébergé publiquement via GitHub Pages en configurant la branche `main` dans les paramètres du dépôt.
