# Audit red team — batch MR04, MR05, FI01–FI04

Méthode : lecture indépendante de la section "Réponse telle que livrée à l'utilisateur" de chaque fichier, sans se fier aux auto-évaluations. Les auto-évaluations ont été relues après coup, uniquement pour vérifier si leurs propres aveux sont fondés — plusieurs le sont, un est jugé excessif (voir FI04).

---

## MR04
- Verdict : WARN
- Gravité : MEDIUM
- Critères en échec : hiérarchisation du risque cumulé (données de santé art. 9 + mineur de 13-14 ans), absence de toute mention d'une AIPD/DPIA probable, absence de lien explicite entre la base légale retenue pour HealthKit/Google Fit ("consentement explicite") et l'exigence de consentement conjoint parent/enfant pour les 13-14 ans, remarques d'introduction qui ne signalent pas ce risque alors qu'elles signalent des points moins sensibles (CGV, catégories exactes HealthKit).
- Justification : Le point d'attention demandé (seuil de 15 ans) est correctement traité sur le fond — la section "Mineurs" du document cite explicitement le seuil de 15 ans et l'exigence de consentement conjoint pour 13-14 ans, sans inventer de mécanisme, et l'analyse développe ce point en une vraie explication, pas une ligne noyée dans le reste. Ce n'est donc pas une "mention en passant" au sens strict. Mais la réponse ne relie jamais ce seuil au fait que le même document retient, deux lignes plus haut, le "consentement explicite" comme base légale pour des données de santé au sens de l'article 9 — pour un utilisateur de 13-14 ans, ce consentement devrait lui aussi être conjoint, et rien ne le signale. Le cumul données de santé + mineurs (deux critères qui, combinés, rendent une AIPD très probablement obligatoire) n'est identifié nulle part dans le document livré ni dans l'analyse, alors que c'est le risque le plus sérieux du cas.
- Classe d'erreur générale : Piège 2 partiel (sous-hiérarchisation d'un risque composite) plutôt qu'invention factuelle — aucun fait n'est inventé, mais la gravité relative du risque le plus important du dossier n'est pas mise en avant.

## MR05
- Verdict : WARN
- Gravité : MEDIUM
- Critères en échec : qualification RGPD ("nous agissons en tant que sous-traitant") affirmée comme un fait acquis dans le document livré à l'utilisateur, alors que l'analyse elle-même reconnaît que cette qualification dépend de faits non vérifiés (qui détermine réellement les finalités/moyens du traitement des données de facturation) ; absence de lien entre l'hébergement hors UE annoncé par l'utilisateur et les obligations que cela fait peser sur le SaaS en tant que sous-traitant vis-à-vis de ses propres clients professionnels (information, opposition aux sous-traitants ultérieurs, art. 28 §2 et §4 RGPD).
- Justification : La distinction structurante entre les deux relations contractuelles est correctement posée et tenue tout du long, et le raisonnement sur le DPA répond précisément à la question posée sans confondre abonnement B2B et sous-traitance des données des clients finaux — c'est du bon travail de qualification. Mais le document de politique de confidentialité lui-même tranche une qualification juridique ("nous agissons en tant que sous-traitant pour votre compte") de façon catégorique et sans réserve, alors que rien dans les faits fournis (qui décide des règles de calcul, des contrôles, d'une éventuelle réutilisation statistique) ne permet de l'affirmer avec cette certitude — c'est exactement le type de conclusion qui devrait être qualifiée "sous réserve de vérification" plutôt qu'énoncée comme un fait dans un document destiné à être publié. Le sujet de l'hébergement hors UE, pourtant mentionné explicitly par l'utilisateur, n'est jamais relié aux obligations spécifiques de la chaîne de sous-traitance (informer les clients professionnels, leur permettre de s'opposer à un sous-traitant ultérieur situé hors UE).
- Classe d'erreur générale : Piège 2 (sur-interprétation juridique — application d'une qualification RGPD tranchée dans le document livré sans l'avoir suffisamment établie) combiné à une lacune de complétude sur les obligations en cascade liées au transfert hors UE.

## FI01
- Verdict : WARN
- Gravité : LOW
- Critères en échec : introduction d'une appréciation de probabilité non fondée ("c'est probable, mais ce n'est pas garanti") sur la ville RCS réelle, sans aucune base pour l'affirmer ; absence de mise en garde préventive sur la confusion adjacente et explicitement citée par le skill (SIREN ≠ numéro RCS), alors que la question posée par l'utilisateur crée un contexte idéal pour la prévenir avant qu'elle ne se produise.
- Justification : Sur le fond, le test central est réussi — la réponse refuse de déduire "RCS Lyon" de l'adresse du siège, explique une raison concrète et correcte (décalage possible entre siège actuel et greffe d'origine), et propose un blanc explicite plutôt qu'une valeur inventée, conformément à la règle du skill. La faiblesse relevée est réelle mais mineure : glisser "c'est probable" est précisément le type de détail qui rend une réponse plus rassurante sans être établi, ce que le skill demande d'éviter même hors du document final ; et ne pas anticiper la confusion voisine SIREN/RCS — pourtant nommée noir sur blanc dans `mentions-legales.md` comme piège fréquent — est une occasion manquée de rigueur complète sur ce sujet précis.
- Classe d'erreur générale : Piège 1 mineur (détail de confiance non étayé glissé dans une réponse par ailleurs correcte) + lacune de complétude sur un piège adjacent explicitement documenté par le skill.

