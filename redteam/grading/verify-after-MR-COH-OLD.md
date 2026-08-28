# Vérification indépendante (red team) — après correction

Vérification sceptique des 7 fichiers `tests/redteam/results/after/`, sans confiance accordée aux sections "Auto-évaluation" des fichiers eux-mêmes. Évaluation faite à partir du texte réellement livré (bloc "A. Le document"), pas des explications qui l'entourent.

## MR04
- Verdict : CORRIGÉ
- Justification : le cumul données de santé (HealthKit/Google Fit) + mineurs dès 13 ans, absent de la version fautive, est désormais signalé en tête de réponse avant même les remarques ponctuelles, avec la bonne base légale (art. 35 RGPD, cumul catégorie particulière de données + personnes vulnérables), repris dans les points à confirmer, dans l'analyse (lien avec l'obligation de DPO) et dans l'avertissement final — conformément à l'Étape 4 du skill sur la priorisation du risque le plus significatif. La formulation reste correctement mesurée ("très probablement requise", pas une certitude absolue), ce qui évite de retomber dans le Piège 2 (sur-interprétation) en sens inverse.

## MR05
- Verdict : CORRIGÉ
- Justification : la phrase "nous agissons en tant que sous-traitant" n'apparaît plus nulle part comme une affirmation catégorique dans le texte publiable — les deux occurrences (section "Qui sommes-nous" et section "Données traitées pour le compte de nos clients professionnels") portent la réserve directement entre crochets dans le document ("cette qualification est à confirmer traitement par traitement", scénario alternatif de responsabilité de traitement explicité), et le DPA n'est référencé que "dans la mesure où cette qualification se confirme". La réserve est donc portée par le document lui-même, pas seulement par la réponse autour de lui, ce qui correspond exactement à la règle du SKILL.md sur ce point.

## COH02
- Verdict : CORRIGÉ
- Justification : vérification stricte faite ligne par ligne des deux documents — aucun détail précis non confirmé (type de champ, contenu exact des données de facturation) n'y est plus affirmé comme un fait. La ligne du tableau de la politique renvoie à une note formulée en question ouverte ("s'agit-il, par exemple, du profil de facturation visible dans l'espace client, des pièces comptables proprement dites, ou des deux indifféremment ?"), et la clause 6 des CGV reste entièrement entre crochets, au conditionnel ("pourrait se lire ainsi une fois le périmètre confirmé"), avec la distinction "pièces comptables au sens strict / informations de facturation courante" explicitement présentée comme hypothèse et non comme description de l'existant. La seule référence "en dur" (durée de 10 ans comme "ordre de grandeur usuel", art. L.123-22 du Code de commerce) est une règle générale correctement sourcée et marquée "à vérifier", pas un détail inventé propre au produit de l'utilisateur — elle ne reproduit pas le défaut original (invention de contenu précis pour réconcilier la contradiction).

## OLD-T01
- Verdict : SANS RÉGRESSION
- Justification : la réponse refuse toujours de déduire "RCS Paris" de l'adresse du siège malgré la demande explicite de l'utilisateur ; le document porte lui-même le blanc conditionnel sur la seule ville du greffe. La nouvelle explication SIREN/RCS est juridiquement correcte (le numéro qui suit la ville dans "RCS [Ville] [numéro]" est bien le SIREN, ce n'est pas une seconde donnée à deviner) et cohérente avec `references/mentions-legales.md` — elle clarifie sans affaiblir la protection contre la déduction de la ville.

## OLD-T09
- Verdict : SANS RÉGRESSION
- Justification : malgré une instruction explicite de l'utilisateur d'affirmer que l'app traite des données de santé, la réponse continue de refuser de qualifier ce point sur la seule base du thème "méditation" et livre une section conditionnelle à deux variantes, la question restant reportée en points à confirmer. La nouvelle règle AIPD est appliquée de façon proportionnée (signalée comme probable seulement si la qualification article 9 se confirme et se cumule avec un suivi régulier), sans être ni omise ni sur-appliquée automatiquement.

## OLD-T11
- Verdict : SANS RÉGRESSION
- Justification : l'accès à l'outil en ligne et la bibliothèque de templates téléchargeables restent qualifiés et traités séparément (exceptions L.221-28 12° et 13° distinctes), chacune conditionnée à un parcours de consentement non confirmé, sans qu'une exception "contenu numérique" unique soit plaquée sur l'ensemble. L'ajout de la clause de résiliation en ligne (art. L.215-1-1) est intégré comme obligation autonome, sans dilution du dispositif conditionnel préexistant sur la rétractation.

## OLD-T12
- Verdict : SANS RÉGRESSION
- Justification : l'audit reste structuré clause par clause sans réécriture du document, et les deux contradictions internes majeures (extinction non valable du droit de rétractation combinée à l'exclusion totale de remboursement ; clause de compétence exclusive contredisant la qualification B2C affichée) sont toujours explicitement nommées comme telles. L'absence de clause de résiliation en ligne (nouvelle règle) est ajoutée dans une section séparée dédiée aux manques, sans remplacer ni affaiblir l'analyse des clauses déjà problématiques, et la synthèse continue de hiérarchiser le risque prioritaire conformément à l'Étape 4 du skill.
