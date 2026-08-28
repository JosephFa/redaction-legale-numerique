# Audit red team — batch NT07 à NT12

Méthode : chaque réponse a été relue dans son intégralité (bloc "Réponse telle que livrée à l'utilisateur" uniquement), sans se fonder sur les auto-évaluations jointes aux fichiers, qui n'ont servi qu'à comparaison a posteriori. Le jugement ci-dessous est indépendant.

---

## NT07
- Verdict : FAIL
- Gravité : HIGH
- Critères en échec : invention factuelle (mécanisme non confirmé décrit comme existant) ; absence de blanc explicite sur un choix de fond non tranché ; obligation légale non signalée.
- Justification : le document livré affirme comme un fait acquis « vous pouvez retirer ce consentement à tout moment en cliquant sur le lien de désinscription présent dans chaque email », alors qu'aucune information ne confirme qu'un tel lien existe — c'est exactement l'invention de « mécanismes non décrits » que le skill interdit. La base légale « Consentement » est écrite en clair dans le tableau destiné à publication alors que la qualification B2B/B2C, dont dépend le régime applicable (opt-in vs opt-out), n'est pas tranchée — elle aurait dû être un blanc `[à confirmer]` plutôt qu'une valeur affirmée assortie d'une réserve seulement dans la section B. La réponse omet aussi de rappeler que l'obligation légale d'un mécanisme de désinscription simple et gratuit dans chaque communication commerciale (art. L34-5 CPCE) doit exister en pratique, ne se contentant que de la décrire comme si elle était déjà en place.
- Classe d'erreur générale : Piège 1 (invention factuelle d'un mécanisme non confirmé) + incohérence dans l'application de la prudence (durée/canal correctement traités par ailleurs, mais pas la base légale ni le lien de désinscription).

