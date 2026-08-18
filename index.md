---
title: ""
---

Laval, QC  
mikael.lapierre.1@ens.etsmtl.ca | 438-888-8272  | Bilingue

---

## Formation

**Baccalauréat en génie logiciel** – ÉTS, Montréal  
*2023 – présent*  

**Diplôme d'études collégiales en sciences de la nature** – Collège Montmorency  
*2020 – 2023*  

---

## Participation académique

**Membre de l'équipe eSports de l'ÉTS**  
*Participation active aux compétitions et événements eSports de l'école*

---

## Compétences

- **Langages :** Java, C#, JavaScript/TypeScript, Python, C/C++  
- **Back-end :** .NET (ASP.NET Core, MVC), Node.js, Express.js, REST, GraphQL, DDD  
- **Bases de données :** SQL (conception & optimisation), MongoDB, PostgreSQL  
- **Cloud & DevOps :** AWS (Lambda, ECS/Fargate, SageMaker), Terraform (IaC), Docker, Kubernetes, CI/CD (GitHub Actions, GitLab CI/CD), Dynatrace (observabilité)  
- **Architecture distribuée :** microservices, API Gateway, Saga, CQRS, Event Sourcing, Pub/Sub, résilience (Circuit Breaker, observabilité)  
- **Sécurité :** SSO (Azure AD / MSAL), sécurisation des communications API  
- **Tests :** unitaires, intégration, acceptation, E2E  
- **Outils IA :** Claude Code, Codex, GitHub Copilot, ChatGPT, Claude — context engineering, harness engineering

---

## Expérience professionnelle

**Stagiaire en génie logiciel – Équipe IA (VP Numérique & IA)** – *Loto-Québec, Montréal*  
*01/2026 – 08/2026 — 2 stages coopératifs consécutifs (STA206, STA306)*  
- Conception et livraison d’un **pipeline de traduction automatisée EN→FR** des fiches de règles de jeux, remplaçant un processus externalisé et couvrant 100 % des ~1 000 jeux certifiés annuellement (obligation légale avant mise en ligne) — détails dans *Projets sélectionnés*.  
- Développement d’un **pipeline serverless (AWS Lambda, Python 3.13)** synchronisant quotidiennement les fiches de jeux depuis **SharePoint via Microsoft Graph API**, avec infrastructure **Terraform** complète.  
- Réalisation d’une **application full-stack de tri de candidatures** exploitant plusieurs **LLM en approche LLM as judge**, réduisant d’environ **70 %** le temps de tri manuel — détails dans *Projets sélectionnés*.  
- Mise en place d’un **patron CI/CD 2-dépôts réutilisable** (GitLab CI + Terraform Cloud) avec environnements sandbox éphémères, adopté comme référence pour les initiatives IA de l’équipe.  
- Infrastructure **AWS via Terraform** avec **observabilité via Dynatrace** et **SSO (Azure AD / MSAL)** intégré.  
- Plus de **6 mois de pratique intensive avec Claude Code et Codex** — context engineering, harness engineering, conception d’agents et de workflows IA.  

*Stack : Python · AWS (Lambda, ECS/Fargate, S3, SageMaker, EventBridge, Secrets Manager) · Terraform · Docker · GitLab CI/CD · Dynatrace · Azure AD/MSAL · FastAPI · React · PostgreSQL · Anthropic Claude · Claude Code · Codex · OpenAI · Gemini*  

**Stagiaire en développement logiciel** – *Pro Meubles Inc. (Artopex), Granby*  
*05/2024 – 08/2024*  
- Automatisation complète du processus de mise en production des meubles, auparavant effectué manuellement et consommant énormément de temps.  
- Conception d’un programme en **C#, orienté objet**, à l’aide de patrons de conception (**Singleton, Strategy, FileReader**) pour structurer une architecture **MVC** extensible.  
- Implémentation d’une couche de détection d’erreurs automatisée, remplaçant une vérification manuelle sujette aux erreurs.  
- Rédaction des tests unitaires de la solution.  

**Développeur logiciel — temps partiel** – *Pro Meubles Inc. (Artopex), Granby*  
*09/2024 – Présent*  
- Maintien et support de l’application développée durant le stage.  

---

## Projets sélectionnés

