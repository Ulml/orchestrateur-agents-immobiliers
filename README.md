# Orchestrateur d'agents distribués — Immobilier

Prompt d'orchestrateur pour un système multi-agents d'analyse immobilière, inspiré de l'architecture *distributed biological reasoning* (Sun et al., 2026).

## Principe

- **Un agent par annonce** : chaque sous-agent reçoit un harness standard (fiche du bien, contexte, outils, données contextuelles, format de sortie)
- **Auto-réparation** : si un élément du harness manque, un agent dédié le génère selon le SOTA
- **Synthèse transversale** : l'orchestrateur fusionne les rapports et ne remonte que les patterns (quartiers surévalués, typologies sous-cotées, signaux récurrents)

## Fichiers

- `PROMPT_ORCHESTRATEUR.md` : le prompt complet, prêt à coller dans un agent

## Inspiration

Basé sur le preprint *Distributed AI agents enable comprehensive discovery of biological insights at scale* (Sun, Park, DeTomaso et al., Scripps Research / OpenAI / PerturbAI, bioRxiv, octobre 2026) : https://doi.org/10.64898/2026.10.15.759436

L'idée clé : découper l'interprétation selon la structure même du problème — beaucoup de petites unités indépendantes qu'il faut relier — au lieu de charger un agent unique d'un corpus massif.
