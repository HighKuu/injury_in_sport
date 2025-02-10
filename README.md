# Mission Data

## 📌 Objectif

L'objectif de cette mission est d'analyser les blessures des athlètes en utilisant des indicateurs clés de performance (KPI) et d'explorer les relations entre les charges d'entraînement, les risques de blessure et la performance.

📄 Lien vers le Notebook : Le collab d’exploration

## 📊 KPI Suivis

Fréquence des blessures par athlète : Nombre total de blessures subies par chaque athlète sur une période donnée.

Taux de blessures par type d’activité : Pourcentage de blessures survenues lors de différentes activités ou sports.

Temps moyen de récupération : Durée moyenne nécessaire à un athlète pour se rétablir complètement après une blessure.

Impact des blessures sur la performance : Comparaison des performances d’un athlète avant et après une blessure.

Taux de récurrence des blessures : Pourcentage de blessures récurrentes chez les athlètes.

### 🗂️ Structure des Données

1. Athlete Information

Athlete_ID : Identifiant unique de l'athlète.

Age : Âge de l'athlète (18–25 ans).

Gender : Sexe de l'athlète (Male/Female).

Height_cm : Taille en centimètres (160–200 cm).

Weight_kg : Poids en kilogrammes (55–100 kg).

Position : Poste dans l'équipe (Guard, Forward, Center).

2. Training Information

Training_Intensity : Intensité moyenne des entraînements (1-10).

Training_Hours_Per_Week : Heures d'entraînement par semaine (5–20 heures).

Recovery_Days_Per_Week : Nombre de jours de récupération par semaine (1–3 jours).

3. Schedule Information

Match_Count_Per_Week : Nombre de matchs par semaine (1–4 matchs).

Rest_Between_Events_Days : Nombre moyen de jours de repos entre les matchs (1–3 jours).

4. Derived Features

Load_Balance_Score : Score (0–100) indiquant l'équilibre entre charge d'entraînement et récupération.

ACL_Risk_Score : Score de risque de blessure des ligaments croisés antérieurs (0–100).

5. Injury Information

Injury_Indicator : Indicateur de blessure (1 = Oui, 0 = Non).

6. Performance Metrics

Fatigue_Score : Niveau de fatigue perçu (1–10).

Performance_Score : Score de performance global (50–100).

Team_Contribution_Score : Score de contribution à l'équipe (50–100).

📈 Analyse des Corrélations

## 🔥 Corrélations fortes (positives)

Load_Balance_Score et Team_Contribution_Score (~0.6) → Un bon équilibre de charge est associé à une meilleure contribution à l'équipe.

ACL_Risk_Score et Team_Contribution_Score (~0.6) → Un risque élevé de blessure pourrait être lié à une forte contribution à l’équipe.

## ❄️ Corrélations modérées (négatives)

Load_Balance_Score et Rest_Between_Events_Days (~-0.5) → Plus de jours de repos entre les événements entraînent un score d'équilibre de charge plus faible.

Load_Balance_Score et Injury_Indicator (~-0.5) → Une meilleure gestion de charge réduit les blessures.

## 📉 Corrélations faibles

La majorité des autres variables présentent des corrélations faibles (~0), suggérant peu de relation entre elles.

## 🔎 Exploitation des Corrélations

L’étude de la relation entre ACL_Risk_Score et Team_Contribution_Score pourrait aider à comprendre l'impact des charges de travail élevées sur le risque de blessure.

Certaines variables faiblement corrélées avec Injury_Indicator pourraient nécessiter une transformation pour améliorer leur pertinence dans un modèle prédictif.

## 📌 Prochaines étapes :

Exploration approfondie des variables influençant le risque de blessure.

Identification des meilleurs indicateurs pour la prévention et la réhabilitation.

Modélisation prédictive pour anticiper les risques de blessure.

