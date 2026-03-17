# Bulletin de veille technologique — Mars 2026 (1–17 mars)
## BnL · Responsable projets IA et Data · Réf. E00040484

**Auteur :** Djebar Hammouche  
**Période :** 1–17 mars 2026 (bulletin partiel — mi-mois)  
**Date de production :** 17 mars 2026

---

## Synthèse du mois

Mars 2026 est le mois d'exécution : HIPE-OCRepair publie ses données d'entraînement (2 mars) et ouvre son leaderboard HuggingFace (23 mars). Qwen3.5 complète sa famille avec les small models (2 mars). Le POC ILH est réalisé et mesuré (14 mars). Le REMI Initiative se tient le 17 mars. Et la deadline de candidature BnL (27 mars) approche.

**Signal majeur du mois :** Le POC ILH est terminé — CER 2,72% vs Nautilus/Kraken 3,68% sans fine-tuning, sur les mêmes images officielles. La porte 1 de la roadmap est franchie.

**Signal de clôture (17 mars) :** Autoresearch (Karpathy) — boucle d'optimisation LLM autonome applicable directement à la distillation Phase 2/3 d'ILH (Qwen3.5-397B → Lux-Heritage-7B sur MeluXina-AI).

---

## Axe 1 — IA et patrimoine numérisé

### Signal 1.1 · Qwen3.5 Small Series — 2 mars 2026
**Source :** github.com/QwenLM/Qwen3.5 · marktechpost.com  
**Scoring BnL :** ★★★★☆ Haute pertinence

Le 2 mars 2026, Alibaba complète la famille Qwen3.5 avec quatre modèles compacts : 9B, 4B, 2B, 0.8B. Tous nativement multimodaux (texte + image + vidéo), Apache 2.0, 201 langues. Architecture dense (plus simple à déployer que MoE). Le Qwen3.5-9B surpasse sur MMMU-Pro (70,1) des modèles 3× plus grands comme Gemini 2.5 Flash-Lite (59,7). Le 4B tient sur laptop (12 Go VRAM). Le 2B tourne sur iPhone 17 Pro en mode avion.

**Pertinence BnL :**
- **Qwen3.5-9B** : candidat optimal pour l'inférence CTIE en production (serveurs GPU CTIE AI4Gov). Dense, déploiement vLLM standard, VRAM compatible.
- **Qwen3.5-4B** : prototype local sur workstation dev (RTX 3090/A6000 24 Go) — itérations rapides sans MeluXina-AI
- **Distillation** : roadmap ILH Phase 2 prévoit 35B→7B. La série 4B/9B dense confirme la faisabilité de distillation vers ces tailles.

**Action :** Tester Qwen3.5-9B sur les 19 blocs CC0 BnL pour établir la courbe CER vs taille de modèle avant G0.

---

### Signal 1.2 · HIPE-OCRepair 2026 — données d'entraînement disponibles (2 mars)
**Source :** hipe-eval.github.io/HIPE-OCRepair-2026/ · mail-archive.com/corpora-list  
**Scoring BnL :** ★★★★★ URGENT — Action avant 23 mars

Calendrier HIPE-OCRepair 2026 vérifié et mis à jour :

| Date | Événement |
|------|-----------|
| 10 déc. 2025 | Sample data release |
| **2 mars 2026** | **Training + dev data release + scorer** |
| **23 mars 2026** | **HuggingFace leaderboard release** |
| 6–8 avr. 2026 | Evaluation phase (test release + soumission) |
| 10 avr. 2026 | Publication des résultats |
| 31 août–4 sept. 2026 | Présentation ICDAR 2026 (Vienne) |

Le benchmark couvre anglais, français et allemand, matériaux historiques 17e–20e siècle, journaux et imprimés. Les données d'entraînement (2 mars) sont déjà disponibles sur HuggingFace.

**Pertinence BnL :** Le ground truth NautilusOCR BnL (CC0, 6 723 blocs, presse LU 1840–1960, DE/FR/LB) complète les langues couvertes (FR/DE déjà présents). La BnL pourrait contribuer le LB et les données luxembourgeoises manquantes au benchmark — contribution scientifique ET visibilité internationale.

**Action :**
1. Télécharger les données d'entraînement disponibles depuis le 2 mars
2. Contacter les organisateurs pour confirmer les modalités de contribution dataset LB
3. Surveiller le leaderboard HuggingFace qui ouvre le 23 mars

---

### Signal 1.3 · POC ILH — résultats mesurés (14 mars 2026) ★ Réalisé
**Source :** github.com/hdjebar/IntelligentLuxembourgHeritage  
**Scoring BnL :** ★★★★★ — Porte 1 franchie

Le POC ILH (Intelligent Luxembourg Heritage) est réalisé et mesuré le 14 mars 2026 sur données CC0 BnL.

**Résultats (CER — Character Error Rate) :**

| Système | CER | Jeu de test |
|---------|-----|-------------|
| Tesseract 5 (baseline) | 5,13% | 19 blocs CC0 BnL |
| Nautilus/Kraken publié | 3,68% | 6 723 blocs (Schneider 2023) |
| **Qwen3.5 zero-shot (POC)** | **3,37%** | **19 blocs CC0 BnL** |
| **Qwen3.5 zero-shot Section 9** | **2,72%** | **6 blocs officiels Nautilus** |

CER 2,72% vs Nautilus/Kraken 3,68% **sans fine-tuning**, sur les mêmes images officielles de référence. Réduction de 34% vs Tesseract. Fraktur : amélioration systématique (3/3 blocs, dont img5 : 25,19% → 2,04%). Coût session complète : 2,01$ via OpenRouter.

---

