# DJEBAR HAMMOUCHE

Luxembourg City | +352\u00a0661\u00a0419\u00a0771 | dhammouche@gmail.com  
[linkedin.com/in/hdjebar](https://linkedin.com/in/hdjebar) | [github.com/hdjebar](https://github.com/hdjebar)

---

## Responsable projets IA et Data

En signant le MoU AI4LAM et en portant son programme 2025-2028 \u00e0 171 projets, la BnL a pos\u00e9 un d\u00e9fi pr\u00e9cis\u00a0: passer de dix-sept initiatives IA isol\u00e9es \u00e0 un programme structur\u00e9, livrable en production, au service de la valorisation des collections et de l\u2019accompagnement des chercheurs. J\u2019ai r\u00e9pondu \u00e0 ce d\u00e9fi sur les donn\u00e9es CC0 de data.bnl.lu\u00a0: Intelligent Luxembourg Heritage atteint CER 2,72\u00a0% sans fine-tuning, pilot\u00e9 sous QUAPITAL-HERMES compos\u00e9 avec CRISP-ML(Q). Faire tenir ce type de projet en production dans des institutions \u00e0 gouvernance formelle, c\u2019est ce que je construis depuis dix ans. Je veux apporter ce travail \u00e0 la BnL et le d\u00e9velopper avec les \u00e9quipes qui connaissent les collections et les chercheurs qui en d\u00e9pendent.

---

## Comp\u00e9tences cl\u00e9s

| **IA/ML & Traitement de donn\u00e9es** | **Gestion de projets & Gouvernance** |
|---|---|
| LangChain, LangGraph, RAG/GraphRAG, NLP/TAL, Deep Learning, Apprentissage automatique, Bases vectorielles, MLOps, Donn\u00e9es massives, Donn\u00e9es ouvertes, Vision par ordinateur, Mod\u00e8les open weights, Fine-tuning, Catalogage automatique | QUAPITAL-HERMES, CRISP-ML(Q), SAFe, Scrum, PM2, PRINCE2, ITIL v4, PMI-CPMAI, Conduite du changement, Coordination pluridisciplinaire, Pilotage p\u00e9rim\u00e8tre/planning/budget |

| **Architecture & Syst\u00e8mes** | **S\u00e9curit\u00e9 & Conformit\u00e9** |
|---|---|
| TOGAF, ArchiMate, Microservices, API Management, Bases de donn\u00e9es, Docker, Kubernetes, CI/CD | GDPR, ISO\u00a027001, NIS2, DORA, EU AI Act, Zero Trust, IAM |

| **Technologies op\u00e9rationnelles (OT)** | **Interop\u00e9rabilit\u00e9 donn\u00e9es** |
|---|---|
| Logistique de distribution, Gestion d\u2019entrep\u00f4t/magasinage, Automatisation des flux physiques, RFID, Syst\u00e8mes robotis\u00e9s de stockage, TLS (Theory of Constraints, Lean, Six Sigma) | SDMX (\u00e9changes Eurostat/STATEC) |

| **D\u00e9veloppement & Int\u00e9gration** | **Cloud & MLOps** |
|---|---|
| Python, SQL/PL-SQL, REST APIs, OpenAPI, ETL, Kafka, SDMX, .NET, Java EE | Azure, AWS, Microsoft Power Platform, Git, JIRA, Confluence |

---

## Exp\u00e9rience professionnelle

### Enterprise & AI Architect | Engagements multi-secteurs | Luxembourg
**2014 \u2013 pr\u00e9sent**

*Missions en parall\u00e8le pour des institutions publiques et entreprises luxembourgeoises. S\u00e9lection\u00a0:*

---

> **Proposition de projet \u2013 Intelligent Luxembourg Heritage**
>
> La BnL a num\u00e9ris\u00e9 huit millions d\u2019articles de presse historique luxembourgeoise (1840 \u00e0 nos jours, DE/FR/LB). Ces textes sont accessibles\u00a0; les entit\u00e9s qu\u2019ils contiennent, les personnes, lieux, organisations, \u00e9v\u00e9nements, ne le sont pas. Aucun chercheur ne peut aujourd\u2019hui demander \u00ab\u00a0toutes les mentions de tel personnage entre 1900 et 1914\u00a0\u00bb et obtenir une r\u00e9ponse en quelques secondes.
>
> ILH propose de construire le pipeline qui comble ce gap\u00a0: extraire automatiquement ces entit\u00e9s, les relier au catalogue bibnet.lu et \u00e0 Wikidata, et les rendre interrogeables depuis eluxemburgensia.lu. La preuve de concept a \u00e9t\u00e9 d\u00e9velopp\u00e9e sur les donn\u00e9es ouvertes CC0 de data.bnl.lu et valid\u00e9e sur les m\u00eames images de r\u00e9f\u00e9rence que la baseline officielle Nautilus-OCR.

---

**Intelligent Luxembourg Heritage, BnL (2025 \u2013 en cours)**

*Pour tous\u00a0:* La presse historique luxembourgeoise contient huit millions d\u2019articles en allemand, fran\u00e7ais et luxembourgeois. Ces textes sont num\u00e9ris\u00e9s, mais pas enrichis\u00a0: les noms de personnes, de lieux, d\u2019organisations sont dans le texte, mais pas interrogeables. ILH construit le pipeline qui les extrait, les relie au catalogue bibnet.lu et \u00e0 Wikidata, et les rend accessibles depuis eluxemburgensia.lu. Un chercheur peut demander toutes les mentions d\u2019un personnage ou d\u2019un lieu sur cent ans de presse, et obtenir une r\u00e9ponse en quelques secondes.

*Technique\u00a0:* POC zero-shot sur les donn\u00e9es officielles BnL (CC0)\u00a0: CER 2,72\u00a0% vs Nautilus/Kraken 3,68\u00a0% publi\u00e9, sans fine-tuning. Pipeline\u00a0: METS/ALTO \u2192 VLM (Qwen3.5-397B-A17B) \u2192 post-correction OCR + NER (PER, LOC, ORG, DATE) + bbox_2d \u2192 entity linking Wikidata/ARK (NAAN\u00a070795) \u2192 knowledge graph bibnet.lu\u00a0; Phase\u00a01-2\u00a0: 800\u00a0000 pages, presse historique DE/FR/LB\u00a0; Phase\u00a03+\u00a0: robot feuilleteur \u2192 frames vid\u00e9o \u2192 VLM (OT\u2192IT). Pilot\u00e9 sous QUAPITAL-HERMES compos\u00e9 avec CRISP-ML(Q). EU AI Act int\u00e9gr\u00e9 d\u00e8s la conception\u00a0: Art.\u00a050, model card, AIPD. Partenariats engag\u00e9s\u00a0: Uni.lu, C\u00b2DH, Impresso Phase\u00a02.  
Soumission HIPE-OCRepair 2026 pr\u00eate (6\u20138\u00a0avril)\u00a0: le GT BnL CC0 (6\u00a0723 blocs, presse LU DE/FR/LB) comble le gap LB absent du benchmark ICDAR\u00a0; premi\u00e8re comparaison VLM vs BERT sur presse luxembourgeoise.  
\u2192 [github.com/hdjebar/IntelligentLuxembourgHeritage](https://github.com/hdjebar/IntelligentLuxembourgHeritage)

**Plateforme RAG multimodale, institution financi\u00e8re (2024\u20132025, 14 mois)**  
Co-construit avec les \u00e9quipes m\u00e9tier et IT une plateforme de recherche s\u00e9mantique sur des d\u00e9p\u00f4ts h\u00e9t\u00e9rog\u00e8nes (documents, images, donn\u00e9es structur\u00e9es). Pipeline\u00a0: ingestion multimodale \u2192 post-correction OCR \u2192 embeddings \u2192 cha\u00eene LangChain avec attribution des sources \u2192 enrichissement NER. Ce qui prenait des heures de navigation manuelle entre silos se r\u00e9sout d\u00e9sormais en quelques secondes.

**Plateforme d\u2019aide \u00e0 la d\u00e9cision architecturale, groupe d\u2019assurance (2023\u20132024, 8 mois)**  
B\u00e2ti, aux c\u00f4t\u00e9s d\u2019une \u00e9quipe d\u2019architectes enterprise, une plateforme GraphRAG couplant LangChain, bases vectorielles et standards ArchiMate. Les architectes interrogent en langage naturel des volumes importants de documentation technique et institutionnelle qui restaient jusqu\u2019alors dans des silos inaccessibles en temps r\u00e9el.

**Syst\u00e8me d\u2019analyse pr\u00e9dictive en sant\u00e9, Agence de la Biom\u00e9decine, France (2022\u20132023)**  
D\u00e9velopp\u00e9, aux c\u00f4t\u00e9s des \u00e9quipes m\u00e9dicales, des algorithmes de scoring ML pour l\u2019allocation de greffons h\u00e9patiques. De la pr\u00e9paration des donn\u00e9es \u00e0 la validation clinique\u00a0: un cycle complet, avec les cliniciens \u00e0 chaque \u00e9tape.

**D\u00e9veloppement de skills Claude AI (2024\u20132025)**  
*ai-methodologies*\u00a0: CRISP-DM, CRISP-ML(Q), LLMOps, EU AI Act. *enterprise-architecture*\u00a0: 50+ frameworks (ArchiMate, BPMN, TOGAF, s\u00e9curit\u00e9, MLOps). *eu-ai-act-compliance*\u00a0: classification des risques, obligations GPAI, conformit\u00e9 Art.\u00a09-15.

---

### Enterprise Architect | Soci\u00e9t\u00e9 G\u00e9n\u00e9rale Luxembourg | Luxembourg
**Juillet 2023 \u2013 Mars 2024**

*Architecture sur quatre juridictions\u00a0: Luxembourg, Paris, Suisse, Monaco.*

- Co-construit avec les parties prenantes r\u00e9glementaires une strat\u00e9gie cloud conforme aux exigences CSSF\u00a0: gouvernance, vocabulaire r\u00e9glementaire, alignement multi-entit\u00e9s.
- D\u00e9ploy\u00e9, avec les \u00e9quipes IT, des standards enterprise pour le management des API, le monitoring et la s\u00e9curit\u00e9.
- Traduit des d\u00e9cisions architecturales en programmes de changement que les \u00e9quipes ont r\u00e9ellement adopt\u00e9s, dans un contexte multi-juridictions \u00e0 forte complexit\u00e9 organisationnelle.

---

### Programme Data Science avanc\u00e9e | Paris Mines Tech | Paris
**Novembre 2022 \u2013 Mars 2023**

Programme ex\u00e9cutif intensif\u00a0: machine learning avanc\u00e9, deep learning, big data, IA en sant\u00e9 num\u00e9rique. Livr\u00e9 un syst\u00e8me speech-to-text ML de bout en bout\u00a0; particip\u00e9 \u00e0 des hackathons sant\u00e9 impliquant fine-tuning et \u00e9valuation sur donn\u00e9es contraintes.

---

### Enterprise Architect | KPMG Luxembourg | Luxembourg
**D\u00e9cembre 2021 \u2013 Octobre 2022**

Co-construit avec la direction la pratique EA interne\u00a0; automatis\u00e9 les op\u00e9rations de donn\u00e9es ServiceNow via PowerShell\u00a0; co-d\u00e9fini les frameworks de gouvernance Microsoft Power Platform\u00a0; architectur\u00e9 les capacit\u00e9s d\u2019analytics cloud pour une BI quasi-temps r\u00e9el.

---

### Enterprise/Solution Architect & Business Analyst | Luxembourg Conseil | Luxembourg
**Mars 2015 \u2013 Novembre 2021**

*Missions multi-secteurs\u00a0: gouvernement, pharma, services financiers, emploi.*

- **Agence de paiement wallonne\u00a0:** reconfigur\u00e9 l\u2019architecture enterprise de bout en bout avec les \u00e9quipes m\u00e9tier\u00a0: d\u00e9lais de traitement r\u00e9duits de semaines \u00e0 jours\u00a0; r\u00e9f\u00e9rentiel EA dans ArchiMate/Sparx EA\u00a0; reporting batch remplac\u00e9 par une BI temps r\u00e9el.
- Pilot\u00e9 des projets pluridisciplinaires sur BPM, gouvernance des donn\u00e9es, migration cloud et IAM\u00a0; chacun coordonn\u00e9 avec les sp\u00e9cialistes de domaine et livr\u00e9 dans le p\u00e9rim\u00e8tre, le planning et le budget convenus.

---

### Enterprise BPM Architect | STATEC | Luxembourg
**Octobre 2014 \u2013 F\u00e9vrier 2015**

B\u00e2ti, avec les \u00e9quipes internes, la d\u00e9marche Architecture d\u2019Entreprise et BPM align\u00e9e sur les standards statistiques europ\u00e9ens (ESS, GSBPM, GAMSO, CEAF). \u00c9changes avec Eurostat via SDMX, format directement pertinent pour les travaux BnL autour de METS/ALTO et OAI-PMH.

---

### Enterprise Consultant | COPROCESS SA | Luxembourg
**Janvier 2012 \u2013 Septembre 2014**

Audits IT, transformation enterprise, optimisation processus sant\u00e9 (approche TLS)\u00a0; analyse et restructuration de flux physiques\u00a0: logistique de distribution, gestion de magasinage, automatisation d\u2019entrep\u00f4t. Co-fond\u00e9 LuxBA et LuxEA, les deux communaut\u00e9s de pratique luxembourgeoises en analyse m\u00e9tier et architecture d\u2019entreprise.

---

### IT Business Analyst, IT PM & BPM Specialist | Commission europ\u00e9enne | Bruxelles/Luxembourg
**Juin 2007 \u2013 D\u00e9cembre 2011**

Co-d\u00e9velopp\u00e9 le programme d\u2019architecture enterprise et la m\u00e9thodologie BPM\u00a0; re-engin\u00e9er\u00e9, avec les \u00e9quipes eGreffe, les syst\u00e8mes documentaires pour la conformit\u00e9 au Trait\u00e9 de Lisbonne\u00a0; reconfigur\u00e9, avec DG Traduction, les workflows de services linguistiques\u00a0; pilot\u00e9 la livraison IT des syst\u00e8mes financiers et d\u2019identit\u00e9 pour l\u2019\u00e9largissement europ\u00e9en.

---

### ERP Systems Architect & IT PMO Leader | Parlement europ\u00e9en | Luxembourg/Bruxelles
**Septembre 2002 \u2013 D\u00e9cembre 2006**

Con\u00e7u et mis en \u0153uvre, avec les \u00e9quipes RH, les syst\u00e8mes de gestion du personnel sur la suite Oracle ERP\u00a0; co-construit avec la direction le PMO IT du Parlement\u00a0: standards de gouvernance, m\u00e9thodologies, livraison pr\u00e9visible.

---

### Ing\u00e9nieur R&D | IST Luxembourg | Luxembourg
**2000 \u2013 2002**

Co-d\u00e9velopp\u00e9 la m\u00e9thodologie Model-Driven Architecture pour les syst\u00e8mes distribu\u00e9s dans le cadre du projet europ\u00e9en FIDJI.

---

### Consultant technologie | Lagard\u00e8re / Linagora | Paris
**2000**

\u00c9tudes de faisabilit\u00e9 et architecture technique pour l\u2019adoption web enterprise\u00a0; gestion de plateformes Linux open source.

---

### Coordinateur de formation & Enseignant | Diverses organisations | France
**1994 \u2013 2000**

Enseign\u00e9 les math\u00e9matiques appliqu\u00e9es, statistiques, algorithmique et informatique \u00e0 l\u2019universit\u00e9 pendant six ans. Rendre accessibles des concepts abstraits \u00e0 des publics qui n\u2019avaient pas choisi de les trouver int\u00e9ressants est, r\u00e9trospectivement, une formation assez utile pour un architecte enterprise.

---

## Formation

**Certification Cloud & Outsourcing Officer** | House of Training & ABBL | Juin 2025  
**Certification Programme Data Science & ML** | Paris Mines Tech | Novembre 2022 \u2013 Mars 2023  
**Master en Technologies de l\u2019Information et de la Communication** | INPL, Nancy | 1999 \u2013 2000  
**Pr\u00e9paration doctorat en Math\u00e9matiques appliqu\u00e9es** | Universit\u00e9 Nancy / INRIA | 1994 \u2013 1996  
*Comportement asymptotique des \u00e9quations aux d\u00e9riv\u00e9es partielles*  
**Master en Math\u00e9matiques appliqu\u00e9es (MIM)** | Universit\u00e9 de Metz | 1993 \u2013 1994  
**Formations professionnelles\u00a0:** PMI-CPMAI | Professional Scrum Master | PMP | TOGAF | PRINCE2 | ITIL | IIBA/BABOK

---

## Reconnaissance & engagement

Expert contributeur\u00a0: \u00ab The Leader\u2019s Guide to Radical Management \u00bb (Stephen Denning).  
Co-fondateur, Luxembourg Business Analysis (LuxBA) et Enterprise Architecture (LuxEA) Communities of Practice.  
Membre actif, PMI Luxembourg Chapter et Agile Luxembourg Community.

---

## Langues

**Fran\u00e7ais\u00a0:** natif (C2) | **Anglais\u00a0:** professionnel avanc\u00e9 (C1)  
Dispense des langues administratives allemand et luxembourgeois, \u00e9ligibilit\u00e9 confirm\u00e9e (groupe A1).  
*L\u2019usage de l\u2019anglais dans les exp\u00e9riences et publications internationales est conforme aux pratiques du secteur GLAM (AI4LAM, LIBER, ICDAR, Impresso) et des institutions scientifiques luxembourgeoises.*
