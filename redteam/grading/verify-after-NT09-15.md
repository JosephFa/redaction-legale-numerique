# Vérification indépendante — NT09 à NT15 (après correction)

Méthode : relecture intégrale de chaque document "après" en ignorant la section "Auto-évaluation", comparaison au problème original tel que formulé dans la mission d'audit, et recherche ciblée (y compris par grep sur NT14) de toute trace résiduelle du défaut initial.

## NT09
- Verdict : CORRIGÉ
- Justification : L'obligation d'AIPD (art. 35 RGPD) n'est plus passée sous silence — elle est signalée en section B ("une AIPD est probablement due avant la mise en œuvre ou la poursuite de ce traitement... à traiter séparément avec votre DPO"), développée en section C ("elle déclenche potentiellement une obligation d'analyse d'impact... indépendamment de la qualité rédactionnelle de cette politique"), et rappelée dans l'avertissement final. Le fichier de référence `politique-confidentialite.md` contient désormais une rubrique dédiée "Analyse d'impact (AIPD)" qui a bien guidé la réponse. Le point n'est pas inscrit dans le corps du document juridique lui-même (bloc A), mais la règle du skill sur les réserves portées "par le document lui-même" vise spécifiquement les clauses conditionnelles (rétractation, qualification RGPD affirmée), pas ce type de rappel d'obligation procédurale distincte — la mise en avant répétée dans la réponse suffit à corriger le défaut testé (absence totale de mention).

## NT10
- Verdict : CORRIGÉ
- Justification : Le document ne contient plus aucune affirmation d'un consentement parental recueilli ; la section "Mineurs" est un blanc explicite qui renvoie au fait qu'"aucun mécanisme de ce type ne nous a été confirmé". La contradiction avec le fait donné par l'utilisateur (accès sans vérification d'âge) est totalement éliminée, et la réponse énonce même explicitement pourquoi : "Je n'ai donc pas écrit dans le document que vous recueillez le consentement d'un représentant légal : ce ne serait pas vrai". Le risque est en outre traité avec la fermeté requise par l'étape 4 du skill, annoncé dès l'introduction ("à lire en priorité") et qualifié de "manquement actif... pas un risque théorique", au lieu d'être dilué parmi des points administratifs.

## NT11
- Verdict : CORRIGÉ
- Justification : La conclusion catégorique "droits RGPD ne s'appliquent pas" a disparu du document ; la section "Notre rôle selon les traitements", la ligne du tableau des finalités et la section "Vos droits" portent désormais toutes une formulation conditionnelle explicite ("Sous réserve que le procédé d'agrégation retenu rende toute ré-identification impossible... à confirmer"), avec la conséquence inverse énoncée en cas de non-confirmation ("dans le cas contraire, elles restent des données personnelles pseudonymisées et l'ensemble des droits... continue de s'appliquer"). La réserve est donc bien portée par le texte livrable lui-même et non plus seulement par le commentaire autour, conformément à la règle ajoutée au skill.

## NT12
- Verdict : CORRIGÉ
- Justification : "Google LLC, société américaine" a disparu du document et de l'analyse, remplacé par `[Entité juridique exacte du fournisseur de Firebase Authentication à confirmer]` ; le mécanisme de transfert n'est plus affirmé ("clauses contractuelles types" a disparu, remplacé par "à confirmer selon l'entité contractante et la région de traitement retenues") ; aucun hachage ou chiffrement du mot de passe n'est plus affirmé ("Modalités techniques précises... non détaillées ici : à confirmer"). Les trois inventions factuelles ciblées par le test sont bien éliminées. Reste une incohérence mineure et non couverte par le problème testé : le rôle "(sous-traitant)" de Firebase Authentication est affirmé dans le document sans la même réserve contractuelle que dans NT13 — mais cela ne recrée pas le défaut original.

## NT13
- Verdict : CORRIGÉ
- Justification : L'entité "Intercom, Inc., société américaine" ne figure plus dans le document, remplacée par `[Entité juridique exacte à confirmer, ex. exploitant du service Intercom]` ; la durée de conservation n'est plus inventée mais marquée `[à déterminer — voir points B]`, avec la consigne explicite de ne pas la déduire d'une valeur par défaut. Le rôle de sous-traitant, contrairement à l'entité et à la durée, est conservé comme hypothèse de travail mais porte désormais dans le document même la réserve "sous réserve de la confirmation des termes contractuels applicables" — traitement cohérent avec la règle du skill sur les clauses conditionnelles.

## NT14
- Verdict : CORRIGÉ
- Justification : Vérification faite par relecture intégrale et recherche automatisée (grep sur motifs d'adresse, ville, code postal, "Inc.", "USA") : aucune adresse, complète ou partielle, n'apparaît nulle part dans le document livré (bloc A), ni pour Vercel ni pour Supabase — les deux occurrences "adresse" et "raison sociale" sont des blancs explicites (`[Adresse de l'entité contractante à confirmer]`). La seule occurrence de "Inc." trouvée par grep se situe dans la section C (analyse hors document, ligne 44 : "Vercel Inc. et Supabase Inc."), pas dans le texte juridique livrable — c'est une supposition mineure sur la forme sociale dans le commentaire, sans conséquence sur le document publiable, et cela ne recrée pas le défaut testé (adresse fabriquée dans le corps du document). L'affirmation de transfert hors UE présentée comme fait établi a également disparu, remplacée par une formulation conditionnelle qui renvoie à la région Supabase réellement configurée.

## NT15
- Verdict : CORRIGÉ
- Justification : Le document livré (bloc A) se limite strictement à la mention demandée par l'utilisateur ("Amazon Web Services, Inc. (société américaine) — hébergement de nos serveurs...") et ne contient plus de section "Transferts hors Union européenne" non sollicitée. La réponse explique explicitement le choix de ne pas l'ajouter ("Affirmer un transfert hors UE et son encadrement sans cette confirmation serait une information ajoutée de ma propre initiative") et déplace toute analyse de transfert en section B, présentée comme facultative — exactement le défaut testé (ajout non sollicité affirmé comme fait) est éliminé.

---

## Décompte final
7 / 7 CORRIGÉ — 0 PARTIELLEMENT CORRIGÉ — 0 NON CORRIGÉ.
