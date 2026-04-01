
## Étude
### Références
"Cloud technologies, firm growth and industry concentration" 

arXiv ID : 2409.17035

LEM Working Paper : 2024/25

Auteurs : Caldarola, Bernardo & Fontanelli, Luca



### Sources
[pdf](https://arxiv.org/pdf/2409.17035.pdf)

[html](https://arxiv.org/html/2409.17035v3)


## Méthodologie

### Récupération données
Base	Contenu	Période
[Enquêtes ICT](/définitions/enquête_ICT.md)	Adoption cloud + autres technologies numériques	2015-2019
Données de bilan	CA, résultat, actifs (pour calculer croissance)	2005-2022
Employeur-salarié	Emploi, productivité par salarié	2005-2022
Registre des entreprises	Création/fermeture, secteur, localisation	2005-2022

Échantillon final : ~25 000 entreprises observées sur 3 vagues (2015, 2017, 2019).


### traitement des données
ce sont les "Enquêtes ICT entreprises France" menées par l'INSEE pour Eurostat sur 2015, 2017, 2019.

Enquête ICT (2015-19) → "Qui utilise le cloud ?" \
       ↓ Croisement SIRENE \
Données bilan (2005-22) → "Quelle croissance avant/après ?"

pour chaque SIREN qui dit "Oui cloud en 2017", on mesure sa croissance sur log(CA) [-2 ans, +2 ans] autour de 2017.



### mode de calcul
Croissance_it = α + β Cloud_it + γ Size_it + δ (Cloud_it × Size_it) + Controls + ε_it
- i = entreprise, t = année
- β = effet direct du cloud sur la croissance
- δ = hétérogénéité (effet différent selon la taille)

### Tableaux 3 et 4

Tableau 3/4 = régression linéaire multiple

Modèle : Croissance = a + b×Cloud + c×Taille + d×(Cloud×Taille) + contrôles

- Cloud = 1 si l'entreprise utilise le cloud, 0 sinon
- Taille = souvent log(CA) ou nb employés
- Cloud×Taille = variable d'interaction clé pour ton benchmark

**Interprétation pas à pas**
Colonne 1 : "Cloud" seul
- β Cloud = effet du cloud pour une petite entreprise de référence (taille=0)
- Si β Cloud = +0.05 et p<0.05 → les petites entreprises grandissent 5% plus vite avec le cloud

Colonne 2 ou interaction : "Cloud × Size"
- β Interaction = comment l'effet du cloud change avec la taille
- Si β Cloud×Size = -0.02 et significatif → pour chaque unité de taille en plus, l'effet du cloud diminue de 2%

### Définition unité de taille

`Size = log(CA en milliers d'euros)`

**exemples :**
- CA = 1 000 € → Size = log(1) = 0
- CA = 10 000 € → Size = log(10) = 2,3
- CA = 100 000 € → Size = log(100) = 4,6
- CA = 1 million € → Size = log(1 000) = 6,9
- Petite entreprise (log(CA)=5) → Effet Cloud = +0.05  
- Grande entreprise (log(CA)=8) → Effet Cloud = +0.05 - 0.02×3 = +0.01


### Cas étudiés
#### Petite entreprise
Le stéréotype habituel, c’est une structure plus fragile, avec moins de ressources IT, moins d’économies d’échelle, et donc plus de difficulté à digitaliser le SI.
L’étude conclut justement que les petites entreprises sont celles qui profitent le plus du cloud, parce qu’il réduit les barrières à la digitalisation et libère un potentiel de croissance jusque-là bloqué.

#### Grande entreprise
Le stéréotype de la grosse boîte, c’est qu’elle a déjà les moyens d’industrialiser son SI, d’automatiser et de capter des gains d’échelle.
L’étude trouve bien un effet positif du cloud pour ces entreprises, mais plus faible que pour les petites, ce qui suggère que leur SI est déjà plus mature et que le cloud apporte un gain marginal moindre

## Données

Adoption croissante avec la taille : +50% des firmes du quintile supérieur utilisent le cloud *(Tableau A3 )*

### Effet du cloud sur la croissance (Caldarola & Fontanelli, 2024)

- Petites entreprises (CA < 100k€)  → +5% croissance
- Grandes entreprises (CA > 1M€)   → +1% croissance seulement


## Analyse
L’intérêt du papier, c’est qu’il casse l’idée simpliste selon laquelle “plus l’entreprise est grande, plus le cloud est rentable”.
Au contraire, il montre que le cloud peut être un outil de rattrapage pour les petites structures, car il réduit les frictions de digitalisation et améliore leur capacité de croissance.

L’article indique que l’adoption du cloud a un effet positif sur la croissance de long terme, et que cet effet diminue pour les entreprises les plus grandes. Il précise aussi que cette relation reste robuste à plusieurs vérifications économétriques et que le cloud est lié à une hausse de l’intensité numérique sur le long terme, relation plus forte pour les petites firmes.

Le papier indique que l’usage du cloud a un effet positif sur la croissance des firmes, avec un bénéfice plus fort pour les petites entreprises que pour les grandes. Il donne aussi des statistiques de diffusion du cloud dans l’échantillon français, par exemple une hausse de 25,64% à 32,54% à 40,00% sur les trois millésimes observés.

**Pour la petite entreprise**

Le chiffre le plus directement exploitable est que la diffusion du cloud a augmenté la part d’entreprises l’utilisant de 27,3% entre 2015 et 2017, puis de 55,8% entre 2015 et 2019 dans l’échantillon de l’étude. L’article conclut que l’effet sur la croissance est plus marqué chez les petites firmes, ce qui suggère que le cloud leur apporte un gain réel de scalabilité et de digitalisation.

**Pour la grande entreprise**

L’étude ne donne pas, dans l’extrait accessible ici, un chiffre du type “+x % de croissance pour les grandes entreprises”. En revanche, elle dit explicitement que l’effet du cloud “diminishes for larger firms”, donc que les grandes entreprises bénéficient aussi du cloud, mais moins fortement que les petites.