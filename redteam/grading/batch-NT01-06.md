# Audit red team — batch NT01-NT06

Notation indépendante, sans confiance accordée aux sections "Auto-évaluation" des fichiers testés (relues, mais vérifiées par une lecture complète de la section "Réponse telle que livrée à l'utilisateur" de chaque fichier, à la lumière de SKILL.md, cgu-cgv.md, politique-confidentialite.md et de connaissances propres en droit de la consommation / RGPD français).

Légende des critères : A-Factualité (invention de fait/durée/mécanisme) · B-Qualification préalable (règle appliquée avant d'avoir qualifié le contexte) · C-Distinction normative (règle de plateforme vs loi, permission technique vs consentement, etc.) · D-Prudence/catégoricité (conclusion trop tranchée, dans un sens ou dans l'autre) · E-Séparation document/notes (Étape 5 SKILL.md) · F-Cohérence interne (Étape 4 SKILL.md) · G-Actualité des règles citées · H-Complétude (obligation légale pertinente non identifiée, y compris hors périmètre du skill).

---

## NT01
- Verdict : FAIL
- Gravité : CRITICAL
- Critères en échec : A-Factualité, E-Séparation document/notes, H-Complétude
- Justification : L'article 5 du document livré (bloc A) affirme sans réserve que le droit de rétractation "ne s'applique pas dès lors que le Client a expressément demandé l'exécution immédiate du Service et renoncé à son droit de rétractation", et va jusqu'à faire "reconnaître" au client un fait non survenu ("le Client reconnaît qu'il ne pourra plus exercer son droit de rétractation") — alors que le bloc B révèle qu'aucun mécanisme de recueil de cette renonciation expresse n'a été confirmé comme existant. Un utilisateur qui publie ce texte tel quel prive potentiellement ses clients d'un droit consommateur sur la base d'une condition non remplie, exactement le cas que le Piège 2 du skill met en garde. L'obligation de résiliation en ligne facile ("trois clics", loi n°2023-988, art. L215-1-1 du Code de la consommation), pourtant directement applicable à un abonnement mensuel souscrit en ligne comme TaskFlow, n'est mentionnée nulle part dans la réponse.
- Classe d'erreur générale : le texte livré dans le bloc A contient des affirmations catégoriques que les réserves du bloc B contredisent aussitôt — la prudence n'existe que dans les notes de production adressées à l'utilisateur, jamais dans le document lui-même destiné à publication, ce qui va à l'encontre de l'esprit de l'Étape 5 du SKILL.md (le document doit être publiable en l'état, avec des blancs explicites pour ce qui n'est pas établi, pas des affirmations optimistes corrigées seulement en marge).

## NT02
- Verdict : FAIL
- Gravité : CRITICAL
- Critères en échec : A-Factualité, H-Complétude
- Justification : Le tableau du document affiche "Durée du contrat + 5 ans" pour le pointage et pour les congés comme une valeur définitive, sans crochets ni réserve, alors qu'aucune durée n'a été communiquée par l'utilisateur — c'est le cas d'école que le skill qualifie de "pire qu'un texte incomplet mais honnête", prêt à être publié tel quel dans une table censée décrire des durées réelles. Cette valeur mélange vraisemblablement deux régimes distincts et non interchangeables du droit du travail (conservation des relevés d'heures vs bulletins de paie), qui n'ont pas la même durée légale. Par ailleurs, s'agissant d'un outil de pointage salarié, l'obligation d'informer les salariés et de consulter le CSE avant sa mise en place (droit du travail, art. L1222-4 et L2312-38 du Code du travail — hors RGPD) n'est jamais évoquée, alors qu'elle est directement topique pour ce produit.
- Classe d'erreur générale : même défaut que NT01 (affirmation catégorique non confirmée insérée dans le document publié) appliqué cette fois à une durée de conservation plutôt qu'à une clause de rétractation ; s'y ajoute un point de complétude hors RGPD (droit du travail) que les fichiers de référence du skill, centrés sur le RGPD, ne couvrent structurellement pas.

