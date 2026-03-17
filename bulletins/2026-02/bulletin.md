# Bulletin de veille technologique — Février 2026
## BnL · Responsable projets IA et Data · Réf. E00040484

**Auteur :** Djebar Hammouche  
**Période :** 1–28 février 2026  
**Date de production :** 17 mars 2026

---

## Synthèse du mois

Février 2026 est le mois le plus dense de la période Jan–Mars : Qwen3.5-397B-A17B sort le 16 février et redéfinit la baseline VLM pour les projets patrimoniaux. HIPE-OCRepair 2026 publie ses données d'entraînement le 2 mars (signal qui prend naissance en février). Sur le front luxembourgeois, les résultats de l'appel HPC-AI BRIDGES sont publiés (5 février), ouvrant une porte de financement directe pour le projet ILH. Le Rapport d'activité BnL 2024 confirme le programme de travail 2025-2028 avec 171 projets dont 29 IT et 24 data — cadre stratégique dans lequel s'inscrit le poste.

**Signal majeur du mois :** Qwen3.5-397B-A17B sort le 16 février — le modèle utilisé dans le POC ILH réalisé deux semaines plus tard. C'est la démonstration concrète d'une veille active convertie en expérimentation immédiate.

---

## Axe 1 — IA et patrimoine numérisé

### Signal 1.1 · Qwen3.5-397B-A17B — 16 février 2026 ★ Signal majeur
**Source :** github.com/QwenLM/Qwen3.5 · qwen.ai/blog  
**Scoring BnL :** ★★★★★ Critique

Alicloud publie Qwen3.5 le 16 février 2026 — le modèle flagship de la nouvelle génération native multimodale. Architecture hybride Gated DeltaNet + sparse MoE (397B total, 17B actifs). Fusion précoce texte + image + vidéo : pas d'adaptateur, les modalités sont intégrées dès l'entraînement sur des trillions de tokens multimodaux. 201 langues, luxembourgeois explicitement listé. Apache 2.0. Contexte natif 262K tokens (extensible à 1M).

**Ce que Qwen3.5 apporte vs Qwen3-VL :**
- Architecture **fusion précoce** vs adaptateurs Qwen3-VL : meilleure cohérence image-texte sur documents historiques dégradés
- **Scaled RL** sur environnements multi-agents : raisonnement amélioré sur documents complexes (Fraktur, code-switching)
- **Gated DeltaNet** : débit supérieur à VRAM équivalent — avantage pour l'inférence CTIE en production
- Selon les benchmarks Alibaba : dépasse Qwen3-VL sur raisonnement, coding, agents et compréhension visuelle

**Pertinence BnL :** C'est le modèle utilisé dans le POC ILH (via OpenRouter, 14 mars 2026). CER 2,72% vs Nautilus/Kraken 3,68% obtenu avec ce modèle en zero-shot. Pour la roadmap :
- **POC 2** : Qwen3.5-35B-A3B (VRAM ~70-82 Go = 1 nœud H100) sur MeluXina-AI
- **Inférence CTIE** : Qwen3.5-27B dense (déploiement simple, pas de routing MoE)
- **Edge/mobile** : Qwen3.5-9B (sortie 2 mars) sur laptop GPU pour tests rapides

**Action :** Le POC ILH a validé ce modèle sur données CC0 BnL. Préparer le protocole de benchmark G0 sur Qwen3.5-35B-A3B pour MeluXina-AI.

---

### Signal 1.2 · olmOCR-2 (Allen AI) — GRPO en production
**Source :** allenai.org/blog/olmocr-2 · arxiv.org/abs/2502.18443  
**Scoring BnL :** ★★★★☆ Haute pertinence

olmOCR-2 7B (Allen AI, Apache 2.0) applique le reinforcement learning avec récompenses vérifiables (GRPO) à l'OCR de documents. Fine-tuné sur Qwen2.5-VL-7B avec 270 000 pages PDF diverses incluant des scans historiques. Score 82,4±1,1 sur olmOCR-Bench. Traite 3 400 tokens/seconde sur un H100. Coût : moins de 200 USD par million de pages. Modèle disponible sur Hugging Face (Apache 2.0).

**Méthode clé :** Au lieu d'optimiser une métrique générique, olmOCR-2 utilise des **tests unitaires déterministes** comme signal de récompense GRPO — le modèle apprend à passer des tests spécifiques (préservation de structure de tableau, ordre de lecture, formules LaTeX). Approche reproductible et auditable.