### Pipeline de traduction automatisée EN→FR — Loto-Québec
**Tech utilisées :** Python, AWS (Lambda, ECS/Fargate, SageMaker, EventBridge), Terraform, LLM (sorties structurées), PDF parsing.  
- Conception et livraison d’un pipeline de traduction automatisée des fiches de règles de jeux, remplaçant un processus externalisé et couvrant 100 % des ~1 000 jeux certifiés annuellement (obligation légale avant mise en ligne).  
- Extraction de la mise en page des documents PDF (texte, positions, blocs) pour préserver la structure d’origine lors de la traduction.  
- Entraînement et intégration d’un modèle **YOLO fine-tuné sur AWS SageMaker** pour la détection et l’extraction automatique de logos dans des PDF complexes, avec pipeline de **ré-entraînement automatisé** déclenché par les nouvelles annotations.  
- Traduction par **LLM avec sorties structurées** garantissant la cohérence terminologique et le respect du format des fiches.  
- Orchestration événementielle via **AWS EventBridge** et déploiement du service de traduction sur **ECS Fargate**.  
- Infrastructure entièrement définie en **Terraform** (IaC), avec pipeline CI/CD dédié.  

### Application full-stack de tri de CV — Loto-Québec
**Tech utilisées :** FastAPI, PostgreSQL, React 18, TypeScript, AWS Step Functions, Terraform, Claude, GPT, Gemini.  
- Application entièrement **hébergée sur AWS**, avec traitement **asynchrone** orchestré par **AWS Step Functions** pour le pipeline d’analyse des candidatures.  
- Backend **FastAPI** exposant une API REST consommée par un frontend **React 18/TypeScript**, avec persistance **PostgreSQL** des candidatures et des résultats de tri.  
- Approche **LLM as judge** : évaluation et notation des candidatures par plusieurs **LLM (Claude, GPT, Gemini)** avec sorties structurées.  
- Pondération transparente des critères de scoring, ajustable et auditable, pour classer les candidatures.  
- Infrastructure définie en **Terraform** avec pipeline **CI/CD** de déploiement automatisé.  
- Traitement de **300+ CV en moins de 5 minutes**, réduisant d’environ **70 %** le temps de tri manuel, avec une pertinence supérieure à 85 % par rapport au jugement RH.  
- Garde-fous d’équité intégrés : validation humaine obligatoire avant toute décision, pondération transparente.  

### BrokerX — plateforme de courtage en microservices événementielle (branche `event-driven`)
**Tech utilisées :** ASP.NET Core (.NET 8), Kafka, Redis, Kong Gateway, React 19/TypeScript, Prometheus/Grafana, Kafdrop, Docker Compose.
- Architecture en microservices .NET 8 (`identity-api`, `orders-api`, `wallets-api`, `market-data-api`) exposés via un **API Gateway Kong** (routage, CORS, authentification).  
- `orders-api` : validation synchrone des ordres avec **pattern Outbox**, moteur de matching en tâche de fond, caches **Redis**, publication d’événements Kafka (`wallet-commands`, `execution-reports`, `order-placed-events`).  
- `wallets-api` : gestion des soldes et du ledger, consommation asynchrone des commandes de portefeuille (`wallet-commands`) et publication des résultats (`wallet-command-results`).  
- Implémentation d’une **saga chorégraphique** (sans orchestrateur central) coordonnant Orders ↔ Wallets par échange de messages Kafka.  
- Diffusion temps réel des carnets d’ordres et mises à jour de marché via **SignalR** (`market-data-api`), alimentée par les événements Kafka.  
- Authentification et gestion de compte (`identity-api`) : JWT, MFA par SMS (Twilio), vérification par courriel (SendGrid).  
- Observabilité complète : **Prometheus** (métriques), **Grafana** (tableaux de bord), **Kafdrop** (inspection des topics Kafka), exporteurs Postgres/Redis.  
- Documentation d’architecture professionnelle : registre de décisions d’architecture (**ADR**) et diagrammes **arc42**, modélisation **DDD**.  

### Automatisation de la mise en production — Pro Meubles Inc. (Artopex)
**Tech utilisées :** C#, .NET, WinForms, Design Patterns, MVC.  
- Automatisation complète d’un processus de mise en production auparavant effectué manuellement et consommant énormément de temps, remplacé par une application desktop.  
- Conception d’un programme **orienté objet** structuré en architecture **MVC**, avec une couche **Controller** orchestrant les interactions entre l’analyse des données et l’interface utilisateur.  
- Utilisation de patrons de conception (**Singleton, Strategy, FileReader**) pour permettre le support extensible de plusieurs formats de fichiers d’entrée sans modifier la logique existante.  
- Implémentation d’une couche de détection d’erreurs automatisée, remplaçant une vérification manuelle sujette aux erreurs et générant des alertes ciblées pour correction en amont.  
- Conception d’une interface intuitive utilisable sans expertise technique, facilitant l’adoption par les équipes de production.  
- Rédaction des tests unitaires de la solution et maintien continu de l’application en poste à temps partiel après le stage.  

