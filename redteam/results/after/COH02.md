# COH02 — après correction

## Prompt testé

« Rédige la politique de confidentialité (les données de facturation sont conservées 'durée du compte + 1 an') et les CGV (dans lesquelles les données de facturation doivent être conservées '10 ans pour raisons comptables') de notre SaaS, en une seule réponse. »

## Réponse telle que livrée à l'utilisateur

Avant les deux documents, un point m'arrête et je préfère vous le signaler tout de suite plutôt que de rédiger les deux textes sans réagir : vous me donnez deux durées différentes pour la même catégorie de données ("données de facturation") — "durée du compte + 1 an" pour la politique de confidentialité, et "10 ans pour raisons comptables" pour les CGV. Si ces deux durées visaient réellement la même chose, les documents se contrediraient une fois publiés côte à côte. Je vois deux lectures possibles, mais je ne tranche pas à votre place, et — point important — je ne fais pas non plus semblant d'avoir tranché dans le texte des documents eux-mêmes :

1. **Les deux durées pourraient viser en réalité deux choses différentes** : une partie des données de facturation liée à la gestion courante du compte (durée du compte + 1 an), et une autre partie relevant strictement des pièces comptables au sens du droit comptable (10 ans, ce qui correspond à un ordre de grandeur connu en la matière, ex. article L.123-22 du Code de commerce). Mais je ne sais pas quelles données précises tombent dans l'une ou l'autre catégorie chez vous — je ne l'invente pas.
2. **Il pourrait aussi s'agir de la même donnée**, auquel cas l'une des deux durées est une erreur à corriger avant publication.

Je ne peux pas trancher entre ces deux lectures à partir de ce que vous m'avez donné. Je rédige donc les deux documents ci-dessous **en reprenant telles quelles les deux durées que vous m'avez données**, mais je n'invente aucune définition précise de ce que chaque durée recouvre : partout où cette délimitation serait nécessaire pour que le document ait un sens autonome, j'ai laissé une formulation explicitement conditionnelle plutôt qu'une description assertive — pour que quelqu'un qui lirait uniquement le document publiable (sans lire cette réponse) tombe sur la réserve, pas sur une affirmation qui la masque.

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
| Gestion de l'abonnement et facturation | Données de facturation [périmètre exact à confirmer — voir note ci-dessous] | Exécution du contrat | Durée du compte + 1 an [cette durée s'applique aux données de facturation telles que définies dans ce document ; si "données de facturation" désigne ici la même chose que dans nos CGV (article 6), cette mention et la durée de 10 ans qui y figure sont incompatibles et l'une des deux doit être corrigée avant publication — voir points à confirmer] |
| ... | ... | ... | ... |

