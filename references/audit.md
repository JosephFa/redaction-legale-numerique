# Relecture / audit d'un document existant

Une relecture teste une compétence différente d'une rédaction : il ne s'agit pas seulement de repérer ce qui manque, mais aussi d'examiner ce qui est déjà écrit et qui pose problème — et de vérifier que les deux ne se contredisent pas entre eux.

Ne réécris pas l'intégralité du document sauf si l'utilisateur le demande explicitement. Produis une grille d'audit.

## Méthode

1. **Qualifier avant de juger.** Comme pour une rédaction, qualifie d'abord le contrat (bien, contenu numérique, service numérique, abonnement...), les parties (B2B/B2C), le pays. Une clause peut être parfaitement valable dans un contexte et abusive dans un autre — ne lui applique pas une règle générique avant d'avoir fait cette qualification. Par exemple, l'exception au droit de rétractation pour un contenu numérique fourni immédiatement a des conditions précises (accord exprès + renonciation expresse) : ne conclus pas qu'elle s'applique ou ne s'applique pas sans vérifier ce que le contrat propose réellement.

2. **Classer chaque clause existante**, pas seulement lister les absences :

| Statut | Signification |
|---|---|
| 🟢 | Présent et cohérent avec les obligations applicables |
| 🟠 | Présent mais incomplet, ou information à vérifier |
| 🔴 | Absent alors qu'obligatoire, ou juridiquement risqué / potentiellement contraire à une règle impérative |
| ⚪ | Hors sujet / non applicable à ce cas |

3. **Chercher systématiquement les contradictions** entre une clause existante et un droit impératif, ou entre deux parties du document. C'est souvent là que se niche le vrai risque : une clause "aucun remboursement" n'est pas juste une lacune de style, elle contredit potentiellement le droit de rétractation et la garantie légale de conformité en même temps — l'audit doit relier ces points plutôt que les traiter comme des remarques isolées.

4. **Ne pas transformer une bonne pratique en fait établi.** Si tu recommandes une case à cocher au moment de la souscription, dis que c'est une recommandation — ne décris pas un mécanisme d'acceptation qui n'a pas été confirmé comme existant.

5. **Signaler les références datées.** Une mention de plateforme de médiation, de seuil réglementaire ou de règle de store doit être accompagnée d'une invitation à vérifier sa version actuelle plutôt que présentée comme figée.

## Exemple de sortie

```markdown
| Clause / sujet | Statut | Pourquoi |
|---|---|---|
| Prix affiché | 🟠 | Présent mais ne précise pas TTC/HT |
| Droit de rétractation | 🔴 | Absent — contredit la clause "aucun remboursement" |
| Clause de non-remboursement | 🔴 | Entre en conflit avec le droit de rétractation et la garantie légale |
| Modification sans préavis | 🔴 | Clause à risque d'être jugée abusive en B2C |
| Tribunal exclusivement compétent | 🔴 | Non opposable à un consommateur |
| Identité du vendeur | 🔴 | Absente |
```

Termine par l'avertissement standard (pas un avis juridique, relecture par un avocat recommandée) et, si pertinent, signale qu'un autre document (CGU, politique de confidentialité...) pourrait aussi être concerné — sans le rédiger à sa place si ce n'est pas demandé.
