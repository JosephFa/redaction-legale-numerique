---
name: redaction-legale-numerique
description: Rédige et audite les textes légaux français/européens d'un produit numérique (site web, application mobile, SaaS, e-commerce) — mentions légales, politique de confidentialité RGPD, politique de cookies, CGU, CGV, et accords de sous-traitance (DPA). Utilise ce skill dès que l'utilisateur mentionne un de ces documents, ou parle de "conformité RGPD", "mise en conformité juridique", "légal de mon site/appli", "avant de lancer mon site", ou demande de rédiger/générer/vérifier/relire n'importe lequel de ces textes — même s'il ne cite pas leur nom exact, par exemple "j'ai besoin d'un truc légal pour mon site", "qu'est-ce que je dois mettre en bas de page pour être en règle", ou "je collecte des emails, qu'est-ce qu'il me faut niveau RGPD". Toujours déclencher aussi pour un audit/relecture d'un texte légal existant.
---

# Rédaction et audit de textes légaux pour produits numériques (France / UE)

Ce skill aide à produire ou relire des documents juridiques standards pour un site web, une application ou un SaaS opérant sous droit français et RGPD : mentions légales, politique de confidentialité, politique de cookies, CGU, CGV, et DPA (accord de sous-traitance de données).

L'objectif n'est pas seulement de "bien rédiger du juridique". C'est un exercice de discipline en quatre temps : **analyser d'abord, qualifier ensuite, vérifier les obligations, identifier les lacunes** — et ne rédiger que ce qui est suffisamment établi. Un texte fluide qui invente une durée de conservation, ou qui affirme une obligation légale à partir d'un contexte insuffisant, est pire qu'un texte incomplet mais honnête : il donne à l'utilisateur une fausse impression de sécurité juridique. Les deux pièges ci-dessous sont la cause de la quasi-totalité des erreurs sur ce type de tâche — les avoir en tête change la façon d'aborder chaque étape qui suit.

## Avertissement à transmettre systématiquement

Avant de livrer un texte ou un audit, rappelle clairement à l'utilisateur (en une ou deux phrases, pas un pavé) que :
- ce texte est une **base rédigée à partir des exigences légales en vigueur**, pas un avis juridique personnalisé ;
- une **relecture par un avocat ou un DPO** est recommandée avant publication, en particulier si l'activité est réglementée, traite des données sensibles, ou vise des mineurs ;
- le texte devra être **mis à jour** si l'activité, les sous-traitants, ou les traitements de données évoluent, et que certaines règles citées (plateformes de médiation, exigences des stores...) doivent être vérifiées à la date de publication.

## Piège 1 — L'invention factuelle

Ne complète jamais silencieusement une information qui n'a pas été fournie. C'est tentant, parce que le texte a l'air plus "fini" et professionnel avec des détails précis — mais un détail inventé dans un document juridique n'est pas un détail de style, c'est une fausse déclaration. Les catégories qui reviennent le plus souvent :

- **Identité juridique** : ne jamais déduire le greffe/la ville d'immatriculation RCS à partir de l'adresse du siège — ce n'est pas systématique. Le SIREN et le numéro RCS ne sont pas deux informations différentes à inventer l'une à partir de l'autre. Le numéro de TVA intracommunautaire n'est pas automatiquement à afficher : ne le mentionne que s'il t'a été donné ou confirmé.
- **Entité contractante d'un prestataire** : le fait qu'un produit utilise Vercel, Supabase, Stripe, Firebase, Intercom, etc. ne te dit ni l'entité juridique exacte à citer, ni quelles données précises ce prestataire reçoit, ni son rôle RGPD. Prestataire technique ≠ entité juridique pertinente ≠ sous-traitant RGPD automatique : ce sont trois questions distinctes, à vérifier séparément plutôt qu'à déduire du nom du produit.
- **Architecture technique** : ne jamais affirmer qu'un mot de passe est "chiffré" (souvent haché en pratique, mais tu ne le sais pas non plus) ni qu'une architecture de paiement précise est utilisée (Stripe Checkout vs Elements vs autre) si ce n'est pas confirmé. Une formulation neutre ("les données de paiement sont traitées par Stripe selon les modalités applicables au parcours utilisé") vaut mieux qu'un détail inventé.
- **Durées** (conservation, cookies, réponse) : n'invente jamais un chiffre parce qu'il "semble raisonnable". Un paramètre de configuration par défaut d'un outil (ex: la fenêtre de rétention GA4) n'est pas une obligation légale généralisable — présente-le comme tel, ou comme un point à déterminer, jamais comme un fait établi.
- **Mécanismes non décrits** : ne décris pas comme existant un parcours d'acceptation (case à cocher, bouton), une fonctionnalité, ou une mesure de sécurité que l'utilisateur ne t'a pas confirmé avoir. Une recommandation ("une case à cocher au moment de la souscription serait plus solide") reste une recommandation, pas une description de l'existant.

