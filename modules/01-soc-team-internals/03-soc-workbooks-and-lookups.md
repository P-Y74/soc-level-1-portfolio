# SOC Workbooks and Lookups

## Synthèse rapide

- **Sujet principal** : Workbooks et lookups et enrichissement du contexte d’alerte.
- **Objectif de la room** : connaître et savoir utiliser les ressources de l'entreprise mises à disposition pour obtenir des informations supplémentaires et du contexte lors de certaines alertes.
- **Compétences travaillées** : enrichissement d’alerte, recherche de contexte, lecture d’inventaires, compréhension de diagrammes réseau et structuration d’un workflow d’investigation.
- **Lien métier** : cette room montre comment un analyste SOC L1 peut enrichir une alerte avec du contexte utilisateur, machine et réseau avant de prendre une décision.

## 1. Contexte de la room

Cette room démontre l'importance de se baser sur des ressources comme les workbooks, l'inventaire des identités et l'inventaire des actifs.

Le but étant de recueillir, si besoin, les informations nécessaires et ainsi fournir le contexte suffisant lors du triage des alertes.

## 2. Objectifs d'apprentissage

- Se familiariser avec les workbooks d'investigation.
- Apprendre où trouver et comment utiliser l'inventaire des actifs.
- Savoir lire un diagramme de réseau.
- Comprendre l'importance des diagrammes de réseau d'une entreprise.
- Comprendre le workflow d'une analyse d'alerte.

## 3. Notions clés

- **Donner du contexte pour l'escalade** : lorsque les informations d'une alerte ne suffisent pas, utiliser les ressources à disposition pour donner un contexte précis lors de l'escalade.

- **Suivre le workflow** : cela permet de faire une analyse structurée et efficace grâce aux workflows existants dans les entreprises.

## 4. Méthodologie / raisonnement

Lors de l’analyse d’une alerte, il est important de s’appuyer sur les inventaires d’identités, les inventaires d’actifs et les diagrammes réseau afin d’ajouter du contexte avant de prendre une décision. Le workbook permet ensuite de suivre un workflow structuré pour éviter les oublis et rendre le triage plus régulier.

### 1. Les actifs et les identités

- Les identités regroupent les comptes utilisateurs, les comptes de service, leurs rôles, leurs contacts et leurs accès autorisés.
- Les actifs regroupent notamment les serveurs et postes de travail, avec des informations comme l’adresse IP, l’OS, le propriétaire, la localisation et le rôle de la machine.

### 2. Les diagrammes de réseau

Dans la continuité de ce que l'on a vu précédemment, le diagramme réseau est utile pour comprendre et retracer le chemin pris par certaines connexions ou reconstituer un chemin d'attaque.

On y retrouve entre autres les informations suivantes :
- Les localisations existantes.
- Les ports exposés.
- Les sous-réseaux et leurs connexions.

### 3. Les workbooks

Grâce aux étapes précédentes, nous pouvons récupérer les informations nécessaires et donc avoir un contexte précis concernant une alerte.

Le workbook est un document structuré qui permet à un analyste L1 de suivre des étapes logiques tout au long de l’investigation, selon le type d’alerte reçue.

Cela peut se faire en 3 étapes :
- **L'étape d'enrichissement** : récupérer des informations supplémentaires, comme l'utilisateur concerné, l'adresse IP...
- **L'étape d'investigation** : analyser les informations collectées et rechercher des actions suspectes ou malveillantes.
- **L'étape d'escalade** : transmettre l'alerte au L2 si les éléments observés le justifient.

### 4. La pratique du workbook

Un exercice du lab consiste ensuite à créer des workflows simples avec les informations à disposition pour différents types d'alertes.

Le but est de comprendre la logique d’implémentation d’un workbook et le rôle de chaque étape dans le triage.

## 5. Ce que j'ai appris

Cette room m’a permis de comprendre que le triage d’une alerte dépend fortement du contexte disponible.

Une alerte peut sembler suspecte ou légitime selon l’utilisateur concerné, son rôle, ses accès habituels, la machine impliquée, sa fonction dans l’entreprise ou encore sa position dans le réseau.

J’ai aussi compris l’intérêt des workbooks : ils permettent de guider l’analyste L1 avec une méthode claire, d’éviter les oublis et de standardiser le traitement des alertes.

Enfin, les lookups comme l’inventaire des identités, l’inventaire des actifs ou les diagrammes réseau permettent d’enrichir une alerte et d’améliorer la qualité du verdict.

## 6. Difficultés rencontrées

- Ne pas confondre les différentes ressources utilisées pendant le triage : inventaire des identités, inventaire des actifs, diagramme réseau et workbook.
- Comprendre que ces ressources ne donnent pas directement un verdict, mais permettent d’ajouter du contexte pour prendre une décision plus fiable.

## 7. Déclics / points importants

Le principal déclic de cette room est qu’une alerte ne doit pas être analysée uniquement à partir de ses champs techniques.

Pour prendre une décision fiable, un analyste SOC L1 doit souvent enrichir l’alerte avec du contexte : rôle de l’utilisateur, accès autorisés, fonction de la machine, localisation, adresse IP, sous-réseau ou chemin réseau.

J’ai aussi retenu que les workbooks permettent de réduire les oublis et de rendre le triage plus régulier, surtout pour des analystes juniors ou pour des alertes fréquentes.

## 8. Compétences travaillées

- Enrichissement d’une alerte avec du contexte.
- Utilisation d’un inventaire des identités.
- Utilisation d’un inventaire des actifs.
- Lecture d’un diagramme réseau.
- Compréhension du rôle des lookups dans le triage SOC.
- Structuration d’une investigation avec un workbook.
- Suivi d’un workflow d’analyse.
- Meilleure compréhension du lien entre utilisateur, machine, réseau et alerte.

## 9. À approfondir

- Se familiariser avec la lecture des diagrammes de réseau