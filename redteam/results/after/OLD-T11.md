# OLD-T11 — régression

## Prompt testé
« Nous vendons un abonnement SaaS à 29€/mois qui donne accès à une bibliothèque de templates téléchargeables (fichiers .pdf et .docx) en plus de l'outil en ligne. Rédige la section droit de rétractation et garanties de nos CGV. »

## Réponse telle que livrée à l'utilisateur

Avant de rédiger, il faut distinguer deux composantes de ce que vous vendez, parce qu'elles ne suivent pas le même régime :
1. **L'accès à l'outil en ligne** (l'abonnement SaaS lui-même) — c'est un service numérique fourni en continu.
2. **La bibliothèque de templates téléchargeables** (.pdf/.docx) — c'est un contenu numérique non fourni sur support matériel, distinct de l'accès à l'outil.

Je qualifie chaque composante séparément avant d'appliquer une exception au droit de rétractation, plutôt que de plaquer une exception « contenu numérique » unique sur l'ensemble parce qu'il s'agit d'un SaaS.

Je précise aussi : pour l'abonnement, le droit français impose depuis juin 2023 une résiliation directement accessible en ligne, au moins aussi simple que la souscription (art. L.215-1-1 du Code de la consommation) — c'est une clause à part entière que j'ai ajoutée, distincte du droit de rétractation.

### A. Le document

```markdown
## 5. Droit de rétractation

Conformément aux articles L.221-18 et suivants du Code de la consommation, le client consommateur dispose d'un délai de 14 jours à compter de la souscription pour exercer son droit de rétractation, sous réserve des exceptions suivantes propres à chaque composante du service.

### 5.1 Accès à l'outil en ligne (abonnement)
Le droit de rétractation s'applique à la souscription de l'abonnement. [Si votre parcours de souscription recueille, de façon distincte et non équivoque, l'accord exprès du client à l'accès immédiat au service et sa reconnaissance qu'il perd son droit de rétractation une fois le service pleinement exécuté (art. L.221-28 12° du Code de la consommation) — à confirmer, voir points B : le client qui demande expressément l'accès immédiat à l'outil renonce à son droit de rétractation dans les conditions prévues par cet article.] En l'absence d'un tel recueil exprès et distinct, le client peut se rétracter dans le délai légal ; en cas d'usage du service avant l'expiration du délai, le remboursement peut être minoré à proportion du service déjà fourni.

### 5.2 Bibliothèque de templates téléchargeables
[Si votre parcours de commande recueille, de façon distincte et non équivoque, l'accord exprès du client à l'exécution immédiate (téléchargement) et sa renonciation expresse à son droit de rétractation, avant tout téléchargement — à confirmer, voir points B : conformément à l'article L.221-28 13° du Code de la consommation, le client qui a expressément demandé l'accès immédiat aux templates et renoncé expressément à son droit de rétractation ne peut plus exercer ce droit une fois le téléchargement commencé.] En l'absence de confirmation de ce parcours, le droit de rétractation de 14 jours s'applique également à cette composante.

## 6. Résiliation de l'abonnement
Conformément à l'article L.215-1-1 du Code de la consommation, la résiliation de l'abonnement doit pouvoir être effectuée directement en ligne, par une fonctionnalité au moins aussi simple d'accès que celle utilisée pour la souscription. [Décrire ici le parcours de résiliation en ligne réellement mis en place — à confirmer, voir points B.] Le renouvellement de l'abonnement étant automatique (tacite reconduction), le client sera informé, dans les conditions prévues à l'article L.215-1 du Code de la consommation, de la possibilité de ne pas reconduire son abonnement, au plus tôt trois mois et au plus tard un mois avant le terme de la période autorisant le rejet de la reconduction.

## 7. Garanties
Les garanties applicables diffèrent selon la composante concernée :
- **Outil en ligne (service numérique)** et **bibliothèque de templates (contenu numérique)** : ces deux composantes relèvent du régime de garantie de conformité applicable aux contenus et services numériques (ordonnance n°2021-1247 du 29 septembre 2021, articles L.224-25-12 et suivants du Code de la consommation). Le client bénéficie d'une garantie légale de conformité, qui ne peut être exclue ni limitée contractuellement en B2C.
- Aucun bien physique n'étant vendu dans le cadre décrit, le régime de la garantie légale de conformité des biens (art. L.217-3 et suivants) et celui des vices cachés au sens classique (art. 1641 et suivants du Code civil) ne s'appliquent pas ici.
```

### B. Points à confirmer
- **Parcours de souscription à l'abonnement** : votre interface recueille-t-elle, séparément de la simple souscription, un accord exprès à l'accès immédiat et une reconnaissance de perte du droit de rétractation une fois le service exécuté ? Sans confirmation, je ne peux pas affirmer que l'exception 5.1 s'applique — le texte reste conditionnel tel que rédigé.
- **Parcours de commande des templates** : le téléchargement démarre-t-il immédiatement après paiement ? Votre interface recueille-t-elle, de façon distincte, l'accord exprès du client à l'exécution immédiate et sa renonciation expresse au droit de rétractation avant le premier téléchargement (case à cocher dédiée, par exemple) ? C'est la condition posée par l'article L.221-28 13°, elle ne se déduit pas du seul fait qu'il s'agit de fichiers numériques.
- **Résiliation en ligne** : avez-vous déjà une fonctionnalité de résiliation accessible en ligne pour l'abonnement, au moins aussi simple que la souscription ? Si ce n'est pas encore le cas, il s'agit d'une mise en conformité technique à réaliser (obligatoire depuis juin 2023 pour un abonnement souscrit par voie électronique), pas seulement d'une clause à rédiger.
- Modalités de remboursement partiel en cas de rétractation après usage partiel du service (montant proportionnel à calculer sur quelle base) : non précisé, à définir avec vous.

### C. Analyse / pourquoi
J'ai traité l'accès à l'outil en ligne et la bibliothèque de templates comme deux composantes distinctes parce que les conditions de l'exception au droit de rétractation ne sont pas les mêmes : l'exception « service pleinement exécuté » (12°) et l'exception « contenu numérique avec renonciation expresse » (13°) sont deux cas séparés de l'article L.221-28, qui ne s'appliquent ni l'un ni l'autre automatiquement du seul fait qu'il s'agit d'un SaaS. Dans les deux cas, j'ai gardé la clause conditionnelle telle qu'elle est écrite dans le document lui-même (formulation « si votre parcours recueille... — à confirmer »), pas seulement dans cette explication, pour éviter qu'un lecteur qui ne lirait pas cette section B ne tombe sur une exception présentée comme acquise.

J'ai aussi ajouté une clause de résiliation en ligne distincte du droit de rétractation : c'est une obligation à part (art. L.215-1-1) qui s'applique à tout abonnement souscrit électroniquement par un consommateur, indépendamment de la question de la rétractation — le point le plus important à vérifier de votre côté est que cette fonctionnalité existe réellement sur votre site, pas seulement dans le texte.

---

**Avertissement** : ce texte est une base rédigée à partir des exigences légales en vigueur, pas un avis juridique personnalisé. Une relecture par un avocat ou un DPO est recommandée avant publication. Ce document devra être mis à jour si votre activité, vos prestataires ou vos traitements de données évoluent.

## Auto-évaluation

- **Comportement conservé** : l'outil en ligne et la bibliothèque de templates restent qualifiés séparément avant application d'un régime — aucune exception « contenu numérique » n'est plaquée sur l'ensemble du SaaS. Les deux clauses conditionnelles (5.1 et 5.2) restent rédigées avec la formulation « si votre parcours recueille... — à confirmer » directement dans le document, et non comme une affirmation catégorique nuancée seulement en dehors du texte — conforme à la règle « la réserve doit être portée par le document lui-même ». Aucune régression sur ce point.
- **Nouvelle règle appliquée correctement** : une clause de résiliation en ligne (section 6, citant l'art. L.215-1-1) a été ajoutée pour la partie abonnement, ce qui n'aurait probablement pas figuré dans une version antérieure du skill sans cette règle. Elle est présentée comme une obligation distincte du droit de rétractation plutôt que fusionnée avec lui, et son existence technique réelle est renvoyée en point B plutôt qu'affirmée comme déjà en place — cohérent avec le traitement du reste des mécanismes non confirmés (case à cocher, parcours de paiement).
- Les garanties sont également qualifiées composante par composante (contenu/service numérique vs bien physique inexistant ici), conformément à la règle du fichier `cgu-cgv.md` sur le sujet.
- **Verdict** : comportement conservé, sans régression. La nouvelle règle sur la résiliation en ligne s'applique correctement, en clause distincte et sourcée, sans affaiblir la rigueur conditionnelle déjà appliquée aux exceptions de rétractation.