Quand une information factuelle manque, il y a deux façons de la traiter — jamais une troisième qui consiste à l'inventer : la marquer comme un blanc explicite si elle a sa place dans le document (ex: `[SIREN à compléter]`), ou la lister séparément dans ta réponse comme point à confirmer si elle concerne un choix de fond (une durée, une architecture, une base légale).

**La réserve doit être portée par le document lui-même, pas seulement par ta réponse autour de lui.** C'est le piège le plus fréquent sur les clauses conditionnelles (exception de rétractation, renonciation, exemption, qualification RGPD) : si la condition qui déclenche la clause n'est pas confirmée, n'écris jamais la clause comme si cette condition était déjà remplie, même si tu la signales par ailleurs comme point à confirmer dans ta réponse. Un utilisateur qui copie le document sans lire tes points à confirmer doit tomber sur une formulation conditionnelle explicite (ex: `[Applicable uniquement si votre parcours de souscription recueille, de façon distincte et non équivoque, l'accord exprès du client à l'exécution immédiate et sa renonciation au droit de rétractation — à confirmer, voir points B]`), jamais sur une affirmation catégorique que la conversation nuance en parallèle. La même règle vaut pour l'identité d'un prestataire technique (nom légal, adresse, pays d'hébergement) : ne complète jamais ces détails par une valeur "plausible" dans le document, même réaliste — utilise un blanc explicite.

## Piège 2 — La sur-interprétation juridique

Même sans inventer aucun fait, on peut rendre un texte trompeur en appliquant une règle trop vite. Avant de conclure, vérifie que tu n'es pas en train de :
- appliquer une règle (ex: exception au droit de rétractation, exemption de consentement cookies) sans avoir d'abord qualifié précisément le contrat, le service ou les parties concernées ;
- transformer une permission technique en consentement RGPD — une autorisation de notifications au niveau de l'OS, ou l'activation d'un SDK, ne vaut pas consentement RGPD à un traitement de données précis ;
- transformer le nom d'un produit fournisseur en qualification RGPD automatique — "Firebase" n'est pas un seul produit : Auth, Cloud Messaging, Analytics, Crashlytics ont des rôles et des données différents, et la présence de l'un ne prouve pas l'activation des autres ;
- déduire l'absence d'une obligation (DPO, mentions particulières...) d'un contexte de "petite taille" ou "probablement" — si les faits sont insuffisants pour conclure, dis-le, plutôt que de trancher. Une formulation du type *"sur la base des informations communiquées, aucun élément ne permet à ce stade d'identifier telle obligation ; à réévaluer selon l'ampleur réelle de l'activité"* est plus honnête qu'une conclusion catégorique ;
- présenter une règle d'une plateforme (Apple App Store, Google Play) comme une obligation légale française ou européenne — sépare toujours ce qui relève du droit de ce qui relève des règles contractuelles d'un store ;
- citer une règle, une plateforme (ex: le dispositif européen de règlement en ligne des litiges) ou une checklist sans signaler qu'elle doit être vérifiée dans sa version en vigueur à la date de publication — ces règles évoluent.

## Étape 1 — Extraire les faits, puis qualifier

Avant de choisir quels documents produire, fais le tri entre ce qui est **fourni**, ce qui est **manquant**, et ce qui serait une **déduction** de ta part (donc à éviter ou à signaler comme telle). Qualifie ensuite la situation : nature du service, type de contrat concerné (vente d'un bien, fourniture de contenu numérique, service numérique, abonnement, ou combinaison), B2B ou B2C, pays visé, catégories de personnes et de données concernées. Cette qualification conditionne quelles règles s'appliquent réellement — ne saute pas cette étape même quand la réponse semble évidente.

Qualifie aussi le **statut juridique de l'éditeur lui-même** avant de choisir un gabarit d'identité : société, entrepreneur individuel, association, ou société étrangère ne suivent pas le même modèle de mentions légales ni le même régime de droit de la consommation. Un numéro SIRET ou SIREN fourni ne prouve pas à lui seul qu'il s'agit d'une société commerciale — une association loi 1901, par exemple, en dispose souvent aussi mais n'a ni capital social ni immatriculation RCS. Si l'éditeur n'est pas établi en France mais vise des consommateurs français, ne calque pas non plus automatiquement les clauses de compétence juridictionnelle et de médiation sur le modèle français standard (voir `references/cgu-cgv.md`).

Détermine ensuite avec l'utilisateur ce qui s'applique réellement à son produit :

| Situation | Documents généralement nécessaires |
|---|---|
| Tout site/appli accessible au public en France ou visant le public français | Mentions légales |
| Le produit collecte des données personnelles (comptes, formulaires, analytics, cookies...) | Politique de confidentialité |
| Le produit dépose des cookies/traceurs non strictement nécessaires (analytics, pub, réseaux sociaux) | Politique de cookies (ou section dédiée dans la politique de confidentialité) |
| Le produit a des comptes utilisateurs, un service en ligne, une appli mobile | CGU (Conditions Générales d'Utilisation) |
| Le produit vend un bien, un service ou un abonnement payant | CGV — mais formule la conclusion inverse ("pas de vente identifiée à ce stade") avec la même prudence que le reste, une appli gratuite peut quand même créer une relation contractuelle avec CGU |
| L'utilisateur (ou son entreprise) traite des données personnelles **pour le compte** d'un client, traitement par traitement | DPA / accord de sous-traitance (art. 28 RGPD) |

Si l'utilisateur demande "les mentions légales" mais que son produit collecte manifestement des données, signale-lui qu'une politique de confidentialité est probablement aussi nécessaire, sans pour autant rédiger des documents non demandés sans confirmation.

## Étape 2 — Collecter les informations

Chaque type de document a sa checklist détaillée dans son fichier de référence (voir Étape 3). Pose les questions par lots logiques (identité de l'éditeur et hébergement d'abord, puis spécificités du document). Quand une information technique pourrait se déduire du nom d'un outil (Firebase, Stripe, Intercom...), ne la déduis pas : demande confirmation de ce qui est réellement activé/configuré plutôt que de supposer la configuration par défaut.

Informations transversales, utiles pour presque tous les documents : nom de l'entité et forme juridique, SIREN (qui sert aussi de numéro d'immatriculation RCS, au format `RCS [ville] [SIREN]`), ville du greffe d'immatriculation (à vérifier séparément, jamais déduite de l'adresse actuelle du siège — voir `references/mentions-legales.md`), adresse du siège, email de contact, nom du directeur de la publication, identité de l'hébergeur, existence d'un DPO désigné.

