Les 4 modalités principales (2026)
Modèle	Principe	Répartition	Exemple usage
Pay-as-you-go	Facturé à la seconde/heure sur CPU/RAM/stockage/transfert	85-90% des déploiements	Dev/test, workloads variables
Réservations	Engagement 1-3 ans → -40 à 70%	25% des prod critiques	Bases de données, IA lourde
Spot/Preemptible	Ressources "interrompibles" → -80 à 90%	10-15% batch jobs	Big Data, rendering
Savings Plans	Engagement capacité flexible → -30 à 50%	20% entreprises matures	Multi-régions, hybride AWS/Azure

Évolution majeure 2025-2026

FinOps Certified pousse l'adoption des Savings Plans (+35% vs 2024) car plus flexible que les Reserved Instances. Spot explose avec l'IA (+200% adoption).

1. Pay-as-you-go (85-90% des cas)
Principe : Tu payes à la seconde exactement ce que tu consommes.
1 vCPU-heure = 0,02€ | 1 Go RAM-heure = 0,003€ | 1 Go stockage/mois = 0,03€
Risque : gaspillage massif si pas surveillé (VM oubliées = 30% des coûts).

2. Réservations (25% prod critiques)
Principe : Tu t'engages 1-3 ans sur X ressources → -40 à 70%.
Exemple : 10 EC2 m5.large pendant 3 ans → tu payes 60% moins cher
Comme : acheter un forfait téléphone bloqué 24 mois.
Parfait pour : Bases de données stables, ERP critiques, IA lourde.
Risque : surcapacité inutilisée → tu payes quand même.

3. Spot/Preemptible (10-15% batch)
Principe : Tu achètes les ressources "interrompibles" → -80 à 90%.
Le provider peut couper ta VM si urgence → prix divisé par 5-10
Comme : covoiturage → très pas cher, mais ils peuvent changer d'avis.
Comme si : tu achètes une voiture d'occasion sur Leboncoin à -90%. Super deal, mais le proprio peut changer d'avis et te la reprendre si quelqu'un propose plus.
Parfait pour : Big Data, rendering, ML training, backup.
Risque : interruption brutale → nécessite code résilient.
Prix Spot = Prix On-Demand ÷ 5 → 10 (fluctue toutes les 5min)
Si quelqu'un propose >10€ → BOOM, ta VM s'arrête en 2min
Résumé : Ultra pas cher mais ultra risqué. Parfait pour les tâches "restartables".

4. Savings Plans (20% entreprises matures)
Principe : Engagement $ par heure sur 1-3 ans → -30 à 50%, flexible.
Tu dis "je dépense 10$/h sur EC2/Lambda/RDS" → auto-appliqué où tu veux
Comme : un budget global flexible (pas lié à 1 type de VM).
Comme si : au lieu d'acheter exactement 3 paires de Nike, tu dis "je dépense 300€ en baskets sur 1 an, donnez-moi -40% sur tout ce que j'achèterai".
Tu engages "10$/heure pendant 1 an" (soit 87k$)
Peu importe si c'est EC2 Paris, Lambda Tokyo ou RDS Dublin → remise auto-appliquée
Parfait pour : Multi-régions, multi-cloud, équipes FinOps avancées.
Risque : moins d'économies que Reserved (-40% vs -72%).
Reserved = "10 EC2 m5.large Paris x 1 an"
Savings = "$10/h n'importe où, n'importe quoi" (sauf stockage)

SaaS : Abonnements + paliers utilisateurs
Variantes (85% du SaaS) :
- Par utilisateur : Slack = 8€/utilisateur/mois
- Freemium : Notion gratuit < 10 docs, puis 10€/utilisateur
- Usage : Twilio = 0,01€/SMS envoyé
- Stockage : Dropbox = 10€/mois + 0,02€/Go supplémentaire

PaaS : Mix IaaS + SaaS

IaaS → FinOps = optimiser 1000 lignes de facture détaillée
PaaS → FinOps = équilibrer abo fixe vs pics usage  
SaaS → FinOps = négocier contrats + usage par service