### Signal 1.4 · Autoresearch (Karpathy) — boucle LLM autonome applicable à ILH Phase 2/3 (17 mars 2026) ★★ Nouveau
**Source :** marktechpost.com (12 mars 2026) · lukesalamone.github.io · arxiv.org/html/2505.13111  
**Scoring BnL :** ★★★★☆ Haute pertinence — distillation Phase 2/3

Le framework **autoresearch** (Andrej Karpathy, publié 12 mars 2026) est une boucle LLM autonome sur GPU unique : l'agent modifie `train.py`, lance un entraînement limité en temps (5 min), mesure la métrique de validation, garde ou annule. Optimise sans supervision humaine. Un benchmark public rapporte des progrès mesurables sur une tâche de distillation.

**Application directe ILH :**

| autoresearch | ILH Phase 2/3 |
|---|---|
| Teacher model (figé) | Qwen3.5-397B-A17B — pseudo-labels du POC (offline) |
| Student model | Lux-Heritage-7B → 2B (architecture modifiable) |
| `train.py` | QLoRA + L = α·CE + (1-α)·KL(student‖teacher) |
| Métrique figée | CER ≤ 2,72% sur 19 blocs CC0 + F1 NER ≥ G0 |
| Budget par run | 5 min MeluXina-AI (A100 80Go) |
| Déclenchement | Porte G2 validée — Mois 4–8 |

**Avantage clé :** le teacher (397B) n'est pas en live — les corrections du POC servent de pseudo-labels offline. Coût teacher = 0€ pendant la boucle. La métrique (CER sur 19 blocs CC0) est déjà instrumentée dans le POC (`poc_bnl_golden.json`).

**`program.md` pour ILH :**
```
Teacher = Qwen3.5-397B-A17B. Ne jamais modifier ses poids.
Student = Lux-Heritage-7B. Tu peux modifier :
  architecture (layers, hidden, heads), température KD (T),
  mixing α, optimizer, scheduler, sampling.
Amélioration si : CER ≤ 2,72% ET F1 NER ≥ G0
  ET params student ≤ run précédent.
Budget : 5 min · A100 MeluXina-AI
```

**Intégration roadmap :** Point d'entrée = porte G2 (Phase 2, Mois 4–8), après le fine-tuning manuel de base validé. Autoresearch explore ensuite l'espace hyperparamétrique automatiquement.

---

### Signal 1.5 · Qwen3-VL OCR 32 langues — caractères anciens et rares
**Source :** SiliconFlow · Qwen3-VL changelog  
**Scoring BnL :** ★★★★☆ Signal continu

Qwen3-VL (sept. 2025) a étendu le support OCR à 32 langues avec amélioration explicite sur les **caractères anciens et rares, le jargon technique, et l'analyse de structure de longs documents**. Confirmation directe par le résultat POC : img5 Fraktur 1850 : 25,19% → 2,04% en zero-shot.

---

## Axe 2 — Infrastructure et financement

### Signal 2.1 · HPC-AI BRIDGES — appel ouvert 1er mars 2026
**Source :** aifactory.lu  
**Scoring BnL :** ★★★★★ URGENT

Le second appel HPC-AI BRIDGES est ouvert depuis le 1er mars 2026. Le projet ILH (fine-tuning QLoRA Qwen3.5-35B-A3B sur données CC0 BnL + distillation 7B sur MeluXina-AI) correspond exactement au profil attendu : institution publique LU ✓, données CC0 ✓, MeluXina-AI ✓, partenariat Uni.lu/C²DH ✓.

**Budget estimé :** Phase 2 fine-tuning : 50–200€/run · Distillation 35B→7B : 500–1 500€ total.

---

## Axe 3 — Communauté et réglementation

### Signal 3.1 · REMI Initiative — Esch-Belval, 17 mars 2026
**Source :** aifactory.lu  
**Scoring BnL :** ★★★☆☆

Plenière REMI (Regulation Meets Innovation) le 17 mars 2026 à Esch-Belval. Rassemble l'écosystème IA luxembourgeois autour de l'adoption responsable.

---

### Signal 3.2 · Deadline candidature BnL — 27 mars 2026
**Source :** bnl.public.lu  
**Scoring BnL :** ★★★★★ — Deadline absolue

La deadline de candidature pour le poste de Responsable projets IA et Data (réf. F00040485) est le **27 mars 2026** via MyGuichet.

---

## Tableau de bord — Signaux mars 2026 (1–17)

| # | Signal | Score | Urgence | Statut |
|---|--------|-------|---------|--------|
| 1.3 | POC ILH réalisé (14 mars) | ★★★★★ | — | ✅ Porte 1 franchie |
| 3.2 | Deadline candidature BnL (27 mars) | ★★★★★ | 27 mars | 🔄 En cours |
| 1.2 | HIPE-OCRepair données disponibles | ★★★★★ | Avant 23 mars | ⚠️ Action requise |
| 2.1 | HPC-AI BRIDGES appel mars | ★★★★★ | Deadline ? | ⚠️ Dossier à soumettre |
| **1.4** | **Autoresearch Karpathy → ILH G2 (17 mars)** | **★★★★☆** | **Phase 2/3** | **🆕 Nouveau** |
| 1.1 | Qwen3.5 Small (2 mars) | ★★★★☆ | Benchmark | 🔄 À tester |
| 3.1 | REMI Initiative (17 mars) | ★★★☆☆ | 17 mars | 📅 Aujourd'hui |

---

*Bulletin produit dans le cadre de la candidature BnL réf. E00040484.*  
*Dernière mise à jour : 17 mars 2026 · Prochaine révision : bulletin complet fin mars.*
