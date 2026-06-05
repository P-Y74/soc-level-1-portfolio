# SOC L1 Alert Triage

## Synthèse rapide

- **Sujet principal** : triage d'alertes SOC.
- **Objectif de la room** : comprendre le cycle événement → log → alerte, puis appliquer un workflow simple de triage.
- **Compétences travaillées** : lecture d'alertes, priorisation, assignation, investigation initiale, verdict, commentaire et clôture.
- **Lien métier** : cette room correspond aux premières actions attendues d'un analyste SOC L1 face à un dashboard d'alertes.

## 1. Contexte de la room

Cette room introduit le concept d'alerte dans un SOC et le rôle du triage pour un analyste SOC L1.

L'objectif est de comprendre comment une activité observée dans un environnement informatique peut devenir une alerte à traiter dans un dashboard SOC. La room explique le cycle de base : un événement se produit, il est journalisé par un système, les logs sont envoyés vers une solution de sécurité, puis une alerte est générée lorsqu'une activité correspond à une règle ou à un comportement à surveiller.

La room met également en avant l'importance du triage : face à un grand nombre d'alertes, l'analyste L1 doit savoir lesquelles traiter en priorité, comment les prendre en charge, comment les analyser, puis comment les clôturer avec un verdict et un commentaire cohérent.

Cette première room pose donc les bases du travail quotidien d'un analyste SOC L1 : comprendre les alertes, les prioriser, les investiguer et documenter la décision prise.

## 2. Objectifs d'apprentissage

- Comprendre ce qu'est une alerte SOC.
- Comprendre comment un événement peut devenir une alerte.
- Identifier les principales propriétés d'une alerte.
- Comprendre les différents statuts et verdicts possibles.
- Apprendre à prioriser les alertes dans un dashboard SOC.
- Comprendre les étapes principales du triage d'une alerte.
- Pratiquer un workflow simple de triage dans un environnement simulé.

## 3. Notions clés

- **Événement** : action ou activité qui se produit dans un système, comme une connexion utilisateur, le lancement d'un processus ou le téléchargement d'un fichier.

- **Log** : trace enregistrée par un système, un OS, un firewall, un service cloud ou une autre source technique après qu'un événement s'est produit.

- **Alerte** : notification générée par une solution de sécurité lorsqu'un événement ou une séquence d'événements correspond à une règle de détection ou à une activité considérée comme suspecte.

- **SIEM** : solution permettant de centraliser, corréler et analyser des logs de sécurité. Dans la room, le SIEM est présenté comme une plateforme courante pour gérer les alertes SOC.

- **EDR / NDR** : solutions orientées endpoint ou réseau, capables de générer leurs propres alertes et dashboards.

- **SOAR** : solution permettant d'agréger, centraliser ou automatiser certaines actions autour des alertes, plutôt utilisée dans des SOC plus matures.

- **ITSM** : outil de gestion de tickets ou de workflows pouvant être utilisé pour suivre le traitement des alertes.

- **Alert Status** : état de traitement de l'alerte, par exemple `New`, `In Progress` ou `Closed`.

- **Alert Verdict** : classification finale de l'alerte après analyse, par exemple `True Positive` ou `False Positive`.

- **Alert Assignee** : analyste responsable du traitement de l'alerte.

- **Triage** : processus de prise en charge, d'analyse, de qualification et de clôture d'une alerte.

## 4. Méthodologie / raisonnement

La room propose une approche simple et opérationnelle du triage d'alertes.

### 1. Choisir la bonne alerte à traiter

Avant de commencer l'analyse, il faut sélectionner une alerte pertinente dans le dashboard :

- ne pas prendre une alerte déjà assignée à un autre analyste ;
- ne pas prendre une alerte déjà en cours d'investigation ;
- privilégier les alertes encore nouvelles ou non résolues.

### 2. Prioriser les alertes

La priorisation se fait principalement selon deux critères :

1. **La sévérité**
   - commencer par les alertes critiques ;
   - puis les alertes high ;
   - ensuite medium ;
   - puis low.

2. **Le temps**
   - à sévérité équivalente, commencer par l'alerte la plus ancienne.

L'idée importante est qu'une alerte ancienne peut correspondre à une activité malveillante déjà en cours depuis plus longtemps. Elle doit donc être traitée avant une alerte plus récente de même niveau.

### 3. Prendre en charge l'alerte

Une fois l'alerte sélectionnée, les premières actions consistent à :

- s'assigner l'alerte ;
- changer son statut en `In Progress` ;
- lire le nom de l'alerte ;
- lire sa description ;
- identifier les champs importants ;
- comprendre ce que l'alerte signale.

Cette étape évite que plusieurs analystes travaillent sur la même alerte et permet d'assumer clairement la responsabilité de son traitement.

### 4. Investiguer l'alerte

L'investigation consiste à comprendre si l'activité observée est légitime ou suspecte.

La room met en avant plusieurs réflexes :

- identifier qui ou quoi est concerné par l'alerte ;
- comprendre l'action décrite ;
- regarder les événements autour de l'alerte ;
- utiliser les ressources disponibles, comme les logs, les workbooks, les playbooks, les runbooks ou la threat intelligence si nécessaire.

### 5. Prendre une décision

Après investigation, l'analyste doit déterminer si l'alerte correspond à une menace réelle ou non.

