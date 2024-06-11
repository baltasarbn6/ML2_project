Prédiction du Taux de Clics
Introduction
Ce projet répond à une compétition Kaggle visant à prédire si une publicité mobile sera cliquée ou non. Le taux de clics (Click-Through Rate, CTR) est une mesure essentielle pour évaluer la performance des publicités en ligne. L'objectif est de construire un modèle qui prédit la probabilité de clic sur une publicité en utilisant des données historiques fournies par Avazu.

Objectif
L'objectif principal est de développer un modèle de machine learning pour prédire la probabilité de clic sur une publicité mobile. Les prédictions sont évaluées à l'aide de la Logarithmic Loss, où des valeurs plus faibles indiquent de meilleures performances.

Méthodologie
Le projet suit les étapes suivantes :

Chargement et Échantillonnage des Données : En raison de la grande taille du jeu de données, les données sont chargées par morceaux et échantillonnées pour l'entraînement.
Nettoyage des Données : Les entrées invalides dans la colonne hour sont supprimées pour garantir une conversion correcte en datetime.
Ingénierie des Caractéristiques : Les caractéristiques temporelles (jour, heure, jour de la semaine) sont extraites de la colonne hour. Les variables catégorielles sont transformées à l'aide du hachage.
Analyse Exploratoire des Données (EDA) : Visualisations pour comprendre la distribution des données et l'importance des caractéristiques.
Entraînement du Modèle : Le CatBoostClassifier est utilisé pour son efficacité avec les données catégorielles. Le modèle est entraîné en utilisant le GPU pour un traitement plus rapide.
Évaluation : Les performances du modèle sont évaluées à l'aide de la Logarithmic Loss et l'importance des caractéristiques est analysée.
Choix du Modèle
Initialement, des modèles classiques tels que la Régression Logistique, les Forêts Aléatoires et les Gradient Boosting Machines ont été envisagés. CatBoost a été choisi pour sa gestion supérieure des caractéristiques catégorielles et ses performances globales.

Résultats
Le modèle a été entraîné et évalué, atteignant ses meilleures performances à l'itération 245. Les caractéristiques les plus importantes identifiées incluent site_id, site_domain et device_model.

Conclusion
Le projet a réussi à développer un modèle pour prédire la probabilité de clics sur les publicités, en utilisant CatBoost pour son efficacité avec les données catégorielles. Les prédictions peuvent aider les annonceurs à optimiser leurs campagnes et à améliorer l'engagement des utilisateurs.
