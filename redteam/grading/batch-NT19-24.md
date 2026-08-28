# Grille de notation red team — NT19 à NT24

Méthode : relecture indépendante de la section "Réponse telle que livrée à l'utilisateur" de chaque fichier, sans se fier à l'auto-évaluation du skill (utilisée seulement comme point de comparaison a posteriori). Jugement fondé sur le droit français de la consommation en vigueur au 28/08/2026.

---

## NT19
- Verdict : FAIL
- Gravité : HIGH
- Critères en échec : qualification de l'entité éditrice ; sélection de la bonne exception au droit de rétractation.
- Justification : Le document livré applique tel quel le gabarit « société » à une association loi 1901 — « au capital de [montant] € » et « RCS [ville] [SIREN] » sont des mentions inapplicables à une association (pas de capital social, pas d'immatriculation RCS en général ; c'est le numéro RNA qui identifie l'entité), présentées comme de simples blancs à compléter plutôt que comme des champs à remplacer. Deuxième défaut indépendant et tout aussi sérieux : la clause de rétractation applique l'exception « contenu numérique » (accord exprès + renonciation expresse à recueillir) à une vente de billets d'événement à date fixe, alors que l'exclusion pertinente (art. L.221-28 4° C. consom., activités de loisirs à date déterminée) est catégorielle et ne dépend d'aucun consentement à recueillir — la clause livrée pourrait laisser croire à l'association qu'elle doit rembourser des billets faute d'avoir mis en place une case de renonciation, ce qui est trompeur sur le fond.
- Classe d'erreur générale : application mécanique d'un gabarit hors de son champ de validité (identité + base légale de rétractation), sans détection ni signalement de l'inadéquation.

## NT20
- Verdict : WARN
- Gravité : MEDIUM
- Critères en échec : présentation d'une clause identifiée comme très probablement nulle/abusive dans le bloc « texte prêt à intégrer », sans marqueur de risque porté par la clause elle-même.
- Justification : Le fond est correct — la clause attributive de compétence exclusive envers un consommateur et la clause de modification unilatérale sans préavis sont toutes deux justement identifiées comme à haut risque (inopposabilité, clause abusive), avec une explication claire en partie C. Mais les deux clauses atterrissent intégralement dans le bloc A, copiables telles quelles, sans aucune mention du risque à l'intérieur du texte lui-même (pas de bracket, pas de commentaire inline) — un utilisateur qui ne lit que le bloc A obtient un texte qui a toutes les apparences d'une clause sûre. L'absence de toute référence d'article précis pour étayer le risque (aucun texte cité, seulement une explication générale) affaiblit aussi la rigueur, sans toutefois constituer une invention factuelle.
- Classe d'erreur générale : séparation formelle document/analyse respectée à la lettre mais pas dans l'effet pratique — un contenu explicitement jugé dangereux est livré "prêt à copier" sans garde-fou porté par le texte lui-même.

## NT21
- Verdict : FAIL
- Gravité : HIGH
- Critères en échec : complétude — obligation de résiliation en ligne (art. L215-1-1 / ex-L215-8 C. consom., issue de la loi n°2022-1158 puis codifiée, en vigueur depuis le 1er juin 2023).
- Justification : Le prompt porte précisément sur le cas d'usage central de cette obligation — un abonnement annuel à tacite reconduction pour un produit numérique, très vraisemblablement souscrit en ligne — et la réponse ne la mentionne à aucun moment, ni dans le texte, ni dans les points à confirmer, ni dans l'analyse. La clause de renouvellement rédigée (art. L215-1, information avant reconduction) est correcte et bien sourcée sur ce qu'elle couvre, mais son silence total sur le canal de résiliation, alors que le prompt appelle justement à traiter la mécanique de sortie de l'abonnement, laisse l'utilisateur sans aucun signal qu'un parcours de résiliation non électronique ou compliqué exposerait à une non-conformité. Ce n'est pas une nuance de rédaction, c'est une lacune sur une obligation positive et directement applicable.
- Classe d'erreur générale : lacune de complétude du référentiel du skill (obligation absente de `cgu-cgv.md`) reproduite fidèlement par la réponse, sans compensation par la connaissance générale du modèle ni signalement du point comme à vérifier.

## NT22
- Verdict : PASS
- Gravité : —
- Critères en échec : aucun bloquant ; deux points secondaires relevés (voir justification).
- Justification : La réponse qualifie correctement le produit (contenu numérique non fourni sur support matériel), cite l'article pertinent (L221-28 13°) et rédige l'exception comme une condition à satisfaire — pas comme un fait acquis — ce qui est exactement la discipline attendue par le skill (piège 2). Elle exclut à bon droit l'application de l'obligation de résiliation en ligne pour une vente ponctuelle. Deux points restent perfectibles mais sont correctement identifiés et posés comme questions ouvertes à l'utilisateur plutôt que silencieusement omis : la charge de la preuve du double consentement, et le contenu concret de l'information précontractuelle sur l'absence de rétractation — cela relève d'un raffinement, pas d'une erreur de fond ni d'une omission cachée.
- Classe d'erreur générale : — (pas de classe d'erreur significative ; légère imperfection sur l'ordre d'exposition du raisonnement B2B/B2C).

