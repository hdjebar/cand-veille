# DJEBAR HAMMOUCHE

Luxembourg City | +352 661 419 771 | dhammouche@gmail.com  
[linkedin.com/in/hdjebar](https://linkedin.com/in/hdjebar) | [github.com/hdjebar](https://github.com/hdjebar)

---

## Responsable projets IA et Data

La BnL a numérisé huit millions d’articles de presse historique. Ils sont accessibles. Ils ne sont pas interrogeables — pas au sens où un chercheur peut demander toutes les mentions d’un personnage sur cent ans et obtenir une réponse en quelques secondes. Intelligent Luxembourg Heritage adresse ce gap sur les données CC0 de data.bnl.lu : CER 0,88 % avec Qwen3-VL en few-shot, 4× sous l’état de l’art, bbox pixel natif, zéro GPU, zéro fine-tuning — 1 702 blocs annotés transformés en avantage architectural. Premier corpus FR/DE/LB post-correction en CC0 pour ALT-EDIC (CENL 2025). Piloter ce type de projet — de la modélisation d’information à la connexion aux systèmes productifs — dans des institutions qui ont leur propre façon de décider, c’est ce que je construis depuis dix ans.

---

## Compétences clés

| **IA/ML & Traitement de données** | **Gestion de projets & Gouvernance** |
|---|---|
| LangChain, LangGraph, RAG/GraphRAG, NLP/TAL, Deep Learning, Apprentissage automatique, Bases vectorielles, MLOps, Données massives, Données ouvertes, Vision par ordinateur, Modèles open weights, Fine-tuning, Catalogage automatique | QUAPITAL-HERMES, CRISP-ML(Q), SAFe, Scrum, PM2, PRINCE2, ITIL v4, PMI-CPMAI, Conduite du changement, Coordination pluridisciplinaire, Pilotage périmètre/planning/budget |

| **Architecture & Systèmes** | **Sécurité & Conformité** |
|---|---|
| TOGAF, ArchiMate, Microservices, API Management, Bases de données, Docker, Kubernetes, CI/CD | GDPR, ISO 27001, NIS2, DORA, EU AI Act, Zero Trust, IAM |

| **Technologies opérationnelles (OT)** | **Interopérabilité données** |
|---|---|
| Logistique de distribution, Gestion d’entrepôt/magasinage, Automatisation des flux physiques, RFID, Systèmes robotisés de stockage, TLS | SDMX (échanges Eurostat/STATEC) |

| **Développement & Intégration** | **Cloud & MLOps** |
|---|---|
| Python, SQL/PL-SQL, REST APIs, OpenAPI, ETL, Kafka, SDMX, .NET, Java EE | Azure, AWS, Microsoft Power Platform, Git, JIRA, Confluence |

---

## Expérience professionnelle

### Architecte IA & Data | Projets & missions | Luxembourg
**2014 – présent**

*Missions en parallèle pour des institutions publiques et entreprises luxembourgeoises. Sélection :*

---

> **Proposition de projet – Intelligent Luxembourg Heritage**
>
> La BnL a numérisé huit millions d’articles de presse historique luxembourgeoise (1840 à nos jours, DE/FR/LB). Ces textes sont accessibles ; les entités qu’ils contiennent — personnes, lieux, organisations, événements — ne le sont pas. Aucun chercheur ne peut aujourd’hui demander « toutes les mentions de tel personnage entre 1900 et 1914 » et obtenir une réponse en quelques secondes.
>
> ILH construit le pipeline qui comble ce gap : extraire automatiquement ces entités, les relier au catalogue bibnet.lu et à Wikidata, et les rendre interrogeables depuis eluxemburgensia.lu. La preuve de concept a été développée sur les données ouvertes CC0 de data.bnl.lu et validée sur les mêmes images de référence que la baseline officielle Nautilus-OCR.

---

**Intelligent Luxembourg Heritage, BnL (2025 – en cours)**

*Pour tous :* Huit millions d’articles en allemand, français et luxembourgeois. Numérisés, mais pas enrichis — les noms de personnes, de lieux, d’organisations sont dans le texte, indistinguables du reste. ILH les extrait, les relie au catalogue bibnet.lu et à Wikidata, et les rend accessibles depuis eluxemburgensia.lu. Un chercheur, un généalogiste, une commune retrouve cent ans de mentions en quelques secondes. Les données sont dissiminées en CC0 pour accompagner les chercheurs dans l’usage des données ouvertes de la BnL.

*Technique :* Pipeline METS/ALTO → VLM (Qwen3-VL, open weights Apache 2.0) → OCR + NER (PER, LOC, ORG, DATE) + bbox pixel natif → entity linking Wikidata/ARK (NAAN 70795) → knowledge graph bibnet.lu. Connexion aux systèmes productifs BnL : Nautilus-OCR → METS/ALTO existant → ILH → eluxemburgensia.lu. Phase 3+ : robot feuilleteur → frames vidéo → VLM. Piloté sous QUAPITAL-HERMES/CRISP-ML(Q), EU AI Act Phase 0 (Art. 50, AIPD). Partenariats : Uni.lu, C²DH, Impresso Phase 2.

Résultats POC : CER 0,88 % (Qwen3-VL few-shot) vs Nautilus/Kraken 3,68 % (Schneider 2023), gain 4×, zéro GPU, zéro fine-tuning, données CC0. Localisation bbox pixel native : surlignage direct sur les scans. Le few-shot comme brique d’un cycle auto-améliorant : oracle de sélection SFT (0,88 % vs 3,54 % zero-shot), amorcé QLoRA sur signal propre, générateur de paires synthétiques depuis les 10 880 pages de L’Union (1860–1869, CC0) sans annotation humaine, récompense GRPO CER+IoU. Pool few-shot : Ground Truth Pack (33 000 lignes, 99,95 %), Sample Pack (11 titres DE/FR, 1845–1877), D’Wäschfra 1868 (lb XIXe). 1 702 blocs annotés transformés en avantage architectural. Pipeline conçu pour 800 000 pages (DE/FR/LB). Soumission HIPE-OCRepair 2026 prête. Premier corpus FR/DE/LB post-correction CC0 pour ALT-EDIC (CENL 2025).  
→ [github.com/hdjebar/IntelligentLuxembourgHeritage](https://github.com/hdjebar/IntelligentLuxembourgHeritage)

**Plateforme RAG multimodale, institution financière (2024–2025, 14 mois)**  
Co-construit avec les équipes métier et IT une plateforme de recherche sémantique sur des dépôts hétérogènes : documents, images, données structurées. Pipeline ingestion multimodale → post-correction OCR → embeddings → LangChain avec attribution des sources → NER. Ce qui prenait des heures de navigation manuelle entre silos se résout en quelques secondes. Même architecture de fond qu’ILH, appliquée au secteur financier.

**Plateforme d’aide à la décision architecturale, groupe d’assurance (2023–2024, 8 mois)**  
Bâti avec une équipe d’architectes enterprise une plateforme GraphRAG couplant LangChain, bases vectorielles et standards ArchiMate. Les architectes interrogent en langage naturel une documentation technique qui restait dans des silos inaccessibles en temps réel. Même défi qu’eluxemburgensia.lu : rendre cherchable ce qui ne l’est pas.

**Système d’analyse prédictive en santé, Agence de la Biomédecine, France (2022–2023)**  
Développé avec les équipes médicales des algorithmes de scoring ML pour l’allocation de greffons hépatiques. De la préparation des données à la validation clinique, avec les cliniciens à chaque étape — ce qui exige d’expliquer des concepts complexes à des interlocuteurs non techniques et que le système soit adopté, pas seulement livré.

**Développement de skills Claude AI (2024–2025)**  
*ai-methodologies* : CRISP-DM, CRISP-ML(Q), LLMOps, EU AI Act. *enterprise-architecture* : 50+ frameworks (ArchiMate, BPMN, TOGAF, sécurité, MLOps). *eu-ai-act-compliance* : classification des risques, obligations GPAI, conformité Art. 9-15.

---

### Architecte d’entreprise | Société Générale Luxembourg | Luxembourg
**Juillet 2023 – Mars 2024**

*Architecture sur quatre juridictions : Luxembourg, Paris, Suisse, Monaco.*

Quatre juridictions — autant de façons différentes de résister. Co-construit une stratégie cloud conforme CSSF avec les parties prenantes réglementaires. Déployé des standards enterprise pour le management des API et la sécurité. Traduit des décisions architecturales en programmes de changement que les équipes ont réellement adoptés.

---

### Programme Data Science avancée | Paris Mines Tech | Paris
**Novembre 2022 – Mars 2023**

Programme exécutif intensif : machine learning avancé, deep learning, big data, IA en santé numérique. Livré un système speech-to-text ML de bout en bout ; hackathons santé avec fine-tuning et évaluation sur données contraintes.

---

### Architecte d’entreprise | KPMG Luxembourg | Luxembourg
**Décembre 2021 – Octobre 2022**

Co-construit avec la direction la pratique EA interne ; automatisé les opérations de données ServiceNow via PowerShell ; co-défini les frameworks de gouvernance Microsoft Power Platform ; architecturé les capacités d’analytics cloud pour une BI quasi-temps réel.

---

### Architecte & Analyste métier | Luxembourg Conseil | Luxembourg
**Mars 2015 – Novembre 2021**

*Missions multi-secteurs : gouvernement, pharma, services financiers, emploi.*

- **Agence de paiement wallonne :** reconfiguré l’architecture enterprise de bout en bout avec les équipes métier : délais de traitement réduits de semaines à jours ; référentiel EA dans ArchiMate/Sparx EA ; reporting batch remplacé par une BI temps réel.
- Piloté des projets pluridisciplinaires sur BPM, gouvernance des données, migration cloud et IAM ; chacun livré dans le périmètre, le planning et le budget convenus.

---

### Architecte BPM d’entreprise | STATEC | Luxembourg
**Octobre 2014 – Février 2015**

Bâti la démarche EA et BPM alignée sur les standards statistiques européens (ESS, GSBPM, GAMSO, CEAF). Échanges avec Eurostat via SDMX — le même type de format structuré que les METS/ALTO et OAI-PMH de la BnL.

---

### Consultant IT | COPROCESS SA | Luxembourg
**Janvier 2012 – Septembre 2014**

Audits IT, transformation enterprise, optimisation processus santé (approche TLS) ; restructuration de flux physiques : logistique de distribution, gestion de magasinage, automatisation d’entrepôt. Co-fondé LuxBA et LuxEA, les deux communautés de pratique luxembourgeoises en analyse métier et architecture d’entreprise.

---

### Analyste métier & Chef de projet IT | Commission européenne | Bruxelles/Luxembourg
**Juin 2007 – Décembre 2011**

Co-développé le programme d’architecture enterprise et la méthodologie BPM ; re-enginéeré avec les équipes eGreffe les systèmes documentaires pour la conformité au Traité de Lisbonne ; reconfiguré avec DG Traduction les workflows de services linguistiques ; piloté la livraison IT des systèmes financiers et d’identité pour l’élargissement européen.

---

### Architecte ERP & Responsable PMO IT | Parlement européen | Luxembourg/Bruxelles
**Septembre 2002 – Décembre 2006**

Conçu et mis en œuvre avec les équipes RH les systèmes de gestion du personnel sur la suite Oracle ERP ; co-construit avec la direction le PMO IT du Parlement : standards de gouvernance, méthodologies, livraison prévisible, au service de l’institution et de son bien commun.

---

### Ingénieur R&D | IST Luxembourg | Luxembourg
**2000 – 2002**

Co-développé la méthodologie Model-Driven Architecture pour les systèmes distribués dans le cadre du projet européen FIDJI.

---

### Consultant technologie | Lagardère / Linagora | Paris
**2000**

Études de faisabilité et architecture technique pour l’adoption web enterprise ; gestion de plateformes Linux open source.

---

## Formation

**Certification Cloud & Outsourcing Officer** | House of Training & ABBL | Juin 2025  
**Certification Programme Data Science & ML** | Paris Mines Tech | Novembre 2022 – Mars 2023  
**Master en Technologies de l’Information et de la Communication** | INPL, Nancy | 1999 – 2000  
**Préparation doctorat en Mathématiques appliquées** | Université Nancy / INRIA | 1994 – 1996  
*Comportement asymptotique des équations aux dérivées partielles*  
**Master en Mathématiques appliquées (MIM)** | Université de Metz | 1993 – 1994  
**Formations professionnelles :** PMI-CPMAI | Professional Scrum Master | PMP | TOGAF | PRINCE2 | ITIL | IIBA/BABOK

---

## Reconnaissance & engagement

Expert contributeur : « The Leader’s Guide to Radical Management » (Stephen Denning).  
Co-fondateur, Luxembourg Business Analysis (LuxBA) et Enterprise Architecture (LuxEA) Communities of Practice.  
Membre actif, PMI Luxembourg Chapter et Agile Luxembourg Community.

---

## Langues

**Français :** natif (C2) | **Anglais :** professionnel avancé (C1)  
Je sollicite la dispense de deux des trois langues administratives prévue pour le groupe A1 dans les conditions d’admission du poste.  
*L’usage de l’anglais dans les expériences et publications internationales est conforme aux pratiques du secteur GLAM (AI4LAM, LIBER, ICDAR, Impresso) et des institutions scientifiques luxembourgeoises.*
