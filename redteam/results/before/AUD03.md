# AUD03 — audit de document

## Document soumis

Message utilisateur d'accompagnement :
> Peux-tu auditer nos CGV ? On est un service de coaching en ligne par abonnement, ouvert à tous.

Document :
```
CGV de CoachPro. Abonnement 39€/mois, renouvellement automatique. Aucun remboursement, sauf erreur de notre part. En vous abonnant, vous renoncez à votre droit de rétractation. Nous pouvons à tout moment ajuster nos tarifs sans préavis. Tout litige sera porté devant le Tribunal de commerce de Marseille exclusivement. Service ouvert aux particuliers comme aux professionnels.
```

## Réponse telle que livrée à l'utilisateur

Avant la grille : un point de qualification prioritaire. Vous décrivez le service comme "ouvert à tous" et le document dit explicitement "particuliers comme professionnels" — c'est-à-dire B2C et B2B dans le même texte, sans distinction. Or le droit de rétractation, le régime des clauses abusives et la compétence juridictionnelle protectrice ne s'appliquent qu'aux consommateurs (particuliers), pas aux professionnels. Tant que ce point n'est pas tranché — un seul document pour les deux publics, ou deux jeux de clauses distincts — le reste de l'audit ci-dessous est fait en supposant qu'une partie au moins de votre clientèle est composée de consommateurs B2C, ce qui semble être le cas pour un coaching "ouvert à tous".

### Grille d'audit

| Clause / sujet | Statut | Pourquoi |
|---|---|---|
| Qualification B2C/B2B dans un même document | 🔴 | "Particuliers comme professionnels" traités par les mêmes clauses, alors que rétractation, clauses abusives et for compétent divergent selon la partie — à trancher avant tout le reste |
| Identité du vendeur (dénomination, forme juridique, SIREN, adresse, contact) | 🔴 | Absente du document |
| Description du service | 🔴 | Absente — on sait seulement qu'il s'agit d'un abonnement de coaching, sans autre précision |
| Prix (39€/mois) | 🟠 | Présent, mais TTC/HT non précisé (obligatoire en B2C) |
| Renouvellement automatique | 🟠 | Mentionné, mais sans l'information préalable de reconduction tacite exigée en B2C avant la date limite de dénonciation (art. L215-1 du Code de la consommation) |
| Ajustement tarifaire à tout moment, sans préavis | 🔴 | Sur un contrat à exécution successive avec des consommateurs, ce type de clause est à haut risque d'être jugée abusive (le professionnel se réserve un droit de modification unilatérale sans encadrement ni information préalable) |
| "Aucun remboursement, sauf erreur de notre part" | 🔴 | Entre en conflit avec le droit de rétractation (voir ligne suivante) et avec la garantie légale de conformité, qui ne peut être écartée par contrat en B2C |
| "En vous abonnant, vous renoncez à votre droit de rétractation" | 🔴 | L'exception au droit de rétractation pour un contenu/service numérique suppose un accord exprès à l'exécution immédiate ET une renonciation expresse distincte, recueillis explicitement — le simple fait de s'abonner ne vaut pas cette renonciation. Rien dans le texte ne montre que ce mécanisme (case dédiée, confirmation séparée) existe |
| Droit de rétractation — délai et modalités d'exercice | 🔴 | Absent : le document ne décrit à aucun moment le délai légal de 14 jours ni la procédure d'exercice, seulement une clause de renonciation dont la validité n'est pas établie |
| Garanties légales (conformité, vices cachés selon ce qui est vendu) | 🔴 | Absentes |
| Médiation de la consommation | 🔴 | Absente, alors qu'elle est obligatoire dès qu'il y a des clients consommateurs |
| Tribunal de commerce de Marseille — compétence exclusive | 🔴 | Une clause attributive de compétence exclusive n'est pas opposable à un consommateur, qui conserve le choix de son tribunal |
| Droit applicable | ⚪ | Non mentionné séparément — à intégrer si un droit applicable explicite est ajouté |
| Modalités de résiliation par le client | 🔴 | Absentes |

### Contradictions identifiées