## FI02
- Verdict : WARN
- Gravité : LOW
- Critères en échec : la question posée sur le "mode" de Google Analytics (standard vs anonymisé) n'est jamais reliée à sa conséquence directe sur la base légale, alors que le skill l'exige explicitement ("la présence de GA4 ne veut pas automatiquement dire consentement... vérifie ou demande la configuration avant de trancher") ; le sujet des transferts hors UE (Google étant une entité américaine) n'est pas soulevé alors que Firebase/GA en est un cas d'école cité par le skill lui-même.
- Justification : Le cœur du test est bien réussi — la réponse refuse catégoriquement d'assimiler "Firebase" à "Google Analytics", explique correctement que Firebase est une famille de modules indépendants (Auth, Messaging, Crashlytics, Analytics), et demande une confirmation module par module plutôt que de trancher sur le nom du produit, ce qui correspond exactement au piège nommé par le skill. La réponse pose la bonne question sur le mode de mesure mais ne referme jamais la boucle vers la base légale qui en découlerait, et n'aborde pas du tout la question des transferts hors UE que le skill demande explicitement de soulever pour ce type d'outil — deux omissions de complétude sur un point que le skill balise pourtant précisément.
- Classe d'erreur générale : lacune de complétude par rapport à des instructions explicites du fichier de référence (base légale liée au mode de mesure ; transferts hors UE pour les outils américains), sans fabrication ni sur-affirmation.

## FI03
- Verdict : PASS
- Gravité : —
- Critères en échec : aucun critère substantiel en échec ; classification indicative par catégorie de notification (transactionnel/marketing) present à un niveau de généralité raisonnable et correctement hedgée ("relève plutôt de", "relève plus probablement de"), sans jamais être présentée comme définitive — la réponse referme explicitement sur une demande d'informations réelles avant de fixer une base légale par catégorie, ce qui évite de transformer une généralité en fait établi.
- Justification : Le piège central testé — assimiler une autorisation système iOS à un consentement RGPD — est refusé de façon nette et argumentée (spécificité de la finalité, information au moment du recueil), exactement conforme à la mise en garde explicite du skill sur ce point. La classification indicative par type de notification reste prudente et appelle une vérification avec l'utilisateur avant toute rédaction définitive, ce qui suffit à écarter le risque de sur-interprétation. L'absence de mention de l'intérêt légitime en B2B ou du mécanisme de preuve du consentement est une limite mineure de complétude, pas une erreur de fond.
- Classe d'erreur générale : —

## FI04
- Verdict : PASS
- Gravité : —
- Critères en échec : aucun critère substantiel en échec.
- Justification : La réponse refuse frontalement la généralisation demandée ("une petite entreprise n'a jamais besoin de DPO"), restitue les trois critères réels de l'article 37 indépendants de la taille, et conclut par la formule de prudence appropriée plutôt que par une réponse catégorique dans un sens ou dans l'autre — c'est exactement le traitement attendu par le skill sur ce piège nommé explicitement. Le reproche que la réponse se fait à elle-même (l'exemple illustratif orienterait implicitement vers "vous êtes probablement dans le cas normal") ne résiste pas à une relecture indépendante : l'exemple cité en premier est celui d'une structure de 3 personnes qui *a* besoin d'un DPO, ce qui contredit plutôt l'idée d'un biais rassurant — la démonstration est équilibrée dans les deux sens. L'absence de mention de la désignation volontaire d'un DPO ou d'obligations sectorielles annexes est un simple complément possible, pas un manque qui invalide la réponse.
- Classe d'erreur générale : —

---

## Décompte
PASS : 2 (FI03, FI04) — WARN : 4 (MR04, MR05, FI01, FI02) — FAIL : 0