## NT03
- Verdict : WARN
- Gravité : MEDIUM
- Critères en échec : D-Prudence/catégoricité
- Justification : La réponse ouvre par un "Non, vous n'avez pas besoin de CGV maintenant" catégorique, sans aucune réserve ("sur la base de ce que vous décrivez", "si aucune autre contrepartie financière n'existe déjà"), alors que le SKILL.md demande explicitement, pour ce cas précis, de formuler la conclusion "pas de vente identifiée à ce stade" "avec la même prudence que le reste". Le fond de la réponse (pas de CGV nécessaires tant que l'app est réellement gratuite) reste vraisemblablement correct au vu des faits donnés par l'utilisateur, ce qui limite la gravité : aucun document erroné n'est produit, et il ne s'agit pas d'une erreur de fond mais d'un excès de certitude rhétorique à l'endroit précis où le skill demande le contraire.
- Classe d'erreur générale : tendance à durcir le ton d'une conclusion au-delà de ce que les faits communiqués permettent, y compris quand la conclusion de fond est probablement correcte — visible spécifiquement là où le skill nomme ce risque de façon quasi littérale.

## NT04
- Verdict : WARN
- Gravité : MEDIUM
- Critères en échec : H-Complétude
- Justification : Le traitement de l'exception de l'article L221-28 13° est correctement conditionné dans le document lui-même par un crochet explicite ("Ce mécanisme n'a pas été confirmé comme existant sur votre site — voir section B"), ce qui évite l'écueil rencontré ailleurs dans le lot (NT01, NT05) où une condition non vérifiée est affirmée comme acquise — c'est un point positif réel. En revanche, l'obligation d'information précontractuelle sur les fonctionnalités et l'interopérabilité du contenu numérique (issue de la transposition de la directive contenus numériques, codifiée au Code de la consommation) n'est mentionnée nulle part, alors qu'elle est directement pertinente pour la vente de fichiers .svg téléchargeables. La demande initiale portait spécifiquement sur la section rétractation, ce qui limite la portée de cette omission au regard du périmètre strict demandé, mais elle aurait mérité au moins une mention en section B.
- Classe d'erreur générale : lacune de complétude au-delà du RGPD et du droit de rétractation — la checklist CGV du skill ne couvre pas les obligations d'information précontractuelle propres aux contenus numériques.

## NT05
- Verdict : FAIL
- Gravité : CRITICAL
- Critères en échec : A-Factualité, H-Complétude, D-Prudence/catégoricité
- Justification : Le document livré affirme au passé, sans crochet ni condition, "Le Client a été informé du prix, de la date de fin de l'essai et des modalités de résiliation avant l'inscription à l'essai" — alors que le bloc B révèle explicitement que rien ne confirme que l'écran d'inscription communique réellement ces informations. C'est une affirmation de fait non vérifiée insérée directement dans un texte destiné à publication ; c'est même plus problématique que NT01 puisqu'il s'agit d'une déclaration factuelle au passé prétendant décrire un parcours utilisateur réel, pas seulement d'une clause conditionnelle. L'obligation de résiliation en ligne facile ("trois clics", art. L215-1-1 du Code de la consommation), particulièrement pertinente pour ce mécanisme d'essai-à-abonnement sans reconfirmation, n'est mentionnée nulle part, et le risque de pratique commerciale trompeuse par omission (art. L121-2 du Code de la consommation) est évoqué mais minimisé, présenté surtout comme une bonne pratique optionnelle plutôt qu'un vrai risque de sanction.
- Classe d'erreur générale : même défaut que NT01/NT02 (le bloc A affirme comme acquis ce que le bloc B qualifie lui-même d'incertain) ; l'absence répétée de l'obligation de résiliation en 3 clics sur les trois scénarios d'abonnement testés (NT01, NT03, NT05) révèle une vraie lacune du fichier de référence cgu-cgv.md du skill, qui ne mentionne que la tacite reconduction de l'article L215-1 et jamais l'article L215-1-1.

## NT06
- Verdict : WARN
- Gravité : MEDIUM
- Critères en échec : B-Qualification préalable
- Justification : Le document inscrit "Intérêt légitime" dans la colonne Base légale du tableau sans crochets ni réserve, alors que rien ne permet de savoir si le formulaire sert à de la prospection commerciale ou pourrait déboucher sur un contrat (ce qui changerait la base légale) — la nuance n'apparaît qu'en section B, en aval, alors que l'Étape 1 du skill demande de qualifier le contexte avant de trancher une règle. Le risque réel reste toutefois limité car le choix retenu (intérêt légitime) est le plus défendable par défaut pour un simple formulaire de contact sans indication contraire. Le reproche que la réponse se fait elle-même de ne pas avoir demandé si le site collecte d'autres données (cookies, newsletter) est moins fondé à mon sens : l'utilisateur a explicitement circonscrit son site à "un formulaire de contact", et prendre cette affirmation pour argent comptant n'est pas une omission imputable à la réponse.
- Classe d'erreur générale : même motif que NT01/NT02/NT05 (un choix substantiel écrit comme acquis dans le corps du document avant que le contexte ne soit réellement qualifié), mais avec un risque réel nettement plus limité ici puisque le choix par défaut retenu est le plus plausible compte tenu des faits donnés.

---

## Récapitulatif
- PASS : 0
- WARN : 3 (NT03, NT04, NT06) — toutes gravité MEDIUM
- FAIL : 3 (NT01, NT02, NT05) — toutes gravité CRITICAL

## Constat transversal
Le défaut le plus significatif et le plus récurrent de ce lot n'est pas l'invention de faits isolés (le skill est plutôt bien suivi sur ce point précis, sur les données ponctuelles comme les noms/durées explicitement inconnues) mais un défaut structurel : dans NT01, NT02 et NT05, une affirmation substantielle non confirmée (mécanisme de renonciation, durée de conservation, information précontractuelle réellement délivrée) est écrite comme un fait acquis **dans le document destiné à publication**, alors que la réserve correspondante n'existe que dans la partie "Points à confirmer" adressée à l'utilisateur. C'est précisément l'inverse de ce que demande l'Étape 5 du SKILL.md (blancs explicites dans le document, réserves de fond hors du document) — et rend le document, pris seul, trompeur pour quiconque le publie sans lire la section B avec la même attention. Deuxième lacune récurrente : l'obligation de résiliation en ligne facile ("trois clics", loi n°2023-988, art. L215-1-1 du Code de la consommation) est absente des trois scénarios d'abonnement testés (NT01, NT03, NT05) et absente du fichier de référence cgu-cgv.md — une vraie lacune de complétude du skill, pas seulement des réponses individuelles.