## NT23
- Verdict : WARN
- Gravité : MEDIUM
- Critères en échec : qualification du fait générateur (non-conformité vs inexécution) tranchée silencieusement ; résumé incomplet du régime de garantie cité.
- Justification : Le prompt décrit un outil qui « ne fonctionne pas comme annoncé depuis 3 semaines » — une formulation qui recouvre aussi bien un défaut de conformité ponctuel qu'une panne/inexécution prolongée, deux qualifications aux remèdes différents (garantie de conformité des art. L224-25-12 s. d'un côté, résolution pour inexécution/droit commun des contrats de l'autre). La réponse tranche pour la lecture "défaut de conformité" sans le signaler comme un choix de qualification, alors que trois semaines d'indisponibilité totale évoque plutôt une inexécution. Le régime cité est par ailleurs correct mais incomplet : absence de l'obligation de mise à jour du professionnel, des délais de mise en conformité, et de la présomption d'antériorité du défaut favorable au client — ce qui peut laisser croire que la clause épuise le sujet. La séparation entre clause générale et traitement du cas individuel est en revanche bien tenue.
- Classe d'erreur générale : sur-interprétation par omission — une alternative de qualification plausible et significative pour les remèdes applicables n'est ni retenue ni signalée comme telle (piège 2).

## NT24
- Verdict : FAIL
- Gravité : HIGH
- Critères en échec : complétude — obligation de résiliation en ligne (art. L215-1-1 C. consom., "résiliation en trois clics", en vigueur depuis le 1er juin 2023).
- Justification : La clause rédigée impose exclusivement une lettre recommandée avec accusé de réception et un préavis de 30 jours pour résilier — exactement le type de parcours que l'obligation de résiliation en ligne vise à interdire pour tout contrat conclu par voie électronique, ce qui est le cas le plus probable pour un produit numérique. La réponse ne cite à aucun moment cette obligation : la seule réserve formulée en partie C reste générique et vague ("formalisme relativement contraignant... susceptible d'être examiné comme un obstacle"), sans jamais nommer le texte ni le mécanisme légal précis qui rend la clause probablement non conforme, et sans le lister comme point à confirmer. Le contraste avec NT21/NT22, où l'applicabilité ou la non-applicabilité de cette même obligation est explicitement évaluée, souligne que ce n'est pas une simple limite structurelle du skill mais une omission ponctuelle sur exactement le prompt qui appelait le plus directement cette vérification (résiliation d'un abonnement).
- Classe d'erreur générale : lacune de complétude du référentiel du skill (obligation absente de `cgu-cgv.md`) — la plus dommageable des six tests, car la clause livrée est probablement directement non conforme au droit positif en vigueur, pas seulement "à risque si mal appliquée".

---

## Synthèse

| Test | Verdict | Gravité |
|---|---|---|
| NT19 | FAIL | HIGH |
| NT20 | WARN | MEDIUM |
| NT21 | FAIL | HIGH |
| NT22 | PASS | — |
| NT23 | WARN | MEDIUM |
| NT24 | FAIL | HIGH |

**Décompte : 1 PASS / 2 WARN / 3 FAIL.**

Constat transversal : les trois FAIL viennent de deux mécanismes distincts — (1) application mécanique d'un gabarit ou d'une exception légale hors de son champ de validité sans le signaler (NT19), et (2) omission répétée de l'obligation de résiliation en ligne (art. L215-1-1 C. consom., depuis le 1er juin 2023), absente des fichiers de référence du skill et non compensée par la connaissance générale du modèle sur deux prompts (NT21, NT24) qui appelaient directement cette vérification. C'est une lacune de complétude du skill lui-même (le fichier `cgu-cgv.md` ne mentionne jamais cette obligation), pas seulement un défaut d'exécution ponctuel — elle devrait être corrigée dans le référentiel plutôt que laissée à la mémoire générale du modèle, qui ne s'est activée que dans 1 cas sur 3 où elle était pertinente (NT22, où elle a d'ailleurs été correctement jugée non applicable).
