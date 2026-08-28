# CGU et CGV

Ces deux documents sont souvent confondus mais répondent à des logiques différentes — clarifie toujours avec l'utilisateur lequel (ou lesquels) il lui faut réellement.

- **CGU (Conditions Générales d'Utilisation)** : régissent l'usage du service lui-même (compte, comportement attendu, contenu, propriété intellectuelle, résiliation). Pas d'obligation légale générale de les avoir, mais fortement recommandées dès qu'il y a un compte utilisateur ou un service en ligne, car c'est le contrat qui protège l'éditeur (règles d'usage, limitation de responsabilité, droit de suspendre un compte...).
- **CGV (Conditions Générales de Vente)** : régissent la **vente** d'un bien, service ou abonnement. Obligatoires en B2C dès qu'il y a vente à distance (article L221-5 et suivants du Code de la consommation) — leur absence ou leur non-conformité est sanctionnable. En B2B, les CGV sont obligatoires dès qu'un client professionnel le demande (article L441-1 du Code de commerce), même si elles n'ont pas à être publiées spontanément sur le site dans les mêmes conditions qu'en B2C.

Beaucoup de produits numériques ont besoin des deux dans un seul document ou deux documents séparés : un SaaS avec abonnement payant a des CGU (usage de la plateforme) et des CGV (l'abonnement lui-même, la facturation, la résiliation, le remboursement).

## Informations à collecter — CGU

- Description du service (à quoi sert la plateforme)
- Conditions d'accès (âge minimum, création de compte, vérification email...)
- Règles de comportement/contenu attendues (ce qui est interdit : contenu illicite, usage abusif, revente non autorisée...)
- Propriété intellectuelle : qui possède le contenu créé par l'utilisateur, quelle licence l'éditeur se réserve pour l'exploiter (héberger, afficher...)
- Modalités de suspension/résiliation de compte par l'éditeur, et par l'utilisateur
- Limitation de responsabilité (dans les limites permises par la loi — ne pas rédiger de clause qui exonérerait l'éditeur de ses obligations essentielles, ce serait nul)
- Droit applicable et juridiction compétente (souvent la loi française pour un éditeur français, sous réserve des règles impératives protectrices du consommateur pour un client B2C dans l'UE — signaler cette limite à l'utilisateur plutôt que rédiger une clause qui l'ignore). **Si l'éditeur lui-même n'est pas établi en France** mais vise des consommateurs français (société étrangère, notamment UE), ne calque pas automatiquement le for compétent sur le siège de l'éditeur ni le dispositif de médiation sur le modèle français : les règles européennes de compétence protectrices du consommateur permettent en principe à celui-ci d'agir devant les juridictions de son propre pays de résidence (et interdisent en principe au professionnel de l'attraire ailleurs), et le régime de médiation applicable dépend souvent du pays d'établissement du professionnel plutôt que de celui du consommateur — signale ces deux points comme nécessitant une vérification spécifique plutôt que d'appliquer le gabarit France standard.
- Modalités de modification des CGU (préavis, notification)

## Informations à collecter — CGV

- Description précise du bien/service/abonnement vendu, et son prix (TTC pour du B2C)
- Modalités de commande/souscription
- Modalités et moyens de paiement
- Durée de l'abonnement, conditions de renouvellement (tacite reconduction encadrée par l'article L215-1 du Code de la consommation pour le B2C : obligation d'informer le consommateur avant la date limite de dénonciation)
- Droit de rétractation : délai (14 jours par défaut en B2C pour la vente à distance), modalités d'exercice, exceptions. **Avant d'appliquer une exception, qualifie précisément ce qui est vendu** : un bien physique, un contenu numérique non fourni sur support matériel, un service numérique, un abonnement à un service, ou une combinaison — les conditions de l'exception "contenu numérique" (accord exprès du consommateur à l'exécution immédiate + renonciation expresse à son droit de rétractation, recueillis explicitement) ne s'appliquent qu'à certains cas précis et ne se déduisent pas automatiquement du fait qu'il s'agit d'un SaaS ou d'un produit numérique. Ce n'est pas non plus la seule exception possible : l'article L.221-28 du Code de la consommation en prévoit d'autres, distinctes et non interchangeables — notamment les prestations d'hébergement, de transport, de restauration ou de loisirs devant être fournies à une date ou une période déterminée (ex: billetterie d'un événement), exclues du droit de rétractation sans condition de renonciation expresse à recueillir. Ne plaque pas systématiquement l'exception "contenu numérique" sur toute vente numérique — vérifie d'abord si un autre cas de l'article L.221-28 correspond mieux.
- Modalités de résiliation — pour un contrat conclu par voie électronique avec un consommateur (cas très fréquent pour un produit numérique vendu en ligne), le droit français impose depuis le 1er juin 2023 une fonctionnalité de résiliation directement accessible en ligne, au moins aussi simple que la souscription (article L.215-1-1 du Code de la consommation, dite règle de la "résiliation en trois clics"). Une clause qui n'organise la résiliation que par un canal plus contraignant que la souscription (courrier recommandé exclusivement, par exemple) est à signaler comme un point de non-conformité probable, pas seulement comme un choix éditorial neutre — particulièrement pour un abonnement à tacite reconduction.
- Politique de remboursement
- Garanties légales applicables — ne les traite pas comme un bloc unique et interchangeable. Le régime des biens (garantie légale de conformité + vices cachés au sens classique) et celui des contenus/services numériques (garantie de conformité étendue aux contenus et services numériques depuis l'ordonnance de 2021) ne se recouvrent pas parfaitement : identifie ce qui est effectivement vendu avant d'énoncer quelle garantie précise s'applique. Dans tous les cas, ces garanties légales ne peuvent pas être supprimées par contrat en B2C.
- Médiation de la consommation (obligatoire en B2C) — si tu mentionnes une plateforme ou un dispositif européen de règlement en ligne des litiges, signale explicitement que son existence/URL doit être vérifiée à la date de rédaction, ce cadre évolue.

## Gabarit — structure commune

```markdown
# Conditions Générales d'Utilisation
(ou "Conditions Générales de Vente" / "Conditions Générales d'Utilisation et de Vente" selon le cas)

Dernière mise à jour : [date]

## 1. Objet
[Description du service et de ce que les présentes conditions régissent.]

## 2. Acceptation
[Comment l'utilisateur/client accepte les conditions — décris le mécanisme réellement en place (case à cocher, création de compte...) uniquement si l'utilisateur te l'a confirmé. S'il ne l'a pas précisé, ne décris pas un mécanisme comme existant : indique-le comme point à confirmer, et si tu recommandes une case à cocher explicite au moment de la souscription plutôt qu'une acceptation implicite, présente-le clairement comme une recommandation, pas comme une description de l'existant.]

## 3. Accès au service / Compte utilisateur
[Conditions d'accès, création et sécurité du compte.]

## 4. [Si CGV] Commande, prix et paiement
[Modalités.]

## 5. [Si CGV] Droit de rétractation
[Délai, modalités, exceptions applicables au service concerné.]

## 6. Règles d'usage
[Ce qui est interdit, comportements attendus.]

## 7. Propriété intellectuelle
[Répartition des droits sur le contenu de la plateforme et le contenu généré par l'utilisateur.]

## 8. [Si CGV] Résiliation et remboursement
[Modalités.]

## 9. Responsabilité
[Limitation dans les limites légalement permises.]

## 10. Données personnelles
Voir notre [Politique de confidentialité](lien).

## 11. Droit applicable et litiges
[Droit français, juridiction compétente, médiation de la consommation si B2C.]

## 12. Modification des conditions
[Modalités de notification en cas de changement — distingue si besoin une modification des CGV elles-mêmes, un changement de prix, une évolution du service, une modification imposée par la loi, et une modification substantielle qui justifierait un droit de résiliation sans frais : ce ne sont pas nécessairement la même procédure, ne les traite pas comme un bloc unique.]
```

## Pièges fréquents
- Rédiger une clause de résiliation qui n'offre qu'un canal contraignant (courrier recommandé, appel téléphonique uniquement) pour un contrat souscrit en ligne par un consommateur, sans signaler l'obligation de résiliation facilitée en ligne (art. L.215-1-1 du Code de la consommation, en vigueur depuis juin 2023) — vérifie ce point à chaque clause de résiliation ou de tacite reconduction rédigée pour un abonnement B2C conclu par voie électronique.
- Rédiger une clause de responsabilité qui exclut totalement l'éditeur — les clauses abusives sont réputées non écrites en B2C, et certaines clauses limitatives de responsabilité pour faute lourde/dol sont nulles en B2B aussi.
- Affirmer que le droit de rétractation est écarté pour un SaaS/contenu numérique sans avoir vérifié que les conditions précises de l'exception sont réunies (accord exprès + renonciation expresse) — voir la remarque dans la checklist CGV ci-dessus.
- Confondre B2B et B2C dans un même document sans distinguer les règles qui s'appliquent différemment (rétractation, clauses abusives, garanties).
- Ne pas aligner les CGV avec ce qui est réellement configuré dans l'outil de facturation (Stripe, etc.) — demander à l'utilisateur de vérifier la cohérence des durées d'essai, de préavis, de remboursement plutôt que d'inventer ces valeurs.
- Traiter toute clause de "modification des conditions" comme relevant d'une seule et même règle — voir la note dans le gabarit, distingue le type de modification en jeu.
- Livrer un document qui mélange le texte juridique avec des notes de production ("à compléter", commentaires de rédaction) — garde ces notes dans ta réponse, pas dans le fichier final (voir Étape 5 du SKILL.md).