Le verdict peut être par exemple :

- `True Positive` si l'alerte correspond à une activité réellement malveillante ou suspecte ;
- `False Positive` si l'alerte ne représente pas une menace réelle.

### 6. Documenter et clôturer

La dernière étape consiste à :

- rédiger un commentaire expliquant le raisonnement ;
- indiquer les éléments observés ;
- justifier le verdict ;
- repasser l'alerte dans le dashboard ;
- la passer au statut `Closed`.

Cette étape est importante car la décision doit rester compréhensible après coup, que ce soit pour un autre analyste, un analyste L2 ou le suivi qualité du SOC.

## 5. Analyse ou exercice réalisé

La room est organisée en six tasks qui introduisent progressivement le cycle de vie d'une alerte SOC.

| Task | Sujet | Ce que j'en retiens |
|---|---|---|
| Task 1 | Introduction | Une alerte est un élément central du travail SOC. Elle doit être traitée correctement pour éviter de manquer une menace réelle. |
| Task 2 | Events and Alerts | Une alerte provient d'un ou plusieurs événements journalisés puis analysés par une solution de sécurité. |
| Task 3 | Alert Properties | Les champs d'une alerte permettent de comprendre son contexte : temps, nom, sévérité, statut, verdict, assignation, description. |
| Task 4 | Alert Prioritisation | Les alertes doivent être filtrées, puis priorisées par sévérité et ancienneté. |
| Task 5 | Alert Triage | Le triage suit un workflow : assignation, passage en cours, investigation, verdict, commentaire et clôture. |
| Task 6 | Conclusion | Le triage est une base du rôle SOC L1 avant d'aborder le reporting, l'escalade et les actions L2. |

## 6. Ce que j'ai appris

Cette room m'a permis de mieux comprendre le cycle de vie d'une alerte SOC.

J'ai appris qu'une alerte ne sort pas de nulle part : elle est liée à un ou plusieurs événements, eux-mêmes enregistrés dans des logs, puis analysés par une solution de sécurité comme un SIEM, un EDR, un NDR ou un SOAR.

J'ai aussi compris que le rôle du SOC L1 est très opérationnel. L'analyste doit prendre en charge les alertes, éviter les doublons de traitement, respecter une logique de priorisation, investiguer les éléments disponibles, choisir un verdict et documenter sa décision.

Un autre point important est la distinction entre le statut et le verdict. Le statut indique où en est le traitement de l'alerte, tandis que le verdict indique le résultat de l'analyse.

## 7. Difficultés rencontrées

- Bien distinguer les notions d'événement, de log et d'alerte.
- Comprendre la différence entre le statut d'une alerte et son verdict.
- Ne pas se fier uniquement au nom de l'alerte pour conclure.
- Garder une méthode claire dans le choix de l'alerte à traiter.
- Comprendre pourquoi l'ancienneté d'une alerte est un critère important à sévérité égale.

## 8. Déclics / points importants

Le principal déclic de cette room est que le triage d'alertes commence avant même l'investigation technique.

Avant d'analyser une alerte, il faut déjà choisir la bonne alerte, vérifier qu'elle n'est pas déjà prise en charge, la prioriser correctement, puis s'en attribuer la responsabilité.

J'ai aussi retenu que le triage n'est pas seulement une décision finale. C'est un workflow complet : sélection, assignation, analyse, verdict, commentaire et clôture.

Enfin, j'ai compris que la qualité du commentaire final est importante. Même dans une analyse L1, il faut laisser une trace claire de ce qui a été observé et de la raison du verdict choisi.

## 9. Lien avec le rôle de SOC Analyst L1

Cette room est directement liée au travail d'un analyste SOC L1.

Le L1 est souvent le premier analyste à voir et traiter les alertes. Son rôle est de :

- surveiller le dashboard SOC ;
- choisir les alertes à traiter en priorité ;
- prendre en charge une alerte ;
- comprendre les informations disponibles ;
- mener une première investigation ;
- déterminer un verdict ;
- documenter son raisonnement ;
- clôturer ou préparer la suite du traitement selon le workflow de l'équipe.

La room montre aussi que le SOC L1 travaille dans un environnement collectif. Il doit éviter de traiter une alerte déjà prise par quelqu'un d'autre, suivre les statuts du dashboard et produire une analyse exploitable par l'équipe.

## 10. Compétences travaillées

- Compréhension du cycle événement → log → alerte.
- Lecture des propriétés d'une alerte.
- Compréhension des statuts d'alerte.
- Compréhension des verdicts d'alerte.
- Priorisation selon la sévérité.
- Priorisation selon l'ancienneté.
- Prise en charge d'une alerte dans un dashboard.
- Investigation initiale.
- Rédaction d'un commentaire de triage.
- Clôture d'une alerte.

## 11. À approfondir

- Mieux comprendre le fonctionnement d'un SIEM dans la génération d'alertes.
- Approfondir le rôle des règles de détection.
- Étudier des exemples concrets de statuts et verdicts dans différents outils SOC.
- Pratiquer la rédaction de commentaires de triage courts et précis.
- Comprendre comment utiliser efficacement un workbook, playbook ou runbook.
- Approfondir la différence entre une alerte à clôturer et une alerte à escalader.
- Continuer avec la room suivante sur l'alert reporting pour mieux comprendre la documentation et la communication autour des alertes.