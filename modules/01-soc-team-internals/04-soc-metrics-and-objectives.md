# SOC Metrics and Objectives

## Synthèse rapide

- **Sujet principal** : découvrir les métriques clés d'un SOC et comment les améliorer.
- **Objectif de la room** : connaître les métriques et indicateurs et leur importance dans un SOC, les comprendre et gagner en efficacité.
- **Compétences travaillées** : compréhension des métriques SOC, analyse d’indicateurs, identification des causes de mauvais résultats et proposition d’améliorations opérationnelles.
- **Lien métier** : cette room montre comment un analyste SOC L1 peut comprendre l’impact de son travail sur la performance globale du SOC : réduction du bruit, triage plus rapide, escalade pertinente et meilleure réactivité face aux menaces.

## 1. Contexte de la room

Cette room permet de prendre connaissance des différentes métriques et indicateurs qui existent dans un SOC, afin de pouvoir évaluer la performance d'un analyste, d'une équipe.
Le but est de développer des leviers d'amélioration pour ces métriques et indicateurs dans le but de gagner en efficacité.

## 2. Objectifs d'apprentissage

- Connaître les métriques existantes.
- Savoir lire les indicateurs de performance.

## 3. Notions clés

- **MTTD (Mean Time to Detect)** : temps moyen entre le début d’une activité malveillante et sa détection par les outils ou l’équipe SOC.

- **MTTA (Mean Time to Acknowledge)** : temps que met un analyste à prendre en charge une alerte.

- **MTTR (Mean Time to Respond)** : temps moyen nécessaire pour répondre à une menace après sa détection, par exemple en isolant une machine, en sécurisant un compte compromis ou en lançant les actions de remédiation.

## 4. Méthodologie / raisonnement

Les métriques permettent d’évaluer différents aspects du fonctionnement d’un SOC : volume d’alertes, niveau de bruit, qualité du triage, rapidité de détection, prise en charge et réponse aux menaces.
Les indicateurs quant à eux, permettent d'évaluer le pourcentage de faux positifs et de vrais positifs traités, et ainsi, selon les résultats, permettre d'affiner les règles de détection d'outils comme un SIEM par exemple.

### 1. Les métriques principales

- **Le nombre d'alertes**, qui représente le nombre total d'alertes reçues.
- **Le taux de faux positifs**, qui se calcule par rapport aux faux positifs sur le nombre total d'alertes, ça représente le bruit dans les alertes.
- **Le taux d'alertes escaladées**, qui se calcule par rapport au nombre d'alertes escaladées sur le nombre total d'alertes, qui représente principalement la qualité du triage fait par le L1. Un taux trop élevé peut indiquer que les L1 escaladent trop d’alertes et surchargent le L2. À l’inverse, un taux trop bas peut être positif si les L1 traitent correctement les alertes, mais il peut aussi être préoccupant si des vrais positifs sont mal classifiés ou non escaladés.
- **Le taux de menaces détectées** : il se calcule par rapport au nombre de menaces détectées sur le nombre total de menaces réelles. En théorie, ce taux devrait tendre vers 100 %, car chaque menace manquée peut avoir de lourdes conséquences.
- **Dwell time** : durée pendant laquelle un attaquant reste présent dans un environnement compromis avant d’être détecté ou expulsé. Plus ce temps est long, plus l’attaquant a d’opportunités pour faire de la reconnaissance, se déplacer latéralement, voler des données ou préparer une attaque plus impactante.

### 2. Les métriques de triage

Ce sont les métriques évoquées dans les notions clés précédemment :
- MTTD, qui est la moyenne de temps entre une attaque et sa détection par des outils de SOC.
- MTTA, qui est la moyenne de temps d'un analyste L1 pour commencer à trier une nouvelle alerte.
- MTTR, qui est la moyenne de temps pris par le SOC pour stopper une menace.
et également la disponibilité des équipes d'un SOC. par exemple, 24/7 ou 8/5.
Dans ce dernier cas, si une menace est détectée le samedi, elle ne serait pas traitée avant le lundi, ce qui pourrait avoir un impact plus ou moins important selon le type d'alerte.

