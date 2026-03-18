# PRÉPARATION ENTRETIEN — Responsable projets IA et Data
## BnL | Réf. F00040485 | Djebar Hammouche | Mars 2026

---

## 1. Processus de sélection

Poste employé de l'État (CDI). BnL gère la sélection directement, sans EAG préalable.

| Étape | Contenu | Score actuel |
|-------|---------|-------------|
| 1 · Dépôt MyGuichet | CV + Lettre + Artefact (deadline 27 mars) | 10/10 |
| 2 · Shortlist dossiers | Expérience IA/Data, projets patrimoniaux, artefact | 9/10 |
| 3 · Épreuve spéciale BnL | Entretien professionnel 45-60 min | 8/10 |
| 4 · Langues | Dispensé 2 des 3 langues admin | 9/10 |
| 5 · Admission stage | CDI permanent après 1 an de stage | — |

---

## 2. Composition probable du jury

**Yves Maurer** — Head of IT & Digital Innovation — N+1 direct — Juré technique principal  
Informaticien Imperial College London. BnL depuis 2007. Construit Nautilus-OCR (2020-21) et chatbot (2023).  
→ Veut entendre : vous connaissez ce qu'il a construit. Vous vous branchez EN AVAL. Vous prenez la complexité technique (NER, fine-tuning, distillation) qu'il n'a pas le temps de gérer seul.

**Carlo Blum** — Deputy Director — Signataire MoU AI4LAM — Juré gouvernance/stratégie  
A signé le MoU AI4LAM à la British Library le 3 décembre 2025.  
→ Veut entendre : Vision 2030 maîtrisée. Positionnement CENL/AI4LAM/ALT-EDIC. Maîtrise EU AI Act sans chantier paralysant.

**Membres probables :** RH/CGPO (compétences comportementales) + Chef division Numérisation/Catalogage + Représentant Ministère Culture

---

## 3. Critères d'évaluation

### Compétences techniques (≈ 35 %)
- Maîtrise IA/ML : VLM, NER, fine-tuning QLoRA, distillation, MLOps → 4/5
- Patrimoine numérique : METS/ALTO, OAI-PMH, ARK, Nautilus-OCR, standards GLAM → 5/5
- Pipeline ILH bout en bout : décrire sans notes → 5/5
- EU AI Act : Art.50 chatbot, Art.4 literacy, AIPD, model card → 4/5
- Infrastructure souveraine : CTIE, MeluXina-AI, Apache 2.0 → 4/5

### Gestion de projet (≈ 30 %)
- Méthodologie : QUAPITAL-HERMES + CRISP-ML(Q), 3 portes G0/G2/G4 → 5/5
- Gouvernance publique : décision par comité, délais longs → 4/5
- Parties prenantes : coordonner Uni.lu, CTIE, C²DH, bibnet.lu → 4/5
- Budget : livrer avec ressources limitées → 4/5

### Dimension institutionnelle BnL (≈ 20 %)
- Culture BnL : collections, usagers réels (chercheurs, généalogistes, communes) → 5/5
- Vision 2030 : 7 valeurs, pivot collection → usagers 2025-2028 → 5/5
- Écosystème CENL/AI4LAM : BnF ArGiMi, KB NL Retrotool, BL FRAIM, ALT-EDIC → 4/5

### Compétences comportementales (≈ 15 %)
- Conseiller (A1) : expertise sans imposer les décisions
- Servir le client-usager (A1) : pas seulement chercheurs
- Communication technique : traduire NER/cMER pour non-technique

---

## 4. Questions clés et réponses préparées

**Q : Comment passez-vous de 6 blocs à 800 000 pages ?**  
Phase 1 : Triage EPR — CER > 5% seulement. Phase 2 : QLoRA sur 6 723 CC0 + annotation 200 articles. Phase 3 : distillation 35B → 7B CTIE. Coût : ~2 000 € pour 800 000 pages.

**Q : Comment vous intégrez dans Nautilus-OCR ?**  
EN AVAL — Nautilus produit METS/ALTO, ILH l'enrichit avec NER + corrections OCR. ARK NAAN 70795 préservés.

**Q : EU AI Act sur ILH ?**  
Art.50 : label IA chatbot août 2026 — intégré dès la conception UX. Art.4 : ateliers AI literacy (2h, human in the loop) — prérequis G2. AIPD avant production. Apache 2.0 : obligations fournisseur sur QwenLM.

**Q : Comment ILH s'inscrit dans le programme 2025-2028 ?**  
Pipeline NER explicitement dans le programme. Pivot collection → usagers. Corpus FR/DE/LB → ALT-EDIC (CENL). Même mouvement que BnF/ArGiMi et KB NL/Retrotool.

**Q : NER à un bibliothécaire ?**  
"Vous soulignez des noms dans un document. La NER fait ça sur des millions d'articles. Votre expertise historique est irremplaçable pour valider et corriger."

---

## 5. Questions à poser

- (Yves Maurer) : Contraintes format retour METS/ALTO pour l'interface ILH → eluxemburgensia.lu ?
- (Yves Maurer) : Capacité GPU CTIE actuelle et priorité d'accès MeluXina-AI / AI Factory ?
- (Carlo Blum) : Coordination avec le projet born-digital cataloguing déjà en cours ?
- (Carlo Blum) : Engagements MoU AI4LAM spécifiques à prendre en compte ?

---

## 6. Objections et contre-arguments

- "ILH concurrence Nautilus" → EN AVAL. Nautilus produit le METS/ALTO. ILH l'enrichit.
- "10 ans indépendant — pourquoi employé ?" → Continuité institutionnelle. ILH = 5 phases sur 3 ans.
- "Pas de luxembourgeois" → Dispense demandée. Norme GLAM : anglais. FR/DE pour bibnet.lu.
- "6 blocs c'est petit" → Benchmark officiel Schneider 2023. Comparaison directe sur le même GT.
- "GPT-4o ferait pareil" → Apache 2.0 (CTIE), LB explicite, bbox_2d natif, 670 € vs 19 000 €.

---

## 7. Score global estimé

| Étape | Score | Seuil | Statut |
|-------|-------|-------|--------|
| Dépôt dossier | 10/10 | 10/10 | ✅ |
| Shortlist | 9/10 | 7/10 | ✅ Fort |
| Épreuve technique | 8/10 | 6/10 | ✅ Solide |
| Épreuve stratégique | 8/10 | 6/10 | ✅ Solide |
| Comportemental | 7/10 | 6/10 | ⚠️ À renforcer |
| Langues | 9/10 | Dispensé | ✅ |
| **Global** | **8,2/10** | **6,5/10** | **✅ Finaliste probable** |

---

## 8. ADN BnL — à incarner en entretien

- **Tradition et continuité** : "Le chatbot n'a pas remplacé les bibliothécaires. ILH non plus."
- **Partage** : CC0, open source natliblux, publication LIBER, contribution ALT-EDIC.
- **Fiabilité** : 5 phases, 3 portes formelles, metrics mesurables. Ne pas survendre.
- **Innovation fondée** : POC → mesure cMER → décision. Même démarche que Yves Maurer.
- **Accessibilité pour tous** : "Les généalogistes qui cherchent leur famille dans les journaux de 1900."

---

*Confidentiel — préparation entretien BnL réf. F00040485 · Mars 2026*
