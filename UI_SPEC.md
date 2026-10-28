# Spécification interface — Visualisation de l'analyse immobilière

## Vue carte (localisation)

- Carte interactive centrée sur la zone d'étude (villes cibles de l'orchestrateur)
- Un marqueur par annonce analysée, positionné à l'adresse exacte
- Couleur du marqueur = note finale (vert = 8-10, orange = 5-7, rouge = 1-4)
- Taille du marqueur = écart entre note et médiane du marché local (plus l'écart est fort, plus le marqueur est gros)
- Au clic sur un marqueur : panneau latéral avec la fiche du bien, le rapport de l'agent, et le lien vers le rapport détaillé
- Filtres superposables : par note, par quartier, par typologie, par tendance de prix (hausse / stable / baisse sur 5 ans)
- Couche optionnelle : zones scolaires (polygones colorés par niveau), temps de trajet isochrones (voiture, TC, vélo) autour de chaque bien

## Vue graphiques

- **Évolution des prix** : courbe sur 5 ans par quartier, avec projection à 1 an (ligne pointillée)
- **Évolution des loyers** : même format, pour évaluer la rentabilité future
- **Rendement brut/net** : histogramme par annonce, trié
- **Distribution des notes** : histogramme des 1000 notes finales
- **Tendances par paramètre** : petits multiples (small multiples) — un mini-graphique par paramètre du harness (DPE, charges, écoles, trajets...) montrant l'évolution 5 ans
- **Matrice de corrélation** : note finale vs chaque paramètre, pour identifier ce qui pèse le plus dans le score
- **Graphe de synthèse** : réseau de relations entre quartiers, typologies et signaux récurrents (inspiré du reasoning atlas du preprint Sun et al.)

## Contraintes techniques

- La carte et les graphiques se mettent à jour en temps réel au fur et à mesure que les agents terminent leurs rapports
- Chaque graphique doit être exportable en PNG ou SVG
- Mode sombre et mode clair
- Responsive : utilisable sur desktop et tablette

## Lien avec le preprint

Le graphe de synthèse reprend l'idée du **reasoning atlas** de Sun et al. : un graphe reliant entités (ici quartiers, typologies, paramètres) et preuves (rapports d'agents), au lieu d'une simple liste.