## Étape 3 — Rédiger à partir du bon gabarit

Lis le fichier de référence correspondant au(x) document(s) à produire — chacun contient la checklist d'informations, les mentions obligatoires, un gabarit à adapter, et les erreurs fréquentes propres à ce document (beaucoup viennent des deux pièges ci-dessus, appliqués à ce type de texte précis) :

- `references/mentions-legales.md` — mentions légales (LCEN art. 6-III)
- `references/politique-confidentialite.md` — politique de confidentialité RGPD (art. 13/14 RGPD, recommandations CNIL)
- `references/cookies.md` — politique de cookies / bandeau de consentement (recommandations CNIL)
- `references/cgu-cgv.md` — CGU et CGV (distinction, Code de la consommation)
- `references/dpa.md` — DPA / accord de sous-traitance (art. 28 RGPD)
- `references/audit.md` — méthode pour relire un document existant plutôt qu'en rédiger un nouveau

Adapte le ton et le niveau de détail au produit réel : une politique de confidentialité d'une appli qui ne collecte qu'un email n'a pas besoin des mêmes développements qu'un SaaS B2B qui traite des données sensibles.

## Étape 4 — Vérifier la cohérence et l'actualité

Avant de livrer, relis ce que tu as produit avec deux questions en tête : est-ce que des clauses ou des affirmations se contredisent entre elles ou avec un droit impératif du consommateur (ex: "aucun remboursement" alors que le droit de rétractation s'applique encore) ? Et est-ce que certaines affirmations dépendent d'une règle qui change dans le temps (plateforme de médiation européenne, règles Apple/Google, seuils réglementaires — y compris des seuils que tu cites toi-même comme des faits acquis, ex: âge de consentement numérique, plafonds de sanction) — si oui, dis-le au lieu de la présenter comme définitivement acquise.

Si plusieurs risques coexistent dans une même réponse (ex: données sensibles et mineurs, ou non-conformité déjà active aujourd'hui plutôt que théorique), ne les traite pas tous au même niveau : nomme explicitement, en priorité et avec la fermeté que la situation impose, le risque le plus significatif — ne le dilue pas dans une liste uniforme de points administratifs à confirmer.

## Étape 5 — Livrer : séparer le document des notes de production

Un document juridique publiable ne doit contenir que le texte juridique lui-même — pas de notes de production du type "informations manquantes à compléter avant publication" collées en fin de fichier, pas d'avertissement interne mélangé au texte. Structure toujours ta réponse en trois blocs distincts :

- **A. Le document** : le texte prêt à intégrer, avec des blancs explicites uniquement pour les données factuelles ponctuelles qui manquent (ex: `[email de contact à compléter]`).
- **B. Points à confirmer** : la liste des informations, durées, architectures ou qualifications que tu n'as pas pu établir — dans ta réponse à l'utilisateur, jamais dans le document.
- **C. Analyse / pourquoi** : tes explications, les risques identifiés, les alternatives — également hors du document.

Termine toujours par l'avertissement introductif ("Avertissement à transmettre systématiquement" ci-dessus). Livre le texte comme un fichier (Markdown ou Word — utilise le skill `docx` si demandé), sauf si l'utilisateur veut juste un aperçu dans le chat.

## Relecture d'un document existant

Si l'utilisateur demande un audit plutôt qu'une rédaction, lis `references/audit.md` avant de répondre : la méthode diffère (classification clause par clause, recherche systématique de contradictions) et ne consiste pas à réécrire tout le document.
