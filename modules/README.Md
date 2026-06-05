# Modules du parcours SOC Level 1

Ce dossier regroupe les différents modules du parcours **SOC Level 1**.

Chaque module possède son propre dossier. À l'intérieur de chaque dossier, je documente les rooms associées sous forme de notes d'apprentissage, d'analyses et de synthèses.

L'objectif est de suivre ma progression de manière structurée, tout en développant une approche professionnelle autour des compétences attendues d'un analyste SOC L1 : triage d'alertes, analyse de logs, phishing, SIEM, supervision réseau, threat intelligence, détection et investigation.

> Les notes présentes dans ce portfolio ne contiennent pas de solutions complètes, de flags ou de réponses directes aux rooms. Elles sont orientées compréhension, méthodologie et retour d'expérience.

## Organisation

Chaque dossier de module suit cette logique :

```text
modules/
└── 01-nom-du-module/
    ├── README.md
    ├── 01-nom-de-la-room.md
    ├── 02-nom-de-la-room.md
    └── module-summary.md
```

* `README.md` : présentation du module et des compétences ciblées.
* `XX-nom-de-la-room.md` : note d'analyse pour une room spécifique.
* `module-summary.md` : synthèse du module une fois terminé.

## Liste des modules

### [01 - SOC Team Internals](01-soc-team-internals/)

Explore les compétences essentielles d'un analyste SOC pour trier, classifier et escalader des alertes dans des environnements SOC réalistes.

### [02 - Core SOC Solutions](02-core-soc-solutions/)

Présente les principales solutions utilisées dans un SOC, notamment les SIEM, EDR et SOAR.

### [03 - Cyber Defence Frameworks](03-cyber-defence-frameworks/)

Introduit les frameworks défensifs comme Pyramid of Pain, Cyber Kill Chain et MITRE afin de mieux comprendre les comportements adverses et améliorer la détection, le triage et la réponse.

### [04 - Phishing Analysis](04-phishing-analysis/)

Couvre l'analyse et la défense contre les emails de phishing à travers des scénarios et techniques d'investigation.

### [05 - Network Traffic Analysis](05-network-traffic-analysis/)

Présente les bases de l'analyse du trafic réseau et l'utilisation de Wireshark pour détecter différents types d'attaques.

### [06 - Network Security Monitoring](06-network-security-monitoring/)

Aborde les fondamentaux de la sécurité réseau, la surveillance des périmètres réseau et l'analyse du trafic ou des logs pour détecter des attaques comme le MITM, la découverte réseau ou l'exfiltration de données.

### [07 - Web Security Monitoring](07-web-security-monitoring/)

Présente la surveillance et la protection des environnements web à travers des labs orientés SOC et des scénarios réalistes.

### [08 - Windows Security Monitoring](08-windows-security-monitoring/)

Explique le fonctionnement des logs Windows et leur utilisation pour détecter des attaques courantes dans des scénarios pratiques.

### [09 - Linux Security Monitoring](09-linux-security-monitoring/)

Explique le fonctionnement des logs Linux et leur utilisation pour détecter des attaques courantes dans des labs orientés détection.

### [10 - Malware Concepts for SOC](10-malware-concepts-for-soc/)

Présente les principaux types de malwares, leur objectif, les bases de l'analyse de fichiers et les attaques de type Living off the Land.

### [11 - Threat Analysis Tools](11-threat-analysis-tools/)

Introduit l'utilisation de la threat intelligence pour détecter, investiguer et défendre contre des adversaires à l'aide de données d'enrichissement et de workflows d'analyse.

### [12 - SIEM Triage for SOC](12-siem-triage-for-soc/)

Montre comment les solutions SIEM aident à détecter des signes précoces d'attaque, investiguer des alertes SOC, corréler des logs et construire une chronologie d'incident.

### [13 - SOC Level 1 Capstone Challenges](13-soc-level1-capstone-challenge/)

Regroupe des challenges permettant d'appliquer les compétences travaillées tout au long du parcours sur des incidents et artefacts variés.

## Retour

* [Retour au README principal](../README.md)
* [Voir la roadmap complète](../learning-roadmap.md)