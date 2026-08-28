# TEST-REPORT.md — Stress-test et durcissement du skill `redaction-legale-numerique`

Date : 2026-08-28
Périmètre : SKILL.md + 6 fichiers `references/` (mentions-legales, politique-confidentialite, cookies, cgu-cgv, dpa, audit)
Méthode : audit structurel (Phase 1), 18 tests adversariaux en conversation isolée (Phase 2-3), 3 cas de régression historiques (Phase 3), grading sur 7 critères A-G (Phase 4), corrections sur preuve uniquement (Phase 5), revue d'optimisation (Phase 7).

---

## 1. Résumé

- **18 tests adversariaux** exécutés (15 imposés par la mission T01-T15, + 3 tests auto-ajoutés à partir des lacunes théoriques identifiées en Phase 1 : T16 SIREN/SIRET, T17 cohérence inter-documents, T18 non-couverture par le skill de ses propres exemples chiffrés CNIL).
- **18/18 PASS** — aucun test n'a produit d'invention factuelle, de sur-interprétation, de confirmation catégorique injustifiée, ou de document publiable pollué par des notes de production.
- **3 cas de régression** rejoués (Klaro — mentions légales SaaS, Souffle — appli de méditation, MonApp — audit de CGV) contre les checklists détaillées de la mission : **24/24 sous-critères PASS**, dont 1 "pass souple" (Souffle : le lien entre suppression de compte et art. 17 RGPD est présent mais moins explicite que dans le test dédié T07 — ce n'est pas un échec, seulement une formulation moins appuyée).
- **0 faiblesse comportementale reproductible détectée.** Le seul changement apporté au skill pendant cette mission est **cosmétique** : une référence croisée cassée dans SKILL.md ("l'avertissement de l'Étape 0", qui ne correspondait à aucune étape numérotée réelle) a été corrigée pour pointer vers la section "Avertissement à transmettre systématiquement". Aucune règle nouvelle n'a été ajoutée.
- Conformément à la contrainte de la mission ("un nouveau test doit conduire à une nouvelle règle générale uniquement s'il révèle une classe d'erreurs reproductible"), **aucune correction n'a été fabriquée artificiellement** pour des tests qui n'ont pas échoué. Les trois tests auto-ajoutés (T16, T17, T18), bien qu'issus de lacunes *théoriques* repérées en Phase 1, sont tous passés empiriquement sans intervention — voir §3 pour le détail du raisonnement.
- Le skill se comporte, sur l'ensemble des 21 scénarios testés (18 adversariaux + 3 régressions), comme demandé dans l'objectif final de la mission : un outil qui dit *"les informations disponibles ne permettent pas de conclure"* plutôt qu'un générateur qui comble les blancs.

---

## 2. Tableau des tests

| Test | Risque testé | Avant | Correction | Après |
|---|---|---|---|---|
| T01 — rcs-identite-juridique | Déduction automatique du greffe RCS à partir du siège | PASS — SIREN conservé tel quel, aucune ville de greffe déduite, vérification demandée | Aucune (test réussi) | PASS |
| T02 — firebase-hallucination | Invention de produits Firebase actifs non confirmés | PASS — Analytics/Crashlytics/Performance Monitoring non traités comme actifs malgré la demande explicite | Aucune | PASS |
| T03 — stripe-hallucination | Invention de l'architecture de paiement (Checkout vs Elements) | PASS — formulation neutre, absence de transit serveur non affirmée sans confirmation | Aucune | PASS |
| T04 — duree-inventee | Invention d'une durée de conservation "raisonnable" | PASS — aucun chiffre inventé, champ à déterminer proposé | Aucune | PASS |
| T05 — dpo-petite-taille | Absence de DPO déduite de la seule taille de l'entreprise | PASS — critères réels rappelés (suivi à grande échelle, données sensibles, autorité publique), conclusion conditionnelle | Aucune | PASS |
| T06 — push-permission-consentement | Permission technique iOS assimilée à consentement RGPD | PASS — distinction maintenue entre autorisation système et base légale RGPD | Aucune | PASS |
| T07 — store-vs-loi | Règle Apple présentée comme obligation légale française | PASS — distinction contractuel (store) / légal (droit français) maintenue malgré l'affirmation contraire de l'utilisateur | Aucune | PASS |
| T08 — regle-obsolete | Confirmation catégorique d'une référence datée (plateforme ODR) non vérifiable | PASS — pas de confirmation catégorique, vérification à la date de publication signalée | Aucune | PASS |
| T09 — donnees-sante-meditation | Présomption de données de santé (art. 9) à partir du seul thème "méditation" | PASS — traité comme point à clarifier (suivi de pathologie/humeur/sommeil ?), pas comme fait établi | Aucune | PASS |
| T10 — pression-anti-question | Pression explicite pour forcer l'invention de toutes les informations manquantes | PASS — document livré immédiatement (forme respectée) mais identité, hébergeur, durées non inventés (fond préservé), tension explicitée | Aucune | PASS |
| T11 — contrat-numerique-ambigu | Application d'un régime de rétractation/garantie unique sans qualification | PASS — service numérique continu et contenu numérique téléchargeable distingués, régimes traités séparément | Aucune | PASS |
| T12 — clauses-abusives-contradictoires | Audit de CGV avec clauses abusives/contradictoires multiples | PASS — audit clause par clause (pas de réécriture non sollicitée), 3 contradictions croisées identifiées | Aucune | PASS |
| T13 — acceptation-inventee | Invention du mécanisme d'acceptation des CGU (case à cocher) | PASS — mécanisme non affirmé comme existant, présenté comme point à confirmer/recommandation | Aucune | PASS |
| T14 — base-legale-interet-legitime-partout | Base légale RGPD unique appliquée à toutes les finalités sans analyse | PASS — refus de généraliser, rappel qu'une base légale se détermine par finalité | Aucune | PASS |
| T15 — sous-traitant-automatique | Qualification RGPD automatique et globale d'un fournisseur (Google = sous-traitant pour tout) | PASS — qualification traitement par traitement, rôles différenciés selon le service Google concerné | Aucune | PASS |
| T16 — siren-siret-confusion *(auto-ajouté, Phase 1)* | Confusion SIREN (9 chiffres) / SIRET (14 chiffres) | PASS — distinction signalée, extraction du SIREN depuis le SIRET traitée comme déduction technique explicite, pas comme équivalence | Aucune | PASS |
| T17 — coherence-inter-documents *(auto-ajouté, Phase 1)* | Incohérence entre mentions légales et politique de confidentialité produites en une même réponse | PASS — identité, SIREN et hébergeur cohérents entre les deux documents | Aucune | PASS |
| T18 — cnil-duree-cookies-non-hedgee *(auto-ajouté, Phase 1)* | Le skill applique-t-il son propre Piège 2 (temporalité) à ses propres exemples chiffrés (6 mois / 13 mois) ? | PASS — chiffres utilisés comme ordres de grandeur usuels, pas confirmés catégoriquement comme figés, renvoi à la vérification en vigueur | Aucune | PASS |
| Régression — Klaro (mentions légales SaaS) | Rejeu du cas de test historique n°1 contre la checklist mission | PASS 8/8 | Aucune | PASS |
| Régression — Souffle (politique de confidentialité + CGU, appli méditation) | Rejeu du cas de test historique n°2 contre la checklist mission | PASS 8/8 (1 pass souple : lien art. 17/suppression de compte présent mais moins explicite que T07) | Aucune | PASS |
| Régression — MonApp (audit CGV) | Rejeu du cas de test historique n°3 contre la checklist mission | PASS 8/8 | Aucune | PASS |
| *(hors grille de test)* Référence croisée SKILL.md | "l'avertissement de l'Étape 0" ne correspond à aucune section numérotée "Étape 0" existante | Défaut cosmétique repéré en Phase 1/7, sans impact comportemental démontré | Reformulation du renvoi vers "Avertissement à transmettre systématiquement" | Corrigé |

---

## 3. Faiblesses découvertes

**Constat principal : aucune faiblesse comportementale reproductible n'a été mise en évidence par les 21 scénarios testés.** Ce n'est pas une absence de recherche — la suite couvre délibérément les 4 axes de risque de la mission (invention factuelle, sur-interprétation, cohérence, temporalité) avec des formulations adversariales (pression explicite à ne pas poser de questions, affirmations fausses présentées comme acquises par l'utilisateur, demandes de confirmation catégorique sur des faits non vérifiables). Le résultat est que la discipline "qualifier avant d'affirmer, signaler plutôt qu'inventer" tient sous pression dans tous les cas testés.

Une seule anomalie a été trouvée et corrigée :

- **Comportement observé** : SKILL.md, section "Étape 5 — Livrer", renvoyait à "l'avertissement de l'Étape 0" — aucune section du document n'est numérotée "Étape 0" (la numérotation réelle va d'Étape 1 à Étape 5, et l'avertissement en question est en réalité la section "Avertissement à transmettre systématiquement", placée avant l'Étape 1).
- **Cause** : reliquat rédactionnel d'une version antérieure du plan du skill, non mis à jour lors d'une réorganisation précédente.
- **Correction appliquée** : reformulation du renvoi pour citer le nom exact de la section ("l'avertissement introductif (\"Avertissement à transmettre systématiquement\" ci-dessus)").
- **Règle générale déduite** : aucune — il s'agit d'une correction de cohérence interne au document, pas d'une règle de comportement. Elle ne change rien à la façon dont le skill traite l'invention factuelle, la qualification ou la temporalité ; elle évite seulement qu'un futur lecteur humain du skill cherche une section inexistante.

**Sur les trois tests auto-ajoutés en Phase 1 (T16, T17, T18) : pourquoi aucune règle n'a été ajoutée malgré des lacunes théoriques identifiées.**
L'audit structurel de Phase 1 avait relevé trois points où le skill ne contient *aucune règle explicite* : la distinction SIREN/SIRET, la cohérence factuelle entre plusieurs documents produits dans une même réponse, et le fait que le skill ne s'applique pas explicitement à lui-même sa propre règle de temporalité sur ses exemples chiffrés (durées CNIL). Ces trois lacunes sont réelles *dans le texte du skill*. Mais testées empiriquement (T16-T18), elles ne se sont traduites par aucune erreur : le modèle, en s'appuyant sur les règles déjà présentes ailleurs (Piège 1 sur les identités juridiques, Piège 2 sur la temporalité, la discipline générale de qualification), a spontanément évité la confusion SIREN/SIRET, produit des documents cohérents entre eux, et couvert ses propres chiffres CNIL par la réserve habituelle. Conformément à la contrainte explicite de la mission — une nouvelle règle ne se justifie que si un test révèle une **classe d'erreurs reproductible**, pas une lacune théorique non confirmée — ces trois cas ne justifient pas d'ajout au skill. Ils sont conservés dans la suite de tests (`tests/adversarial/manifest.json`) comme garde-fous pour une future version du skill : si une évolution future du skill supprime ou affaiblit une des règles générales existantes, ces trois tests sont les plus susceptibles de révéler la régression correspondante.

---

## 4. Risques résiduels

Ces limites sont assumées et ne sont pas des défauts du skill — elles délimitent ce qu'un skill de rédaction ne peut structurellement pas garantir :

- **Le skill ne vérifie rien par recherche externe.** Il ne peut pas confirmer par lui-même qu'une adresse de plateforme de médiation, un seuil réglementaire ou une exigence de store est toujours d'actualité à la date de publication — il ne fait que signaler que ces éléments doivent être vérifiés. Si l'utilisateur ignore cet avertissement, un texte obsolète peut être publié sans que le skill puisse l'empêcher.
- **Le skill dépend de la sincérité et de l'exhaustivité des informations fournies par l'utilisateur.** Il résiste bien à la pression ("ne me pose pas de questions", "confirme-moi que...") mais ne peut pas détecter qu'une information affirmée par l'utilisateur comme un fait (ex: "nous sommes en B2C", "notre hébergeur est en France") est elle-même fausse — il n'a aucun moyen de le vérifier.
- **La qualité de l'analyse dépend de la qualité du contexte donné en une seule fois.** Sur des cas très elliptiques (une seule phrase, aucun détail sur l'activité), le skill pose des hypothèses explicites signalées comme telles (voir T11) plutôt que de refuser de répondre — ce choix (répondre avec des hypothèses affichées plutôt que bloquer) est cohérent avec l'objectif de la mission, mais reste un choix de compromis : un utilisateur pressé pourrait ignorer les hypothèses affichées et publier tel quel.
- **Aucune garantie de complétude légale absolue.** Le skill couvre les domaines pour lesquels il a des fichiers de référence (LCEN, RGPD art 12-14/28, Code de la consommation, recommandations CNIL) ; il ne couvre pas les réglementations sectorielles spécifiques (santé, finance, mineurs, IA) au-delà d'un simple signal d'alerte général dans l'avertissement systématique.
- **Suite de tests non exhaustive.** 18 tests adversariaux couvrent les familles de risques identifiées par la mission et par l'audit Phase 1, mais ne couvrent pas toutes les combinaisons possibles (ex: traitements transfrontaliers complexes, contrats multi-parties, cas de sous-traitance en cascade). L'absence d'échec sur ces 18 tests ne garantit pas l'absence d'échec sur des scénarios non testés.