- **"Aucun remboursement" vs droit de rétractation et garantie légale** : la clause de non-remboursement, telle que rédigée, ne fait aucune exception pour la période légale de rétractation ni pour un défaut de conformité relevant de la garantie légale — deux droits que le contrat ne peut pas supprimer pour un consommateur.
- **Renonciation "automatique" à la rétractation vs conditions légales de l'exception** : le texte traite la renonciation comme acquise du seul fait de l'abonnement, alors que la loi exige un consentement exprès et distinct à cette renonciation. Combinée à la clause "aucun remboursement", cette clause aggrave le risque : un consommateur qui se rétracterait dans le délai légal se verrait opposer un texte qui, en l'état, ne prévoit ni délai ni modalité d'exercice.
- **Tribunal exclusif vs protection du consommateur** : la clause de compétence exclusive, combinée à l'absence de toute clause de médiation, prive le consommateur des deux voies de règlement qui lui sont normalement garanties (juridiction de son choix, médiation gratuite).
- **Mélange B2B/B2C** : dans la mesure où les clauses ci-dessus (rétractation, clauses abusives, for compétent) ne s'appliquent qu'aux consommateurs, appliquer un texte unique aux professionnels et aux particuliers revient soit à sur-protéger les professionnels, soit — plus probablement ici — à priver les consommateurs de protections auxquelles ils ont droit.

### Autres points

- Le document ne mentionne aucune modalité d'acceptation des CGV (case à cocher, confirmation de commande) — je ne peux pas savoir si un mécanisme existe déjà ; si vous en avez un, il doit être décrit, sinon c'est un point à ajouter.
- Un document CGU séparé (règles d'usage du service, compte, propriété intellectuelle du contenu de coaching le cas échéant) pourrait aussi être nécessaire si ce n'est pas déjà couvert ailleurs — je ne l'ai pas audité ici puisque seules les CGV ont été transmises.
- Si vous ajoutez une référence à la plateforme européenne de règlement en ligne des litiges, pensez à vérifier son URL/existence à la date de publication : ce dispositif évolue.

Ce document présente un nombre élevé de clauses 🔴, dont plusieurs se recoupent (non-remboursement, renonciation à la rétractation, absence de délai de rétractation) autour d'un même risque central : le contrat, en l'état, ne traite pas correctement le droit de rétractation d'un consommateur.

---

Ceci est une base d'analyse à partir des exigences légales en vigueur, pas un avis juridique personnalisé. Une relecture par un avocat est recommandée avant toute publication ou correction, en particulier vu le nombre de clauses à risque identifiées ici. Les règles citées (seuils, dispositifs de médiation) doivent être vérifiées dans leur version en vigueur à la date de publication.

## Auto-évaluation

Relecture du document original en tant qu'auditeur externe, faille par faille :

1. **Clause de non-remboursement quasi-absolue en conflit avec la garantie légale et le droit de rétractation** — **Repérée.** Signalée en 🔴 dans la grille et reprise dans la section contradictions, avec le lien explicite aux deux droits impératifs concernés.

2. **Renonciation au droit de rétractation "en vous abonnant" sans que les conditions de l'exception (accord exprès + renonciation expresse distincts) soient réunies ni décrites** — **Repérée.** La grille et la section contradictions expliquent précisément pourquoi le mécanisme décrit ("en vous abonnant") ne satisfait pas l'exigence légale.

3. **Ajustement tarifaire à tout moment sans préavis, risqué comme clause abusive ET incohérent avec le renouvellement automatique (qui suppose que le consommateur puisse arbitrer en connaissance de cause)** — **Repérée mais sous-évaluée.** Le risque de clause abusive de la modification tarifaire sans préavis est bien signalé en 🔴. En revanche, l'audit livré ne relie jamais explicitement cette clause à la clause de renouvellement automatique pour signaler l'incohérence spécifique entre les deux : le fait qu'un consommateur ne peut pas exercer un choix éclairé de reconduction ou de résiliation s'il ignore le prix qui lui sera appliqué. Les deux clauses sont traitées comme deux lignes distinctes de la grille, sans que ce lien de cohérence interne au document soit formulé — alors que la méthode du skill demande explicitement de chercher les contradictions "entre deux parties du document", pas seulement entre une clause et un droit impératif externe.

4. **Clause de tribunal exclusivement compétent non opposable à un consommateur** — **Repérée.** Signalée en 🔴, et reliée dans la section contradictions à l'absence de clause de médiation.

5. **Absence de clause de médiation de la consommation malgré l'exposition B2C** — **Repérée.** Ligne dédiée en 🔴 dans la grille.

6. **Mélange B2C/B2B sans distinguer les régimes qui divergent (rétractation, clauses abusives, tribunal compétent) — qualification bâclée à relever en premier** — **Repérée.** C'est le tout premier point soulevé, avant même la grille, conformément à la méthode ("qualifier avant de juger").

Bilan : 5 des 6 failles sont repérées et correctement expliquées. La faille n°3 est identifiée dans sa composante "risque de clause abusive" mais l'angle spécifique de l'incohérence interne avec la clause de renouvellement automatique — pourtant un exemple précis de ce que la méthode d'audit demande de rechercher (contradictions entre deux parties du document, pas seulement avec un droit externe) — n'a pas été formulé dans la réponse livrée.