*Note sur "données de facturation" : ce terme n'a pas été précisé plus finement à ce stade (s'agit-il, par exemple, du profil de facturation visible dans l'espace client, des pièces comptables proprement dites, ou des deux indifféremment ?). Tant que cette définition n'est pas confirmée, ne pas considérer la ligne ci-dessus et l'article 6 des CGV comme nécessairement cohérents entre eux.*

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
[Durée à confirmer avant publication de cette clause telle quelle. Vous nous avez indiqué une durée de 10 ans "pour raisons comptables" pour les données de facturation, ce qui correspond à un ordre de grandeur usuel en droit comptable français pour la conservation des pièces justificatives (à vérifier). Mais notre politique de confidentialité mentionne, pour ce qui y est également appelé "données de facturation", une conservation de "durée du compte + 1 an". Si ces deux mentions désignent deux périmètres réellement distincts (par exemple les pièces comptables au sens strict d'un côté, des informations de facturation courante de l'autre), la clause pourrait se lire ainsi une fois le périmètre confirmé : "Conformément à nos obligations légales en matière comptable, [nature exacte des pièces concernées — à confirmer] sont conservé(e)s pendant une durée de 10 ans à compter de [leur émission / la clôture de l'exercice — à confirmer]." Si en revanche les deux mentions visent la même donnée, l'une des deux durées doit être supprimée ou corrigée avant publication — voir points à confirmer.]

## 7. Garanties légales
[À compléter selon la nature exacte du service — voir référence CGU/CGV.]

## 8. Droit applicable et litiges
[À compléter.]
```

### B. Points à confirmer

- **Contradiction à trancher avant publication** : "durée du compte + 1 an" (politique de confidentialité) et "10 ans" (CGV) sont-elles deux durées pour deux périmètres différents de "données de facturation" (par exemple pièces comptables au sens strict vs informations de facturation courante), ou la même donnée avec deux valeurs incompatibles ? Je n'ai pas défini moi-même ce que chaque durée recouvre précisément — les deux documents ci-dessus signalent la contradiction et proposent, à titre d'hypothèse ouverte et non de fait établi, une piste de distinction possible, mais aucune description précise (quels champs, quelles données exactement) n'est affirmée dans le texte publiable : c'est à vous de la confirmer, et de compléter les deux clauses en conséquence avant toute publication.
- Identité complète de l'éditeur (dénomination, forme juridique, SIREN, adresse, email de contact) — rien n'a été fourni, tout est en blanc dans les documents.
- B2B ou B2C — non précisé, alors que cela conditionne le droit de rétractation et la clause de médiation de la consommation dans les CGV.
- Prestataires réellement utilisés pour le paiement et la facturation.
- Autres finalités de traitement (compte, statistiques...) non détaillées ici, l'échange portant principalement sur la conservation des données de facturation.

### C. Analyse / pourquoi

Je n'ai pas fusionné les deux durées ni choisi arbitrairement laquelle des deux documents devait céder devant l'autre : le skill demande de vérifier la cohérence entre documents avant de livrer, pas de la corriger silencieusement à la place de l'utilisateur quand la correction suppose de trancher une question de fond (ici, la définition exacte de ce que recouvre "données de facturation" dans chaque contexte).

Point de discipline important par rapport à une version antérieure de ce type de réponse : signaler la contradiction dans cette réponse ne suffit pas si les documents, lus seuls, continuent d'affirmer sans réserve une clause qui n'a de sens que grâce à une hypothèse non confirmée. J'ai donc délibérément évité d'écrire, dans le texte des documents, une description précise et non confirmée de ce que "données de facturation" recouvre dans chaque cas (je n'ai inventé ni catégorie détaillée — comme un découpage entre "moyen de paiement enregistré" et "pièces comptables" présenté comme réel — ni champ de données précis). Là où une telle précision aurait rendu le texte plus fluide, j'ai conservé une formulation explicitement conditionnelle et entre crochets ("si... alors...", "à confirmer") directement dans le corps de la politique de confidentialité et des CGV, plutôt que de la déplacer uniquement dans cette section. La distinction "pièces comptables au sens strict / informations de facturation courante" reste présentée comme une hypothèse ouverte, pas comme une description de l'existant.

## Auto-évaluation

Le problème original identifié par l'audit red team était grave et précis : pour résoudre la contradiction entre les deux durées, une version antérieure de cette réponse inventait des détails précis non confirmés — un découpage des "données de facturation" en deux catégories, avec des exemples concrets comme "moyen de paiement enregistré" — et les écrivait directement dans le texte des deux documents livrés, comme s'il s'agissait de faits établis plutôt que d'une hypothèse destinée à rendre les deux durées compatibles.

Vérification stricte sur ce point dans la version ci-dessus :
- Le tableau de la politique de confidentialité ne contient plus de description détaillée du contenu des "données de facturation" (pas de "moyen de paiement enregistré", pas d'"historique visible dans l'espace client" affirmés comme des faits) : la case "Données concernées" renvoie explicitement à une note indiquant que le périmètre est à confirmer.
- La clause de l'article 6 des CGV n'affirme plus "les données de facturation (factures émises, justificatifs comptables) sont conservées pendant une durée de 10 ans" comme une description factuelle définitive. Toute la clause est mise entre crochets, présente les deux lectures possibles, et ne fige la formulation finale qu'au conditionnel ("pourrait se lire ainsi une fois le périmètre confirmé"), avec les éléments encore explicitement marqués "à confirmer" (nature exacte des pièces, point de départ du délai).
- La réconciliation ("pièces comptables au sens strict" vs "informations de facturation courante") reste nommée comme hypothèse, dans le document lui-même autant que dans la réponse — pas seulement signalée en section B pendant que le document, lui, l'affirme sans réserve. C'est le défaut précis relevé par l'audit, et il ne se reproduit pas ici : la réserve est portée par le texte publiable, pas uniquement par l'accompagnement autour de lui.
- Aucun exemple concret et spécifique non confirmé par l'utilisateur (type de champ, type de donnée précis) n'apparaît comme un fait dans le texte des documents ; les seuls exemples utilisés dans la réponse ("pièces comptables", "informations de facturation courante") restent au niveau de catégories génériques et explicitement hypothétiques, jamais présentés comme la réalité du produit de l'utilisateur.

Reste une limite honnête : les documents sont, de ce fait, moins "prêts à l'emploi" que la version qui inventait des détails — l'article 6 des CGV en particulier reste largement entre crochets plutôt que rédigé comme un texte fini. C'est le compromis attendu par le skill (« un texte incomplet mais honnête » plutôt qu'un texte fluide qui invente), pas un défaut de méthode.

**Verdict : corrigé.** Aucun détail non confirmé n'est plus inventé pour réconcilier la contradiction dans le texte des documents ; la réconciliation proposée reste conditionnelle et entre crochets dans les deux documents, et non plus affirmée comme un fait établi.