### 3. Améliorer les métriques

Les métriques sont un moyen d'évaluer la performance d'un SOC ou d'un analyste, et améliorer ces métriques est un levier pour gagner en efficacité et en précision.

Voici des exemples en restant dans la théorie et la méthodologie :
- **Taux de faux positifs** > 80% : cela indiquerait qu'il y a trop de bruit;
    → L'utilisation d'un SOAR ou de scripts d'automatisation pourrait réduire ce bruit.
- **MTTD > 30 min** : le délai de détection est élevé;
    → Ajuster les règles de détection avec le SOC engineer ou vérifier si les logs sont collectés en temps réel pourrait réduire ce délai.
- **MTTA > 30 min** : le délai de prise en charge est élevé.  
    → Des notifications en temps réel et une meilleure répartition des alertes entre les analystes peuvent réduire ce délai.
- **MTTR > 4 heures** : selon le type de menace, elle peut ne pas être contenue à temps.  
    → Le L1 doit escalader rapidement vers le L2 lorsque c’est nécessaire et s’appuyer sur des workflows documentés selon le type d’attaque.

Ce sont des mesures théoriques, le but étant de comprendre qu'il faut avoir un bon équilibre au niveau des règles de détection, des procédures à suivre, afin de garantir le maintien de la triade CIA au sein d'une entreprise.

## 5. Ce que j'ai appris

Cette room m’a permis de comprendre que les métriques permettent de donner une vision globale de l’efficacité du SOC et du traitement des alertes.
Cela peut être également un levier pour améliorer la réactivité et la fiabilité du triage, mais cela requiert de garder un équilibre au niveau des règles de détection ou au niveau des procédures de triage afin de garantir une gestion efficace des alertes et des menaces.

## 6. Difficultés rencontrées

- Trouver un équilibre pour les règles de triage et le tuning des outils.
- Ne pas interpréter les métriques seules comme une vérité absolue, mais les analyser avec le contexte : volume d’alertes, criticité, maturité du SOC, horaires de couverture et qualité des règles de détection.

## 7. Déclics / points importants

Le principal déclic de cette room est que les métriques ne servent pas uniquement au management. Elles permettent aussi aux analystes SOC L1 de comprendre l’impact de leur travail sur l’efficacité globale du SOC.

Un taux élevé de faux positifs peut ralentir le triage et créer de la fatigue d’alertes. Un MTTA élevé peut indiquer que les alertes restent trop longtemps sans prise en charge. Un MTTR élevé peut montrer que la réponse aux menaces n’est pas assez rapide ou que les procédures ne sont pas suffisamment claires.

J’ai aussi retenu qu’une métrique doit toujours être interprétée avec son contexte. Une valeur seule ne suffit pas à juger correctement la performance d’un SOC.

## 8. Compétences travaillées

- Compréhension des métriques SOC principales.
- Lecture d’indicateurs de performance.
- Analyse du taux de faux positifs.
- Compréhension du MTTD, MTTA et MTTR.
- Identification de problèmes opérationnels dans un SOC.
- Proposition d’améliorations : tuning des règles, meilleure priorisation, automatisation, workflows documentés.
- Compréhension du lien entre performance SOC, qualité du triage et réduction du risque.

## 9. À approfondir

- Mieux comprendre comment les SLA sont définis dans un SOC réel.
- Approfondir la différence entre MTTD, MTTA, MTTR et dwell time.
- Étudier comment le tuning des règles SIEM permet de réduire le taux de faux positifs.
- Comprendre comment un SOAR peut aider à automatiser certaines actions de triage.
- Voir comment les métriques varient selon la criticité des alertes et le niveau de maturité du SOC.