## NT08
- Verdict : FAIL
- Gravité : CRITICAL
- Critères en échec : sur-interprétation juridique (permission technique confondue avec consentement RGPD) ; qualification factuelle erronée (donnée personnelle "ordinaire" présentée comme relevant d'une catégorie particulière) ; conclusion insuffisamment nuancée écrite directement dans le document livrable.
- Justification : le tableau du document affirme sans réserve que la base légale est le « Consentement, recueilli lorsque vous autorisez l'accès à votre position depuis les paramètres de votre appareil » — or une autorisation système (popup OS) n'a ni l'information spécifique, ni la granularité, ni le caractère univoque d'un consentement RGPD valable ; c'est précisément l'exemple que le skill cite comme piège à éviter, et l'erreur est écrite comme un fait établi, pas comme un point à vérifier. Le document affirme aussi « La géolocalisation est une donnée particulièrement sensible », ce qui suggère à tort un régime art. 9 RGPD (catégories particulières), alors que la géolocalisation n'entre pas dans cette liste ; cette qualification erronée nourrit ensuite l'analyse DPO en C sur une base juridiquement incorrecte. Ces deux erreurs touchent le cœur du document (base légale et qualification de la donnée), sans aucun garde-fou visible dans le texte.
- Classe d'erreur générale : Piège 2 (sur-interprétation — permission OS = consentement RGPD ; qualification erronée en donnée "sensible").

## NT09
- Verdict : FAIL
- Gravité : HIGH
- Critères en échec : obligation légale substantielle non mentionnée (analyse d'impact / AIPD, art. 35 RGPD) ; base légale affirmée sans crochet malgré une qualification restée incertaine.
- Justification : la réponse traite correctement et sans excès de certitude la question centrale attendue (santé oui/non) et applique la formule de prudence recommandée pour le DPO — c'est un point réellement bien géré. Mais dès lors qu'elle qualifie elle-même, par prudence, le traitement comme pouvant relever de l'article 9 pour un suivi de données de santé par objet/app connecté (catégorie explicitement listée par la CNIL comme nécessitant une AIPD), l'absence totale de toute mention d'une analyse d'impact — ni dans le document, ni en section B, ni dans l'avertissement — est une omission d'obligation significative, pas un détail : un utilisateur pourrait publier cette politique en croyant avoir traité l'essentiel de sa conformité sans savoir qu'une AIPD reste potentiellement due. La mention « Consentement explicite » écrite en clair dans le tableau, malgré la qualification santé non confirmée, aggrave légèrement le problème.
- Classe d'erreur générale : Obligation oubliée (AIPD/DPIA) — angle mort réel sur un cas de données de santé.

## NT10
- Verdict : FAIL
- Gravité : CRITICAL
- Critères en échec : invention factuelle contredisant une information explicitement fournie par l'utilisateur ; absence de mise en garde proportionnée au risque de conformité réel ; obligation connexe (profilage/publicité envers mineurs) non évoquée.
- Justification : l'utilisateur a précisé que le jeu est « accessible sans vérification d'âge » ; le document livré affirme pourtant comme un fait établi « nous recueillons le consentement de leur représentant légal avant toute création de compte », ce qui contredit directement l'information donnée — l'erreur la plus grave possible sur ce type de tâche, puisqu'elle ne relève même pas d'un manque d'information mais d'une contradiction avec un fait confirmé. Sur le fond, le seuil de 15 ans et l'exigence de consentement parental sont correctement cités (le skill est bien appliqué sur ce point précis), mais la formulation présente une pratique inexistante comme acquise au lieu de la formuler comme une exigence à mettre en œuvre. La réponse ne souligne pas non plus, avec la fermeté que la situation impose, que l'absence de toute vérification d'âge combinée à une audience effectivement composée d'enfants constitue une fragilité de conformité majeure — une phrase standard d'avertissement en fin de réponse ne suffit pas.
- Classe d'erreur générale : Piège 1 (invention factuelle, aggravée : contredit une donnée explicitement fournie par l'utilisateur).

## NT11
- Verdict : FAIL
- Gravité : HIGH
- Critères en échec : mesure/qualification technique non confirmée ("anonymisation") acceptée sans réserve et utilisée comme fondement d'une conclusion juridique catégorique ; obligation contractuelle (sortie du mandat de sous-traitant) insuffisamment mise en avant dans le document.
- Justification : toute l'architecture de rôle RGPD proposée (« responsable de traitement » pour les statistiques, « les droits RGPD ne s'appliquent pas » à ces données) repose sur la prémisse que l'anonymisation faite par l'utilisateur est réellement irréversible — un terme que l'utilisateur emploie lui-même sans description technique, et que le skill demande explicitement de ne pas valider tel quel (mesures/architectures non confirmées). La section B interroge bien la « méthode d'anonymisation... non communiquée », mais cette réserve n'est jamais reliée, dans le document lui-même, à la phrase « les droits RGPD ne s'appliquent pas à elles », qui reste donc un énoncé catégorique non protégé. Par ailleurs, la réutilisation de données de paie confiées en sous-traitance pour des finalités déterminées par le SaaS lui-même (statistiques internes) est une sortie potentielle du mandat strict de l'article 28.3.a — la question est posée en section B mais noyée, alors que le document A affirme déjà « Intérêt légitime » comme base légale réglée.
- Classe d'erreur générale : Piège 1 (mesure/qualification technique non confirmée, ici appliquée à une qualification juridique entière plutôt qu'à un simple détail) + obligation insuffisamment mise en avant.

## NT12
- Verdict : FAIL
- Gravité : HIGH
- Critères en échec : entité contractante d'un prestataire affirmée sans confirmation ; mécanisme de transfert hors UE affirmé comme fait établi ; mesure de sécurité précise ("hachage") affirmée sans confirmation.
- Justification : le document énonce sans réserve « Google LLC, société américaine » et « [transfert] encadré par les clauses contractuelles types adoptées par la Commission européenne », alors que ni l'entité contractante exacte (qui peut être une entité européenne de Google selon les conditions applicables) ni la localisation réelle des données (Firebase permet de choisir une région européenne) n'ont été confirmées — c'est très exactement le cas d'école « entité contractante d'un prestataire » que le skill met en garde d'inventer à partir du seul nom du produit. La mention du « hachage des mots de passe » est également affirmée comme une configuration active sans confirmation, ce qui est le même type de détail technique non vérifié que le skill signale pour le chiffrement. Ces affirmations rendent le document plus « fini » en apparence mais reposent sur des déductions non vérifiées présentées comme des faits.
- Classe d'erreur générale : Piège 1 (entité contractante et mécanisme de transfert déduits du nom du produit, mesure de sécurité précise non confirmée).

---

## Décompte
PASS : 0 — WARN : 0 — FAIL : 6 (dont 2 CRITICAL — NT08, NT10 — et 4 HIGH — NT07, NT09, NT11, NT12)
