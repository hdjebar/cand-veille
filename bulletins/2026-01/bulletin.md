# Bulletin de veille technologique — Janvier 2026
## BnL · Responsable projets IA et Data · Réf. E00040484

**Auteur :** Djebar Hammouche  
**Périmètre :** IA appliquée au patrimoine numérisé · Infrastructure souveraine · Réglementation EU AI Act  
**Date de production :** 17 mars 2026 (couverture : janvier 2026)

---

## Synthèse du mois

Janvier 2026 s'inscrit dans la continuité de la dynamique de fin 2025 : la BnL vient de rejoindre AI4LAM (décembre 2025), MeluXina-AI annonce son opérationnalité pour le second semestre 2026, et la fenêtre réglementaire EU AI Act pour les systèmes à haut risque approche (août 2026). Sur le plan technique, Qwen3-Max-Thinking est sorti le 27 janvier 2026 — signal précoce d'une accélération du cycle Qwen qui aboutira à Qwen3.5 dès le 16 février. Le mois de janvier est donc un mois charnière : infrastructure nationale qui monte en puissance, communauté internationale qui s'organise, réglementation qui se précise.

**3 signaux à suivre en priorité :**
1. **MeluXina-AI** : accès possible via l'AI Factory dès mi-2026 — fenêtre de demande d'accès à anticiper maintenant
2. **EU AI Act** : 2 août 2026 = application complète des obligations high-risk. Les systèmes chatbot BnL (Art. 50 risque limité) doivent avoir leur conformité documentée
3. **HIPE-OCRepair 2026** (signal de mars 2026, mais deadline fin mars 2026) : la BnL doit confirmer sa participation comme dataset provider avant fin mars

---

## Axe 1 — IA et patrimoine numérisé (OCR · NER · VLM)

### Signal 1.1 · Qwen3-Max-Thinking — 27 janvier 2026
**Source :** Alibaba Cloud · Wikipedia Qwen timeline  
**Scoring BnL :** ★★★★☆ Haute pertinence

Le 27 janvier 2026, Alibaba publie Qwen3-Max-Thinking, version enrichie du modèle Qwen3-Max avec mode de raisonnement étendu (thinking mode). Capable de générer du texte, des images et de la vidéo. Ce n'est pas encore le modèle multimodal natif optimal pour l'OCR, mais c'est le signal que le cycle Qwen s'accélère fortement — Qwen3.5-397B-A17B suivra le 16 février 2026, soit 3 semaines plus tard, avec des capacités multimodales nativement intégrées (fusion précoce texte+image+vidéo).

**Pertinence BnL :** Signal de veille sur la cadence de release. Le POC ILH a été conduit sur Qwen3.5-397B-A17B (sorti 16 fév. 2026), modèle disponible sur OpenRouter à très faible coût. Qwen3.5-35B-A3B est le candidat naturel pour le fine-tuning sur MeluXina-AI (VRAM : ~70-82 Go = 1 nœud H100, coût ~50-200 € par run QLoRA).

**Action :** Surveiller la sortie de Qwen3.5 (effectivement sorti le 16 fév. 2026) pour mise à jour du tableau de comparaison des modèles dans le dashboard.

---

### Signal 1.2 · Qwen3-VL famille complète — déploiement continu déc. 2025–janv. 2026
**Source :** GitHub QwenLM/Qwen3-VL · Alibaba Cloud Model Studio  
**Scoring BnL :** ★★★★★ Critique

La famille Qwen3-VL se complète entre septembre et décembre 2025 : flagship 235B-A22B (sept.), 30B-A3B (oct.), 4B/8B/2B/32B (oct.–nov.). En janvier 2026, le snapshot `qwen3-vl-flash-2026-01-22` est disponible sur Alibaba Cloud Model Studio avec mode thinking intégré et performances améliorées sur la reconnaissance visuelle. Cette famille constitue la baseline VLM de référence pour l'OCR historique avant que Qwen3.5 ne la dépasse.

**Pertinence BnL :** Qwen3-VL-235B-A22B est le modèle qui précède Qwen3.5. Pour le pipeline BnL :
- Inférence production : Qwen3-VL-8B ou 32B sur CTIE (dense, déploiement simple avec vLLM)
- Fine-tuning intensif : Qwen3.5-35B-A3B sur MeluXina-AI (MoE, meilleur rapport VRAM/performance)
- La transition Qwen3-VL → Qwen3.5 est transparente : même API, même paradigme d'instruction tuning

**Action :** Benchmarker Qwen3-VL-8B sur les 19 blocs CC0 BnL pour établir la courbe VRAM/CER avant de décider du modèle de production CTIE.

---

