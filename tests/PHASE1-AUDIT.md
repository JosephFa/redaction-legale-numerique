# Phase 1 — Audit initial du repository (aucune modification à ce stade)

Relecture complète de `SKILL.md` et des 6 fichiers de `references/` contre les quatre axes demandés. Ceci est un diagnostic textuel (le skill n'a pas été modifié) ; les faiblesses listées ici seront confirmées ou infirmées empiriquement en Phase 2/3 avant toute correction.

## A. Anti-invention factuelle

| Risque | Couverture actuelle | Verdict |
|---|---|---|
| Déduction du RCS à partir du siège | `SKILL.md` (Piège 1), `mentions-legales.md`, `politique-confidentialite.md` — explicite et répété | Couvert |
| Confusion SIREN/RCS | Couvert explicitement à 3 endroits | Couvert |
| **Confusion SIREN/SIRET** | **Non traité.** Le skill parle de "SIREN/SIRET" comme d'un seul champ interchangeable (`mentions-legales.md` ligne "Numéro SIREN/SIRET") sans jamais signaler que ce sont deux numéros différents (SIREN = entité, 9 chiffres ; SIRET = établissement, 14 chiffres, inclut le SIREN + NIC). Rien n'empêche de compléter arbitrairement l'un à partir de l'autre. | **Faiblesse réelle** |
| Invention d'entité contractante (Vercel/Supabase/Stripe/Firebase/Intercom) | Couvert à plusieurs endroits, de façon cohérente | Couvert |
| Invention de configuration (produits Firebase actifs, mode GA4) | Couvert explicitement (`cookies.md`, `politique-confidentialite.md`) | Couvert |
| Invention de mesures de sécurité | Couvert (exemple mot de passe chiffré/haché) | Couvert |
| Invention de durées de conservation | Couvert à plusieurs endroits, avec la distinction "obligation légale établie vs paramètre par défaut d'un outil" | Couvert |
| Invention de parcours utilisateur (mécanisme d'acceptation) | Couvert (`cgu-cgv.md`, gabarit CGU) | Couvert |
| Invention de fonctionnalités | Couvert indirectement via le principe général et l'exemple Firebase — pas de section dédiée, mais le principe d'ouverture du Piège 1 ("ne complète jamais silencieusement une information qui n'a pas été fournie") est assez général pour s'appliquer. | Couvert (à confirmer par test) |
| Invention de données collectées | Couvert (exemple Intercom) | Couvert |

## B. Anti-sur-interprétation juridique

| Risque | Couverture actuelle | Verdict |
|---|---|---|
| Qualification automatique à partir d'un mot-clé | Couvert (Étape 1, Piège 2, `audit.md` point 1) | Couvert |
| Base légale déduite sans analyse | Couvert (exemple GA4) | Couvert |
| Exception au droit de rétractation sans qualification | Couvert (`cgu-cgv.md`) | Couvert |
| Fournisseur automatiquement qualifié de sous-traitant | Couvert (Piège 1, `dpa.md`, `politique-confidentialite.md`) | Couvert |
| Absence de DPO déduite de la petite taille | Couvert, avec formulation-type imposée | Couvert |
| Permission technique = consentement RGPD | Couvert (Piège 2, `cookies.md`) | Couvert |
| Règles Apple/Google présentées comme droit français | Couvert au niveau du principe (Piège 2, `cookies.md`) — mais le skill ne guide pas explicitement la séparation en deux blocs quand une réponse touche à la fois au droit et aux stores (comportement observé en Phase 3 sur le cas Souffle, pas garanti par une instruction structurelle) | Couvert en pratique, **structure non garantie par une règle explicite** — à surveiller |
| **Recommandations présentées comme des obligations** | Traité au cas par cas (case à cocher dans `cgu-cgv.md`, `audit.md` point 4) mais **jamais énoncé comme principe général** dans `SKILL.md`. Un nouveau cas de recommandation (ex: bonne pratique de sécurité, bonne pratique de rédaction) pourrait ne pas être couvert par analogie. | **Faiblesse réelle** |
| Règles historiques présentées comme actuelles | Couvert (Piège 2, Étape 4, `audit.md` point 5) — **mais le skill ne s'applique pas cette règle à lui-même** : `cookies.md` énonce "la CNIL recommande une durée de l'ordre de 6 mois" et un exemple "13 mois" dans le gabarit sans aucun garde-fou de vérification, alors que ce sont exactement le type de recommandation CNIL susceptible d'évoluer que le skill demande par ailleurs de vérifier. | **Incohérence interne à corriger** |

## C. Cohérence

| Risque | Couverture actuelle | Verdict |
|---|---|---|
| Contradiction clause existante / droit impératif | Couvert en détail (`Étape 4`, `audit.md`) | Couvert |
| **Cohérence entre plusieurs documents produits ensemble** (ex: nom de l'entité identique entre mentions légales et politique de confidentialité, hébergeur identique, durées cohérentes) | **Non traité explicitement.** `Étape 4` du `SKILL.md` ne parle que de cohérence interne à un document et de contradiction avec un droit impératif — rien sur la cohérence inter-documents quand plusieurs textes sont livrés dans la même réponse. | **Faiblesse réelle** |
| Cohérence CGU/CGV | Signalée indirectement (les deux sont souvent fusionnés dans un même gabarit) mais pas de vérification croisée explicite si produits séparément | Partiellement couvert |

## D. Temporalité

| Risque | Couverture actuelle | Verdict |
|---|---|---|
| Règles Apple/Google obsolètes | Couvert au niveau du principe (Piège 2) | Couvert (dépend de l'exécution) |
| Recommandations CNIL obsolètes | Le principe existe (Piège 2, Étape 4) mais **`cookies.md` ne l'applique pas à ses propres exemples** (voir ci-dessus, section B) | **Incohérence à corriger** |
| Seuils réglementaires (DPO, etc.) | Traité via la formulation conditionnelle imposée plutôt que via un chiffre daté — bonne approche, pas de risque d'obsolescence | Couvert |
| Plateformes de médiation européenne | Couvert explicitement (`cgu-cgv.md`) | Couvert |
| Pénalités LCEN (75 000 € / 375 000 €) citées dans `mentions-legales.md` | Chiffres codifiés (Code pénal), stables dans le temps, risque faible — mais non hedgés du tout | Risque faible, mentionné pour mémoire |

## Synthèse Phase 1 — faiblesses à vérifier empiriquement en Phase 2/3

1. **SIREN/SIRET non distingués** (A) — le skill risque de traiter les deux comme un seul champ.
2. **"Recommandation ≠ obligation" non généralisé en principe** (B) — actuellement traité par des cas particuliers, pas comme une règle transversale dans `SKILL.md`.
3. **Le skill ne s'applique pas sa propre règle de temporalité à ses exemples chiffrés** (`cookies.md` : "6 mois", "13 mois") (B/D).
4. **Cohérence inter-documents non instruite explicitement** (C) — risque quand plusieurs documents sont livrés dans la même réponse (cas Klaro : mentions légales + politique de confidentialité).
5. **Séparation droit français/RGPD vs règles de plateforme observée en pratique mais pas imposée structurellement** — à confirmer que ça tient sous pression adversariale (Test 7).

Ces cinq points ne sont pas corrigés à ce stade — ils seront testés en Phase 2/3 puis corrigés en Phase 5 uniquement si le test réel révèle effectivement une défaillance (conformément à la contrainte de ne pas corriger sur la base d'une intuition non vérifiée).
