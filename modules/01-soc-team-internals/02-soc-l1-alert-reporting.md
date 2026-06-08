# SOC L1 Alert Reporting

## Synthèse rapide

- **Sujet principal** : reporting d'alertes SOC.
- **Objectif de la room** : comprendre comment rédiger un rapport d’alerte clair, quand escalader une alerte, et comment communiquer efficacement en cas de situation critique.
- **Compétences travaillées** : rédaction de rapport, justification d’un verdict, escalade vers le L2, communication avec les équipes concernées et gestion des situations critiques.
- **Lien métier** : cette room correspond aux premières actions attendues d'un analyste SOC L1 face à un dashboard d'alertes.

## 1. Contexte de la room

Cette room introduit trois compétences importantes pour un analyste SOC L1 : la rédaction d’un rapport d’alerte, l’escalade vers un analyste L2 et la communication avec les bonnes parties prenantes.

L’objectif est de comprendre comment documenter une alerte de manière claire, transmettre le bon contexte lors d’une escalade, et communiquer efficacement lorsque la situation nécessite une coordination avec d’autres équipes.

## 2. Objectifs d'apprentissage

- Savoir rédiger un rapport.
- Savoir quand et pourquoi escalader.
- Communiquer de manière efficace pendant ou après l'analyse.

## 3. Notions clés

- **Donner du contexte pour l'escalade** : un rapport correctement rédigé permet au L2 de gagner du temps et l'aide à comprendre rapidement ce qui s'est passé.

- **Conserver les conclusions pour les archives** : les logs bruts d'un SIEM sont souvent conservés pendant une durée limitée, alors que les alertes peuvent être conservées plus longtemps selon les outils et les procédures internes. Il est donc important d'ajouter le contexte utile directement dans l'alerte.

- **Améliorer les compétences d'investigation** : si l'on ne peut pas expliquer simplement une alerte, c'est qu'elle n'est probablement pas encore bien comprise. Rédiger des rapports est donc un bon moyen d'améliorer les compétences de synthèse et d'analyse d'un L1.

- **Alert reporting** : formalisation des éléments observés pendant l’analyse d’une alerte, afin de conserver le contexte et de faciliter la reprise par un autre analyste.

- **Alert escalation** : transmission d’une alerte à un analyste L2 ou à une équipe plus adaptée lorsque l’alerte nécessite une investigation plus approfondie, une remédiation ou une décision hors périmètre L1.

- **Communication SOC** : échanges avec les analystes, équipes IT, métiers, utilisateurs ou responsables lorsque des informations supplémentaires ou une coordination sont nécessaires.

## 4. Méthodologie / raisonnement

La méthode des 5W est utilisée pour écrire un rapport synthétique et compréhensible (Who, What, When, Where, Why) et fait suite à la room précédente [SOC L1 Alert Triage](01-soc-l1-alert-triage.md).

### 1. Comprendre l'entonnoir d'alerte

- Le bruit est d'abord filtré par le L1 qui escalade les vraies menaces vers le L2. 
- Les vrais positifs sont traités par les L2, qui peuvent escalader vers une équipe DFIR si une réponse à incident est nécessaire.
- Le DFIR s'occupe des incidents et des investigations approfondies, ce qui demande également une communication entre plusieurs équipes.
- Le but est de protéger les données.

### 2. Guide de rédaction d'un rapport

Pour rédiger un rapport utile, il est important de se demander ce qu'un analyste L2, une équipe DFIR ou une équipe IT aurait besoin de comprendre rapidement. La méthode des 5W permet de structurer les informations essentielles :

1. **Who (Qui)** : Quel utilisateur est connecté, quelle(s) commande(s) a/ont été utilisé(es), ou quel(s) fichier(s) a/ont été téléchargé(s) ?

2. **What (Quoi)** : Quelle action ou évènement a été réalisé ?

3. **When (Quand)** : Quand exactement l'activité suspecte a commencé et s'est terminée ?

4. **Where (Où)** : Quel hôte, quelle adresse IP ou quel site web est impliqué dans l'alerte ?

5. **Why (Pourquoi)** : Le point le plus important de la rédaction, le raisonnement qui conduit au verdict final.


### 3. Guide de l'escalade