### Signal 1.3 · PaddleOCR-VL 7B — leader OmniDocBench (score 92,86)
**Source :** CodeSOTA OCR Benchmarks · mars 2026  
**Scoring BnL :** ★★★☆☆ Moyen

PaddleOCR-VL 7B (Baidu, Apache 2.0) prend la tête de l'OmniDocBench avec 92,86 de score composite, dépassant GPT-4o (85,80) sur l'analyse de documents incluant tableaux et formules. Coût auto-hébergé : 167× moins cher que les APIs vendeurs à précision supérieure.

**Pertinence BnL :** Alternative compétitive à Qwen3.5 pour les cas d'usage purement OCR sans NER. Sur Fraktur historique, Qwen3.5 reste probablement supérieur (multilingue natif, 201 langues), mais PaddleOCR-VL mérite un benchmark comparatif dans le cadre de G0.

**Action :** Intégrer PaddleOCR-VL comme baseline alternative dans le protocole benchmark G0 du projet ILH.

---

### Signal 1.4 · HIPE-OCRepair 2026 — deadline dataset provider fin mars 2026
**Source :** hipe-eval.github.io/HIPE-OCRepair-2026/  
**Scoring BnL :** ★★★★★ URGENT

Compétition internationale ICDAR 2026 (31 août–4 sept. 2026) dédiée à la correction post-OCR de documents historiques par LLM. Des équipes du monde entier s'affrontent pour améliorer l'OCR de collections patrimoniales réelles. Les modèles vainqueurs sont publiés en open source, déployables en souveraineté sur MeluXina-AI puis en production CTIE.

Le ground truth NautilusOCR publié sur data.bnl.lu (6 723 blocs, CC0, presse LU 1840–1960, DE/FR/LB) correspond exactement au format dataset provider attendu.

**Pertinence BnL :** Démarche de mutualisation internationale dans l'esprit de data.bnl.lu. En soumettant ce dataset, la BnL obtient des modèles entraînés et benchmarkés sur ses propres données sans investissement de développement. Participation confirmée avant fin mars 2026.

**Action :** Contacter Yves Maurer (yves.maurer@bnl.etat.lu) et l'équipe HIPE-OCRepair avant le 31 mars 2026. [Message LinkedIn rédigé — voir dossier candidature.]

---

## Axe 2 — Infrastructure souveraine Luxembourg

### Signal 2.1 · MeluXina-AI — opérationnalité annoncée S2 2026
**Source :** Ingsci.lu · 20more.lu · SiliconLuxembourg · LuxProvide  
**Scoring BnL :** ★★★★★ Critique pour la roadmap

MeluXina-AI, le supercalculateur optimisé pour l'IA du Luxembourg (€112M, 2 100+ GPU-AI, multi-exaflop), sera opérationnel entre avril et octobre 2026. Hébergé chez LuxConnect (Bissen/Bettembourg), opéré par LuxProvide, intégré au réseau EuroHPC. 50% de la capacité réservée à l'usage national luxembourgeois.