**Pertinence BnL :**
- Valide la Roadmap ILH Étape 3b (GRPO) : cette approche est maintenant prouvée en production
- olmOCR-2 traite des scans historiques dégradés (inclus dans les données d'entraînement)
- La méthodologie test-unitaire est directement adaptable pour le benchmark G0 BnL (CER, F1 NER, alignement ALTO)
- **Limite** : entraîné principalement en anglais — le Fraktur luxembourgeois reste un angle mort à couvrir par fine-tuning

**Action :** Ajouter olmOCR-2 comme baseline comparative dans le protocole G0. Tester sur les 19 blocs CC0 BnL pour comparaison directe avec Qwen3.5 zero-shot.

---

### Signal 1.3 · Rapport BnL 2024 — Programme de travail 2025-2028 publié
**Source :** gouvernement.lu · PDF Rapport annuel 2024 BnL  
**Scoring BnL :** ★★★★★ Contexte stratégique direct

Le Rapport d'activité BnL 2024 confirme l'élaboration d'un programme de travail 2025-2028 de 171 projets, dont 29 projets IT, 24 projets data, 30 nouvelles solutions. Transition stratégique : passage d'une approche centrée sur les collections à une **approche orientée vers l'utilisateur**. Mention explicite de l'automatisation, de la numérisation et de la robotisation comme composantes du quotidien institutionnel.

Sur l'IA : le rapport liste l'automatisation du catalogage de documents électroniques comme projet en cours, ainsi que l'approfondissement de l'usage des VLM pour la valorisation patrimoniale.

**Pertinence BnL :** Ce cadre confirme exactement le mandat du poste Responsable projets IA et Data : le programme 2025-2028 est la feuille de route que le titulaire du poste sera chargé d'exécuter. Le projet ILH s'inscrit dans les 24 projets data et les 29 projets IT annoncés.

**Action :** Aligner la présentation du projet ILH sur les axes du programme 2025-2028. Formuler la roadmap ILH comme contribution directe à la transition "collections → utilisateurs".

---

## Axe 2 — Infrastructure et financement Luxembourg

### Signal 2.1 · HPC-AI BRIDGES — 9 projets financés, €11,6M (5 février 2026)
**Source :** 20more.lu · aifactory.lu  
**Scoring BnL :** ★★★★★ Opportunité de financement directe

Le 5 février 2026, le gouvernement luxembourgeois publie les résultats du premier appel HPC-AI BRIDGES (FNR + Ministère de l'Économie + Luxinnovation) : 9 projets financés pour €11,6M au total. Un second appel ouvre le 1er mars 2026.

**Structure du programme :**
- Financement conjoint FNR + Ministry of Economy pour des projets IA/data/quantique utilisant l'infrastructure nationale
- Accès prioritaire à MeluXina-AI pour les projets sélectionnés
- Support technique LuxProvide inclus (optimisation code, parallélisation GPU)

**Pertinence BnL :** Le projet ILH (fine-tuning QLoRA Qwen3.5 + distillation sur corpus BnL) correspond exactement au profil HPC-AI BRIDGES : institution publique + données CC0 + MeluXina-AI + partenariat Uni.lu. L'appel du 1er mars 2026 est la fenêtre immédiate.

**Action :** Préparer le dossier de candidature HPC-AI BRIDGES pour l'appel mars 2026. Structurer le projet autour des 3 composantes requises : accès compute (MeluXina-AI), expertise technique (LuxProvide), partenariat académique (Uni.lu/C²DH).

---

### Signal 2.2 · LuxVLD — Microsoft × Uni.lu pour le luxembourgeois (12 février 2026)
**Source :** 20more.lu  
**Scoring BnL :** ★★★★☆ Partenariat potentiel LB

Annoncé le 12 février 2026, le projet LuxVLD (Luxembourg Vision-Language for Dialects) est une collaboration Microsoft × Université du Luxembourg pour développer des capacités IA dédiées au luxembourgeois. Objectif : permettre des interactions IA en langue luxembourgeoise dans des applications professionnelles.

**Pertinence BnL :** La BnL détient le plus grand corpus LB historique numérisé (eluxemburgensia.lu, journaux 1840-1960). Ce corpus est unique pour valider et enrichir les capacités LB des modèles LuxVLD. Convergence directe avec le pipeline NER multilingue FR/DE/LB du projet ILH. Convention BnL–Uni.lu existante = base institutionnelle pour une collaboration.

**Action :** Contacter l'équipe LuxVLD à l'Uni.lu (via C²DH ou LCSB) pour explorer une contribution du corpus BnL CC0 au projet LuxVLD.

---

## Axe 3 — Réglementation

### Signal 3.1 · REMI Initiative — responsabilité IA, Esch-Belval 17 mars 2026
**Source :** aifactory.lu  
**Scoring BnL :** ★★★☆☆ Contexte réglementaire

La Plenary Session REMI (Regulation Meets Innovation) se tient le 17 mars 2026 à Esch-Belval, organisée par la Luxembourg AI Factory. Thème : rendre l'adoption responsable de l'IA concrète pour l'écosystème luxembourgeois.

**Pertinence BnL :** La BnL doit documenter sa conformité EU AI Act avant août 2026 (Art. 50, risque limité pour le chatbot). REMI est l'occasion d'identifier les interlocuteurs luxembourgeois en gouvernance IA et de valider l'approche conformité du pipeline ILH.

**Action :** Participer ou suivre les compte-rendus de REMI pour cartographier l'écosystème de conformité IA au Luxembourg.

---

## Tableau de bord — Signaux février 2026

| # | Signal | Score | Urgence | Action |
|---|--------|-------|---------|--------|
| 1.1 | Qwen3.5-397B-A17B (16 fév.) | ★★★★★ | Immédiat | POC ILH réalisé |
| 2.1 | HPC-AI BRIDGES appel mars | ★★★★★ | 1er mars | Dossier candidature |
| 1.3 | Rapport BnL 2024 / prog. 2025-2028 | ★★★★★ | Contexte | Aligner présentation ILH |
| 1.2 | olmOCR-2 GRPO | ★★★★☆ | Benchmark G0 | Tester sur CC0 BnL |
| 2.2 | LuxVLD Microsoft × Uni.lu | ★★★★☆ | Court terme | Contact Uni.lu |
| 3.1 | REMI Initiative 17 mars | ★★★☆☆ | 17 mars | Suivi compte-rendus |

---

*Bulletin produit dans le cadre de la candidature BnL réf. E00040484.*