Une fois le rapport rédigé et le verdict défini, l’analyste L1 doit décider si l’alerte doit être escaladée vers le L2.
Les recommandations suivantes sont celles qui correspondent généralement aux équipes SOC.
On doit généralement escalader si :

1. L’alerte peut indiquer une cyberattaque majeure nécessitant une investigation plus approfondie ou l’intervention d’une équipe DFIR.
2. Des actions de remédiation sont nécessaires, comme la suppression d’un malware, l’isolation d’un hôte ou la réinitialisation d’un mot de passe.
3. Une communication avec des clients, partenaires, équipes internes, management ou autorités est nécessaire.
4. L’analyste L1 ne comprend pas totalement l’alerte et a besoin de l’appui d’un analyste plus expérimenté.

### 4. SOC communication

Chaque SOC possède généralement ses propres procédures de communication en cas de crise.
S'il n'y en a pas, voici certains scénarios qui aident à les gérer efficacement :

- **Si besoin d'escalade urgente, d'alerte critique, mais que le L2 n'est pas disponible ou ne répond pas.**
    → S'assurer de savoir où trouver des contacts d'urgence. Par exemple, essayer le L2, puis le L3 et enfin le manager.
- **Une alerte concerne un compte Teams/Slack compromis et nécessite de valider la connexion avec l'utilisateur concerné.**
    → Ne pas contacter l'utilisateur via le canal potentiellement compromis, utiliser une méthode alternative, comme un appel téléphonique.
- **Si l'on reçoit un grand nombre d'alertes sur une courte période de temps, dont certaines sont critiques.**
    → Prioriser les alertes, comme vu dans la room précédente pour le triage, et informer le L2 en poste à ce moment-là.
- **Après plusieurs jours, on réalise que l'on a mal classifié une alerte et que ce serait une action malveillante.**
    → Contacter immédiatement le L2 et expliquer les inquiétudes. Les acteurs malveillants peuvent rester silencieux plusieurs semaines avant l'impact.
- **L'impossibilité de compléter le triage d'alertes, si les logs du SIEM ne sont pas correctement analysés ou ne sont pas consultables.**
    → Il faut investiguer avec les éléments disponibles et remonter le problème au L2 ou au SOC engineer
.

## 5. Ce que j'ai appris

Cette room m’a permis de comprendre que le reporting d’alerte n’est pas une simple formalité. Un bon rapport permet de transmettre rapidement le contexte au L2, de conserver les éléments importants dans l’historique de l’alerte et de justifier clairement le verdict.

J’ai aussi compris que l’escalade n’est pas seulement liée à la gravité d’une alerte. Elle peut être nécessaire lorsqu’une remédiation est requise, lorsqu’une autre équipe doit être impliquée, ou lorsqu’un analyste L1 manque d’éléments pour conclure correctement.

Enfin, la communication est une compétence essentielle dans un SOC, car une alerte peut nécessiter des échanges avec le L2, le SOC manager, les équipes IT, les utilisateurs ou d’autres parties prenantes.

## 6. Difficultés rencontrées

- Rédiger de manière claire et synthétique un rapport avec le contexte nécessaire.

## 7. Déclics / points importants

Le principal déclic de cette room est que la qualité d’une escalade dépend directement de la qualité du rapport. Un L2 doit pouvoir comprendre rapidement ce qui a été observé, pourquoi le verdict a été choisi et quelles actions peuvent être nécessaires.

J’ai aussi retenu que la communication fait partie intégrante du travail SOC. Une alerte peut nécessiter des échanges avec le L2, les équipes IT, un utilisateur, le management ou d’autres parties prenantes.

## 8. Compétences travaillées

- Analyse d'une alerte.
- Rédaction d'un rapport clair et synthétique.
- Justification d'un verdict.
- Transmission du contexte utile à un analyste L2.
- Compréhension des critères d'escalade.
- Communication avec les équipes internes ou parties prenantes.
- Gestion de situations critiques ou ambiguës.

## 9. À approfondir

- M'entraîner à l'analyse de logs afin de gagner en efficacité.
- Continuer à rédiger des rapports types pour prendre des automatismes.
- Améliorer ma capacité à justifier un verdict de manière courte et claire.
- Mieux comprendre les procédures d'escalade et de communication utilisées dans un SOC réel.