**Chiffres clés :**
- 2 100+ GPU-AI accélérateurs (A100/H100)
- Opérationnel : S2 2026 (fenêtre avril–octobre)
- Accès PME via Luxinnovation (point d'entrée unique)
- HPC-AI BRIDGES : 9 projets financés le 5 fév. 2026 pour €11,6M total
- Prochain appel HPC-AI BRIDGES : 1er mars 2026

**Pertinence BnL :** MeluXina-AI est l'infrastructure cible pour le fine-tuning QLoRA de Qwen3.5 et la distillation 35B→7B du projet ILH. La BnL doit anticiper la demande d'accès via Luxinnovation maintenant — le calendrier de l'appel HPC-AI BRIDGES (appel ouvert 1er mars 2026) est une opportunité directe.

**Action :** Initier le contact avec Luxinnovation pour la demande d'accès MeluXina-AI. Préparer le dossier de projet ILH en format compatible HPC-AI BRIDGES.

---

### Signal 2.2 · Plan national d'inclusion numérique 2026–2030
**Source :** Conseil de gouvernement luxembourgeois · 16 janvier 2026  
**Scoring BnL :** ★★★☆☆ Contexte stratégique

Le gouvernement luxembourgeois a adopté le 16 janvier 2026 le Plan d'action national d'inclusion numérique 2026–2030, prévoyant près de 250 initiatives pour favoriser l'accès aux technologies numériques. Elaboré en concertation avec toutes les parties concernées.

**Pertinence BnL :** Positionnement de la BnL comme acteur clé de l'inclusion numérique via l'accès au patrimoine (eluxemburgensia.lu, data.bnl.lu). Les données ouvertes CC0 de la BnL s'inscrivent directement dans ce plan. La communication BnL peut s'aligner sur ce cadre pour la valorisation des projets IA.

**Action :** Aligner la communication des projets ILH et chatbot sur le vocabulaire du plan d'inclusion numérique 2026–2030.

---

### Signal 2.3 · LuxVLD — modèles IA pour le luxembourgeois (Microsoft × Uni.lu)
**Source :** 20more.lu · 12 février 2026  
**Scoring BnL :** ★★★★☆ Haute pertinence

Annoncé le 12 février 2026, le projet LuxVLD (Luxembourg Vision-Language for Dialects) est une collaboration Microsoft × Université du Luxembourg pour développer des capacités IA dans la langue luxembourgeoise. Pour les acteurs locaux, cela ouvre de nouvelles possibilités pour des interactions IA en luxembourgeois.

**Pertinence BnL :** Convergence directe avec le pipeline NER multilingue du projet ILH (composante LB). Partenariat potentiel avec l'Uni.lu pour les données LB du corpus eluxemburgensia. Le luxembourgeois est explicitement listé dans Qwen3.5 (201 langues) — la BnL dispose d'un corpus unique pour valider ce support.

**Action :** Établir un contact avec l'équipe LuxVLD (Uni.lu) pour explorer une collaboration sur les données LB historiques de la BnL.

---

## Axe 3 — Communauté bibliothèques et patrimoine (GLAM)

### Signal 3.1 · AI4LAM — BnL membre inaugural, Fantastic Futures 2026 Washington
**Source :** BnL Bluesky · AI4LAM/CNI · Décembre 2025 / Annonce 2026  
**Scoring BnL :** ★★★★★ Critique

La BnL a signé le Memorandum of Understanding AI4LAM le 3 décembre 2025 à la British Library (Carlo Blum + Yves Maurer). AI4LAM (Intelligence artificielle pour les bibliothèques, archives et musées) est maintenant une organisation officielle hébergée par la Bibliothèque nationale de Norvège.

Fantastic Futures 2026 se tiendra à Washington DC, 14–18 septembre 2026 — la conférence internationale annuelle de référence sur l'IA dans les GLAM.

**Pertinence BnL :** Membre inaugural = voix dans la gouvernance de la communauté internationale. Fantastic Futures 2026 est l'occasion naturelle de présenter les résultats du projet ILH (POC OCR + NER multilingue + pipeline open source natliblux). Le CER 2,72% vs Nautilus/Kraken 3,68% sans fine-tuning est un résultat publiable.

**Action :** Préparer un abstract pour Fantastic Futures 2026 (deadline à surveiller). Positionner la BnL Luxembourg comme référence sur l'OCR Fraktur et le NER multilingue DE/FR/LB.

---

### Signal 3.2 · Impresso Phase 2 — NER presse historique FR/DE/LB
**Source :** impresso-project.ch · EPFL / Uni. Zurich / C²DH  
**Scoring BnL :** ★★★★★ Partenaire direct

Impresso Phase 2 est le projet européen de référence pour l'analyse sémantique de la presse historique numérisée. Le corpus inclut des données BnL. La méthodologie HIPE (shared task NER/NEL sur presse historique) couvre les langues DE/FR/LB — intersection exacte avec le corpus eluxemburgensia.

Lacune identifiée dans l'état de l'art : aucune étude n'a comparé un VLM fine-tuné contre un BERT fine-tuné sur HIPE. Le benchmark G0 du projet ILH comblerait cette lacune — contribution scientifique originale, publiable LIBER Quarterly ou JDMDH.

**Pertinence BnL :** Partenariat de validation sémantique (porte G2 du projet ILH). Le C²DH (convention BnL–Uni.lu) est le lien institutionnel direct. Les datasets Impresso peuvent servir de benchmark externe indépendant.

**Action :** Planifier une réunion avec Marten Düring (C²DH) pour aligner le protocole de validation G2 sur la méthodologie HIPE.

---

## Axe 4 — Réglementation et gouvernance IA

### Signal 4.1 · EU AI Act — calendrier d'application 2026
**Source :** Commission européenne · EU AI Act tracker  
**Scoring BnL :** ★★★★★ Obligatoire

Calendrier de référence pour la BnL :

| Date | Obligation | Pertinence BnL |
|------|-----------|----------------|
| 2 fév. 2025 | Pratiques interdites + AI literacy | ✅ Appliqué |
| 2 août 2025 | Obligations GPAI (documentation, résumé données entraînement) | ✅ Appliqué pour les modèles nouveaux |
| 2 août 2026 | Application complète règles high-risk + obligations transparence (Art. 50) | ⚠️ Chatbot BnL concerné |
| 2 août 2027 | Systèmes high-risk dans produits réglementés | Non concerné BnL |

**Pertinence BnL :**
- **Chatbot eluxemburgensia.lu** : risque limité (Art. 50) — obligation de transparence applicable août 2026. La mention "généré par l'IA" est déjà en place (bon point).
- **Pipeline NER ILH** : risque minimal — codes de conduite volontaires. Model card + data card suffisent.
- **Modèle Qwen3.5 fine-tuné** : si publié sous Apache 2.0 avec résumé données entraînement → exemption GPAI open source (Art. 53(2)).
- **Données pénales** dans les archives historiques (Art. 10 RGPD) : lot réglementaire distinct requis, AIPD avant montée en charge.

**Action :** Préparer la model card de conformité EU AI Office pour le pipeline ILH. Template disponible : [AI Office GPAI training content summary](https://digital-strategy.ec.europa.eu/en/policies/guidelines-gpai-providers). Initier l'AIPD pour les données pénales historiques.

---

### Signal 4.2 · Digital Package on Simplification — amendements EU AI Act proposés
**Source :** Commission européenne · DIGIBYTE 3 mars 2026  
**Scoring BnL :** ★★★☆☆ À surveiller

La Commission européenne propose d'ajuster le calendrier d'application des règles high-risk en liant leur entrée en vigueur à la disponibilité d'outils de conformité (normes harmonisées CEN-CENELEC). La date butoir reste décembre 2027 au maximum.

**Pertinence BnL :** Allègement potentiel de la charge de conformité pour les déployers (la BnL déploie des systèmes IA, elle ne les met pas sur le marché). Le régime déployer reste moins contraignant que le régime provider. La BnL doit cependant documenter son processus de supervision humaine (Art. 26).

**Action :** Suivre l'avancement du Digital Package. Documenter le processus de supervision humaine (human-in-the-loop) du pipeline NER comme preuve de conformité Art. 26.

---

## Tableau de bord des signaux

| # | Signal | Axe | Score | Urgence | Action |
|---|--------|-----|-------|---------|--------|
| 1.4 | HIPE-OCRepair 2026 | OCR/NER | ★★★★★ | ⚠️ Fin mars | Confirmation BnL dataset provider |
| 2.1 | MeluXina-AI S2 2026 | Infra | ★★★★★ | Anticiper | Demande accès Luxinnovation |
| 3.1 | AI4LAM + Fantastic Futures | GLAM | ★★★★★ | Sept. 2026 | Préparer abstract ILH |
| 4.1 | EU AI Act août 2026 | Règlementation | ★★★★★ | Août 2026 | Model card + AIPD |
| 1.1 | Qwen3-Max-Thinking (27 jan.) | Modèles | ★★★★☆ | Signal | Veille Qwen3.5 (16 fév.) |
| 2.3 | LuxVLD Microsoft × Uni.lu | Infra LB | ★★★★☆ | Court terme | Contact Uni.lu |
| 3.2 | Impresso Phase 2 | GLAM | ★★★★★ | G2 projet | Réunion C²DH |
| 1.2 | Qwen3-VL famille complète | Modèles | ★★★★★ | Benchmark | Tester 8B sur CC0 BnL |
| 1.3 | PaddleOCR-VL 7B | OCR | ★★★☆☆ | Benchmark G0 | Intégrer au protocole G0 |
| 2.2 | Plan inclusion numérique LU | Stratégie | ★★★☆☆ | Communication | Aligner vocabulaire |
| 4.2 | Digital Package Simplification | Règlementation | ★★★☆☆ | À suivre | Documenter supervision humaine |

---

## Sources et références

| Source | Type | Fréquence de suivi |
|--------|------|--------------------|
| github.com/QwenLM/Qwen3.5 | Modèles | Hebdomadaire |
| hipe-eval.github.io/HIPE-OCRepair-2026/ | Compétition | Mensuelle |
| aifactory.lu | Infrastructure LU | Mensuelle |
| bnl.public.lu/fr/bnl/innovation-numerique.html | BnL interne | Mensuelle |
| ai4lam.org | Communauté GLAM | Mensuelle |
| impresso-project.ch | Partenaire | Trimestrielle |
| digital-strategy.ec.europa.eu | Réglementation EU | Mensuelle |
| codesota.com/ocr | Benchmarks VLM | Mensuelle |
| data.bnl.lu | Données BnL CC0 | Trimestrielle |

---

*Bulletin produit dans le cadre de la candidature au poste de Responsable projets IA et Data — BnL réf. E00040484.*  
*Repo principal : [IntelligentLuxembourgHeritage](https://github.com/hdjebar/IntelligentLuxembourgHeritage)*  
*Veille instrumentée avec Claude (Anthropic), ChatGPT (OpenAI), Gemini (Google), recherche académique (arXiv, LIBER Quarterly).*