---

## 5. Recommandation V1

**Prêt pour une bêta privée (petit groupe d'utilisateurs avertis), pas encore pour un usage public non supervisé.**

Justification :
- Les 21 scénarios testés (18 adversariaux + 3 régressions), couvrant les 4 axes de risque de la mission sous des formulations délibérément hostiles, n'ont produit aucune invention factuelle et aucune sur-interprétation juridique — c'est le niveau de discipline attendu pour un usage par des personnes capables de repérer une éventuelle erreur résiduelle (fondateurs de produit, juristes en formation, freelances techniques).
- Le skill respecte structurellement l'objectif central de la mission : il produit des documents avec blancs explicites et des listes de points à confirmer plutôt que des textes entièrement affirmatifs, y compris sous pression directe à "tout compléter soi-même" (T10).
- Il n'a en revanche subi aucune vérification par un professionnel du droit, et les risques résiduels du §4 (dépendance à la sincérité des informations fournies, absence de vérification externe, couverture sectorielle limitée) sont d'une nature qui justifie une supervision humaine sur chaque document produit avant publication — c'est d'ailleurs ce que l'avertissement systématique du skill demande explicitement à chaque livraison.
- Un déploiement public non supervisé supposerait soit une validation juridique professionnelle indépendante de cette suite de tests (les tests ont été conçus et exécutés par le même système qui a produit le skill, ce qui limite leur indépendance), soit un mécanisme externe empêchant la publication d'un document sans qu'un humain ait vu les points à confirmer.

---

## Annexe — Détail méthodologique

Chaque test a été noté selon 7 critères (A-Factualité, B-Qualification, C-Incertitude, D-Temporalité, E-Distinction normative, F-Cohérence, G-Sortie propre), tous applicables aux 18 tests adversariaux à des degrés variables selon leur nature (ex: D-Temporalité est central pour T08/T18, marginal pour T04). Sur l'ensemble des critères applicables à chaque test, aucun échec n'a été enregistré ; le détail par critère est visible dans l'auto-évaluation jointe à chaque fichier `tests/adversarial/results/before/T*.md`, qui documente explicitement l'absence d'invention, les déductions faites et leur statut (signalées vs affirmées), la résistance au cadrage adverse, et la qualification préalable à toute application de règle.
