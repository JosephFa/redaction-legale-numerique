# COH02 — cohérence des durées de conservation

## Prompt testé

« Rédige la politique de confidentialité (les données de facturation sont conservées 'durée du compte + 1 an') et les CGV (dans lesquelles les données de facturation doivent être conservées '10 ans pour raisons comptables') de notre SaaS, en une seule réponse. »

## Réponse telle que livrée à l'utilisateur

Avant les deux documents, un point m'arrête et je préfère vous le signaler tout de suite plutôt que de rédiger les deux textes sans réagir : vous me donnez deux durées différentes pour la même catégorie de données ("données de facturation") — "durée du compte + 1 an" pour la politique de confidentialité, et "10 ans pour raisons comptables" pour les CGV. Si ces deux durées visaient réellement la même chose, les documents se contrediraient une fois publiés côte à côte. Je vois deux lectures possibles, mais je ne tranche pas à votre place :

1. **Les deux durées visent en réalité deux choses différentes** : "durée du compte + 1 an" pour le profil de facturation du client dans votre outil (adresse de facturation, moyen de paiement enregistré, historique visible dans son espace client), et "10 ans" pour les pièces comptables à proprement parler (factures émises, justificatifs) que vous devez conserver au titre de vos propres obligations comptables (l'article L.123-22 du Code de commerce prévoit une conservation de 10 ans des documents comptables, ce qui rend ce chiffre plausible pour cet usage précis). Dans ce cas, il faut le dire explicitement dans chaque document, avec deux lignes distinctes, pas une seule ligne "données de facturation" par document.
2. **Il s'agit bien de la même donnée et l'une des deux durées est une erreur** à corriger avant publication.

Je rédige les deux documents ci-dessous **en reprenant telles quelles les deux durées que vous m'avez données**, chacune dans son document, plutôt que d'en choisir une à votre place ou de les fusionner silencieusement — mais je vous signale que cette contradiction doit être résolue avant toute publication, sans quoi vos deux documents affichent publiquement deux règles différentes pour ce qui apparaît, à première lecture, comme la même catégorie de données.

### A. Les documents

```markdown
# Politique de confidentialité

Dernière mise à jour : [date]

## Qui sommes-nous
[Nom de l'entité], SIREN [à compléter], [adresse à compléter], est responsable du traitement des données décrites ci-dessous.
Contact : [email dédié protection des données à compléter]
[Délégué à la Protection des Données (DPO) : existence à confirmer — voir points à confirmer]

## Quelles données nous collectons et pourquoi

| Finalité | Données concernées | Base légale | Durée de conservation |
|---|---|---|---|
| Création et gestion du compte | [données à compléter] | Exécution du contrat | [durée à compléter] |
| Gestion de l'abonnement et facturation | Données de facturation (adresse de facturation, moyen de paiement enregistré, historique visible dans l'espace client) | Exécution du contrat | Durée du compte + 1 an |
| ... | ... | ... | ... |

## Avec qui nous partageons vos données
[Prestataires réellement utilisés — à compléter, ex: prestataire de paiement.]

## Transferts hors Union européenne
[À compléter selon les outils réellement utilisés.]

## Vos droits
Vous disposez des droits suivants sur vos données : accès, rectification, effacement, limitation, portabilité, opposition, et retrait du consentement à tout moment (l'exercice de certains de ces droits dépend de la base légale du traitement concerné). Pour les exercer, contactez-nous à [email]. Nous répondrons dans un délai d'un mois, pouvant être prolongé de deux mois supplémentaires en cas de demande complexe (art. 12 RGPD).
Vous pouvez également introduire une réclamation auprès de la CNIL (www.cnil.fr).

## Sécurité
[Mesures de sécurité en place, en termes généraux — à compléter.]

## Modifications
Cette politique peut être mise à jour ; la date de dernière modification figure en haut de ce document.
```

```markdown
# Conditions Générales de Vente

Dernière mise à jour : [date]

## 1. Objet
[Description du service et de l'abonnement, édité par [Nom de l'entité], SIREN [à compléter].]

## 2. Prix et paiement
[Modalités à compléter.]

## 3. Durée, renouvellement
[À compléter.]

## 4. Droit de rétractation
[Qualification B2B/B2C non précisée — à compléter.]

## 5. Résiliation et remboursement
[Modalités à compléter.]

## 6. Conservation des données de facturation à des fins comptables
Conformément à nos obligations légales en matière comptable, les données de facturation (factures émises, justificatifs comptables) sont conservées pendant une durée de 10 ans à compter de leur émission, indépendamment de la durée pendant laquelle le compte client reste actif.

## 7. Garanties légales
[À compléter selon la nature exacte du service — voir référence CGU/CGV.]

## 8. Droit applicable et litiges
[À compléter.]
```

### B. Points à confirmer

- **Contradiction à trancher avant publication** : "durée du compte + 1 an" (politique de confidentialité) et "10 ans" (CGV) sont-elles deux durées pour deux catégories différentes de données de facturation (profil client vs pièces comptables), ou la même donnée avec deux valeurs incompatibles ? Les deux documents ci-dessus reprennent chacun la durée que vous m'avez donnée, avec une tentative de délimiter à quoi elle s'applique (voir la reformulation "profil de facturation" / "pièces comptables") — mais cette délimitation est une hypothèse de ma part, pas une confirmation de votre part, et elle doit être validée ou corrigée avant que ces deux textes coexistent publiquement.
- Identité complète de l'éditeur (dénomination, forme juridique, SIREN, adresse, email de contact) — rien n'a été fourni, tout est en blanc dans les documents.
- B2B ou B2C — non précisé, alors que cela conditionne le droit de rétractation et la clause de médiation de la consommation dans les CGV.
- Prestataires réellement utilisés pour le paiement et la facturation.
- Autres finalités de traitement (compte, statistiques...) non détaillées ici, l'échange portant principalement sur la conservation des données de facturation.

### C. Analyse / pourquoi

Je n'ai pas fusionné les deux durées ni choisi arbitrairement laquelle des deux documents devait céder devant l'autre : le skill demande de vérifier la cohérence entre documents avant de livrer, pas de la corriger silencieusement à la place de l'utilisateur quand la correction suppose de trancher une question de fond (ici, la définition exacte de ce que recouvre "données de facturation" dans chaque contexte). J'ai proposé une lecture qui rendrait les deux durées compatibles (profil client vs pièces comptables), parce que 10 ans correspond à une durée connue en droit comptable français (art. L.123-22 du Code de commerce) et qu'il est donc plausible que les deux durées visent des réalités différentes plutôt que de se contredire — mais je présente ça comme une hypothèse à confirmer, pas comme un fait établi, puisque vous ne me l'avez pas précisé.

---

Ces documents sont une base rédigée à partir des exigences légales en vigueur, pas un avis juridique personnalisé. Une relecture par un avocat ou un DPO est recommandée avant publication — en particulier ici, où la contradiction relevée entre les deux durées doit être résolue avant toute mise en ligne. Ces textes devront être mis à jour si votre activité ou vos traitements de données évoluent.

## Auto-évaluation

La question posée est simple : la réponse a-t-elle relevé la contradiction entre les deux durées de conservation des données de facturation, ou l'a-t-elle laissée passer sans réaction ?

**Verdict : la contradiction est relevée**, et pas seulement en passant. Elle est signalée avant même la rédaction des documents (premier paragraphe de la réponse), reprise explicitement en section B comme un point à trancher "avant publication", et une tentative de conciliation est proposée (distinction profil de facturation / pièces comptables) tout en la présentant comme une hypothèse et non comme un fait acquis. C'est exactement le réflexe que l'Étape 4 du skill demande : vérifier si des affirmations se contredisent entre documents avant de livrer.

Deux réserves, cependant, à l'examen honnête de ce qui a été réellement livré :

1. **La contradiction est signalée dans la réponse, mais elle n'est pas neutralisée dans les documents eux-mêmes.** Le document A (politique de confidentialité) affirme, sans aucun crochet ni réserve, "Durée du compte + 1 an" pour les données de facturation ; le document CGV affirme, tout aussi sèchement, "10 ans à compter de leur émission" pour ce qui est décrit comme "données de facturation". Si l'utilisateur ne lit que les documents et les publie tels quels — ce qui est un risque réel puisque c'est exactement ce qu'il a demandé ("rédige... en une seule réponse") — les deux textes se contredisent bel et bien en ligne, malgré la reformulation ("profil de facturation" vs "pièces comptables") que j'ai glissée dans chaque tableau/clause pour tenter de les rendre compatibles. Cette reformulation atténue le problème pour un lecteur attentif, mais elle ne le résout pas : rien dans le texte publié n'indique explicitement que ces deux durées sont volontairement différentes plutôt que contradictoires, en dehors de la réponse à l'utilisateur — qui, par construction, n'est pas dans le document. C'est la même tension déjà identifiée sur d'autres cas de ce skill : signaler un problème dans la réponse ne suffit pas si le document livré, lu seul, continue d'affirmer sans réserve une clause qui n'a de sens que grâce à une hypothèse non confirmée.
2. **La distinction "profil de facturation" / "pièces comptables" est une invention de structure, pas seulement une invention de durée.** Le skill met en garde contre l'invention de durées non fournies — je n'ai inventé aucun chiffre, les deux durées viennent de l'utilisateur. Mais j'ai inventé la catégorisation qui les rend compatibles (deux sous-catégories de "données de facturation" que l'utilisateur n'a jamais distinguées lui-même) et je l'ai fait figurer dans le texte des deux documents (pas seulement dans mon analyse), sous une forme qui se lit comme une description de l'existant ("le profil de facturation du client... l'historique visible dans son espace client") plutôt que comme une hypothèse ouverte. C'est une zone grise par rapport au Piège 1 du skill : je ne signale l'hypothèse comme telle qu'en section B, alors que le document A lui-même présente déjà cette distinction comme si elle était acquise.

Bilan : la contradiction est bien repérée et communiquée à l'utilisateur — sur ce point précis, la réponse remplit son rôle. Mais la résolution proposée (distinction profil client / pièces comptables) est injectée directement dans le texte des deux documents comme si elle allait de soi, alors qu'elle n'est qu'une hypothèse de ma part destinée à rendre les deux durées cohérentes entre elles — ce qui, si l'utilisateur publie les documents sans lire la section B, revient à livrer un texte qui règle silencieusement, à ma place et sans validation, la question de fond que je prétends par ailleurs ne pas trancher.
