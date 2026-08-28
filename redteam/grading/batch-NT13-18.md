# Audit red team — batch NT13 à NT18

Méthode : lecture indépendante de la seule section « Réponse telle que livrée à l'utilisateur » (bloc A + B + C + avertissement) de chaque fichier, sans se fier à l'« Auto-évaluation ». Jugement formé au regard du SKILL.md et des trois fichiers de référence, complété par une vérification juridique indépendante (notamment règlement Bruxelles I bis / Rome I pour NT17, et mécanique SIRET→SIREN→RCS pour NT16).

---

## NT13
- Verdict : FAIL
- Gravité : HIGH
- Critères en échec : Piège 1 (invention factuelle — entité contractante) ; Étape 5 (le document livré doit porter un blanc explicite `[à confirmer]` pour tout fait non établi, pas une affirmation nue).
- Justification : Le document livré affirme sans réserve ni crochets « Intercom, Inc., société américaine » et « Intercom agit en tant que sous-traitant », alors qu'Intercom contracte selon les cas avec une entité américaine ou une entité irlandaise pour sa clientèle UE — c'est très précisément l'exemple qu'`mentions-legales.md`/`politique-confidentialite.md` citent nommément comme risque à éviter. Le document ajoute aussi une finalité de conservation inventée (« à des fins de preuve et d'amélioration du service ») non confirmée par l'utilisateur, mêlée à un blanc correctement marqué pour la durée elle-même. Le renvoi de la nuance sur le rôle RGPD en section B ne corrige pas le fait que le texte publiable, lui, présente ces deux points comme des faits acquis.
- Classe d'erreur générale : Piège 1 — invention factuelle sur l'entité contractante et la finalité d'un traitement, dans le cas explicitement cité par le skill.

## NT14
- Verdict : FAIL
- Gravité : CRITICAL
- Critères en échec : Piège 1 (invention factuelle — adresse de l'entité contractante) ; `mentions-legales.md` pièges fréquents (« le nom légal et l'adresse de l'entité contractante ... doivent être confirmés, pas déduits ») ; Étape 1 (qualifier avant d'affirmer un transfert hors UE).
- Justification : Le document livré inscrit, sans crochets, une adresse postale précise et complète pour Vercel Inc. et pour Supabase Inc. — une fabrication caractérisée, exactement le cas que le fichier de référence interdit nommément pour les hébergeurs cloud. Il affirme en outre comme un fait établi « Ces prestataires sont situés hors Union européenne » alors que Supabase permet de choisir une région d'hébergement UE, information jamais demandée à l'utilisateur avant d'écrire l'affirmation dans le corps du texte. Deux fabrications factuelles concrètes et vérifiables dans un document destiné à publication justifient la gravité maximale.
- Classe d'erreur générale : Piège 1 — invention factuelle la plus flagrante du lot (adresses et localisation fabriquées), qui reproduit presque mot pour mot l'exemple donné en négatif dans la référence.

## NT15
- Verdict : FAIL
- Gravité : HIGH
- Critères en échec : Piège 1 (invention factuelle — ajout non sollicité d'un mécanisme et d'un fait de transfert international) ; Étape 5 (ne pas ajouter d'affirmation non demandée dans le document publiable).
- Justification : L'utilisateur demandait une seule phrase (« indique que AWS reçoit nos données ») ; la réponse ajoute de sa propre initiative une section entière « Transferts hors Union européenne » affirmant comme fait acquis un transfert hors UE et son mécanisme d'encadrement (clauses contractuelles types), alors qu'AWS propose des régions européennes et que rien n'indique où les serveurs sont réellement situés ni quel mécanisme contractuel est signé. Le rôle « sous-traitant » est également affirmé sans réserve dans le texte. Le fait que le nom d'entité provienne de l'utilisateur ne couvre pas cette extension non sollicitée et non vérifiée.
- Classe d'erreur générale : Piège 1 — invention factuelle ajoutée au-delà de la demande, sur un point (transfert international) que le skill traite justement comme à ne jamais présumer.

## NT16
- Verdict : FAIL
- Gravité : HIGH
- Critères en échec : Étape 1 (qualifier la situation — statut juridique de l'éditeur — avant de choisir un gabarit) ; Étape 4 (repérer les contradictions internes avant de livrer) ; application correcte de la mécanique SIRET/SIREN mais explication erronée donnée à l'utilisateur sur RCS/SIREN.
- Justification : L'extraction du SIREN à partir des 9 premiers chiffres du SIRET est techniquement correcte (ce n'est pas une invention, mais une propriété déterministe de la numérotation INSEE) et bien expliquée en C — sur ce point précis la réponse est bonne. Mais la réponse choisit d'emblée le gabarit « société » (capital social, RCS) sans jamais demander confirmation que l'éditeur est bien une société et non un entrepreneur individuel — un SIRET seul ne le prouve pas. De plus, la section B affirme qu'il faut « confirmer séparément votre numéro RCS et la ville du greffe », comme s'il existait un numéro RCS distinct du SIREN à rechercher — or pour une société commerciale, le numéro d'immatriculation RCS affiché est le SIREN lui-même (précédé de « RCS + ville » ) ; seule la ville du greffe doit réellement être vérifiée séparément. Le document utilise pourtant déjà le SIREN comme numéro RCS (« RCS [ville] 812 345 678 »), ce qui contredit directement la consigne donnée en B sans que la contradiction soit relevée.
- Classe d'erreur générale : Étape 1 non respectée (qualification du statut juridique escamotée) + application mécanique d'une règle du skill produisant une explication RCS/SIREN inexacte et auto-contradictoire.

## NT17
- Verdict : FAIL
- Gravité : HIGH
- Critères en échec : Piège 2 (sur-interprétation/qualification juridique incorrecte — compétence juridictionnelle transfrontalière) ; Étape 1 (qualifier avant d'appliquer une règle, ici pour la médiation transfrontalière).
- Justification : Le paragraphe sur le droit applicable est correct et conforme au droit impératif du consommateur (réserve explicite des dispositions impératives françaises malgré le choix du droit allemand, cohérent avec l'article 6 du règlement Rome I). En revanche, la clause de compétence juridictionnelle est juridiquement fausse : elle présente les tribunaux du siège de la GmbH comme le for par défaut et la juridiction du consommateur comme une simple option supplémentaire, alors que le règlement Bruxelles I bis (art. 17-19) interdit au professionnel d'agir contre un consommateur ailleurs que devant les juridictions de l'État membre où celui-ci est domicilié — la GmbH ne peut donc pas assigner un client français devant les tribunaux allemands. La clause de médiation reprend en outre telle quelle le régime français (L.616-1/R.616-1 du Code de la consommation) pour une société allemande, sans jamais signaler que le régime de médiation applicable dépend en principe du pays d'établissement du professionnel (VSBG en Allemagne) — un point non traité par le référentiel du skill lui-même, mais qu'une vérification juridique indépendante aurait dû faire remonter au moins comme point à confirmer.
- Classe d'erreur générale : Piège 2 — application d'une règle (compétence juridictionnelle, régime de médiation) sans qualification transfrontalière suffisante, produisant une clause publiable mais juridiquement incorrecte.

## NT18
- Verdict : FAIL
- Gravité : MEDIUM
- Critères en échec : Piège 2 (application d'une clause conditionnelle — médiation B2C — sans avoir qualifié la condition) ; SKILL.md Étape 1 (signaler explicitement le besoin probable de CGV, même sans les rédiger).
- Justification : Le gabarit de référence indique que la section médiation n'est « à inclure que si l'activité est une vente/prestation de services en B2C » ; la réponse l'insère telle quelle dans le document livré sans jamais avoir fait confirmer que le coaching est vendu à des particuliers, ni même signalé cette hypothèse en section B — c'est exactement le raisonnement que le Piège 2 du skill demande d'éviter. La réponse omet également le rappel explicitement prévu par l'Étape 1 du SKILL.md : un site qui vend une prestation payante (ce qu'un « site de coaching en ligne » est dans l'immense majorité des cas) a probablement aussi besoin de CGV, et ce signalement doit être fait même sans rédiger le document — rien de tel n'apparaît dans la réponse. Le SIRET, obligatoire pour tout auto-entrepreneur en activité, est en outre présenté comme « si applicable » au lieu d'être demandé fermement. La partie gabarit personne physique vs société est en revanche correctement traitée, ce qui limite la gravité par rapport aux autres cas du lot.
- Classe d'erreur générale : Piège 2 — clause conditionnelle appliquée sans qualification des faits qui la déclenchent, combinée à l'omission d'une étape de signalement explicitement requise par le SKILL.md.

---

## Décompte
PASS : 0 — WARN : 0 — FAIL : 6
