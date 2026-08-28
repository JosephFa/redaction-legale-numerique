# monapp — régression post-correction

## Prompt testé

> Peux-tu relire mes CGV et me dire ce qui manque ? Voici le texte : "CGV de MonApp. En utilisant MonApp vous acceptez ces conditions. Le prix est de 9,99€/mois. Aucun remboursement possible. Nous pouvons modifier ces conditions à tout moment sans préavis. Pour tout litige, tribunaux de Paris exclusivement compétents." C'est un service B2C pour des particuliers en France.

## Réponse telle que livrée à l'utilisateur

Voici l'audit clause par clause. Je n'ai pas réécrit le document — vous ne me l'avez pas demandé — mais si vous voulez une version corrigée ensuite, dites-le-moi.

**Qualification préalable** : vous confirmez B2C, particuliers, France. Il s'agit d'un abonnement mensuel (9,99€/mois) — donc à la fois un contrat à exécution successive et, très vraisemblablement, un contrat conclu par voie électronique (souscription en ligne pour une appli), ce qui déclenche des obligations spécifiques de résiliation en ligne détaillées plus bas. Je pars de cette hypothèse "conclu en ligne" comme vraisemblable pour une appli mais je ne l'ai pas vue confirmée explicitement dans votre message — à vérifier.

| Clause / sujet | Statut | Pourquoi |
|---|---|---|
| Identité du vendeur (dénomination, adresse, contact) | 🔴 | Absente. Obligatoire dans des CGV B2C — sans elle, l'ensemble du document est difficilement opposable. |
| Description du service | 🟠 | "MonApp" est nommé mais rien ne décrit ce qui est vendu (fonctionnalités, contenu de l'abonnement) — nécessaire pour qualifier ensuite les exceptions au droit de rétractation et le régime de garantie applicable. |
| Prix | 🟠 | Présent (9,99€/mois) mais ne précise pas s'il est TTC — obligatoire en B2C — ni les modalités de paiement/facturation. |
| Modalités de commande/souscription | 🔴 | Absentes. |
| Durée et tacite reconduction | 🔴 | Absentes. Pour un abonnement mensuel à tacite reconduction, l'article L215-1 du Code de la consommation impose d'informer le consommateur avant la date limite de dénonciation — rien ne l'organise ici. |
| Droit de rétractation | 🔴 | Absent — alors qu'il s'agit d'une clause obligatoire à préciser (délai de 14 jours par défaut en B2C, modalités, exceptions éventuelles). Son absence, combinée à la clause "aucun remboursement", est le point le plus problématique du document (voir plus bas). |
| Clause "Aucun remboursement possible" | 🔴 | Entre en contradiction directe avec le droit de rétractation (14 jours, sauf exception dûment caractérisée et non démontrée ici) et avec la garantie légale de conformité, qui ne peuvent être écartées par contrat en B2C. Une exception au droit de rétractation pour "contenu numérique" existe mais suppose un accord exprès du consommateur à l'exécution immédiate et une renonciation expresse et distincte à son droit de rétractation — rien dans le texte ne montre que cette condition est réunie ; on ne peut donc pas présumer l'exception acquise. |
| Résiliation — accessibilité en ligne | 🔴 | Absente, et c'est un point de non-conformité probable, pas seulement une lacune de rédaction : pour un abonnement souscrit en ligne par un consommateur, l'article L.215-1-1 du Code de la consommation impose depuis juin 2023 une fonctionnalité de résiliation directement accessible en ligne, au moins aussi simple que la souscription ("résiliation en trois clics"). Le texte ne prévoit aucun mécanisme de résiliation, en ligne ou autrement — à corriger en priorité si la souscription à MonApp se fait bien par voie électronique (à confirmer). |
| Garantie légale de conformité | 🔴 | Absente, et implicitement contredite par "aucun remboursement" — pour un contenu/service numérique, la garantie de conformité (étendue depuis l'ordonnance de 2021) ne peut pas être supprimée par contrat en B2C. |
| Modification des conditions "à tout moment sans préavis" | 🔴 | Clause à risque élevé d'être jugée abusive en B2C : une modification substantielle des conditions sans préavis ni droit de résiliation pour le consommateur est généralement sanctionnée. Elle contredit aussi, en pratique, l'exigence d'information préalable posée par l'article L215-1 pour la tacite reconduction si le prix ou la durée de l'abonnement venait à changer sans préavis. |
| Tribunaux de Paris exclusivement compétents | 🔴 | Non opposable à un consommateur : une clause attributive de compétence exclusive n'est pas valable face à un consommateur en droit français, qui conserve la possibilité de saisir la juridiction de son lieu de résidence. |
| Médiation de la consommation | 🔴 | Absente — obligatoire en B2C. Si vous ajoutez une référence à un médiateur ou à la plateforme européenne de règlement en ligne des litiges, son existence/URL doit être vérifiée à la date de rédaction, ce cadre évolue. |

**Contradictions à noter en particulier** : "aucun remboursement" + absence de droit de rétractation + absence de garantie légale forment un même point de risque, pas trois remarques isolées — ce sont les mêmes droits impératifs du consommateur qui sont contournés à trois endroits du texte. La clause de modification libre et la clause de compétence exclusive aggravent le profil de risque global du document (déséquilibre significatif potentiel au sens des clauses abusives).

**Documents connexes** : ces CGV ne mentionnent aucun renvoi vers une politique de confidentialité ni des CGU — si MonApp a des comptes utilisateurs, ces documents sont probablement aussi à vérifier, mais je ne les ai pas audités ici puisque vous ne me les avez pas fournis.

**Avertissement** : cette relecture est une base établie à partir des exigences légales en vigueur, pas un avis juridique personnalisé. Une relecture par un avocat est recommandée avant toute publication, notamment vu le nombre de clauses à risque identifiées ici. Les règles citées (seuils, plateformes de médiation) doivent être vérifiées dans leur version en vigueur à la date de publication.

## Auto-évaluation

**Comportement conservé, sans régression** :
- Méthode d'audit respectée : pas de réécriture intégrale du document, classification clause par clause avec les statuts 🟢🟠🔴⚪, qualification préalable (B2C, particuliers, France, abonnement) avant de juger les clauses.
- Droit de rétractation, clause "aucun remboursement", clause de modification sans préavis, et clause de médiation absente sont bien identifiés comme avant, avec la même sévérité (🔴) et le même lien de contradiction explicite entre "aucun remboursement" et le droit de rétractation/la garantie légale.
- La clause de compétence exclusive de Paris est bien signalée comme non opposable à un consommateur, comme dans les versions précédentes du skill.
- L'exception "contenu numérique" au droit de rétractation n'est pas présumée acquise faute de preuve d'accord exprès + renonciation expresse — conforme au Piège 2.
- Structure de sortie conforme à `references/audit.md` (tableau, pas de document réécrit, avertissement standard en fin de réponse).

**Nouvelle règle art. L215-1-1 — application vérifiée correcte** : l'audit relève désormais explicitement l'absence d'une clause de résiliation facilitée en ligne, avec la référence précise à l'article L.215-1-1 du Code de la consommation et la mention de son entrée en vigueur (juin 2023, règle dite "résiliation en trois clics"). Le point est correctement conditionné à la qualification du contrat ("si la souscription à MonApp se fait bien par voie électronique — à confirmer") plutôt que d'être asséné comme un fait acquis sans vérification, ce qui respecte à la fois la nouvelle règle de fond (`cgu-cgv.md`, piège dédié) et la discipline de qualification préalable du skill (Piège 2 / méthode d'audit, point 1). C'est cohérent avec le fait que MonApp est très vraisemblablement une souscription en ligne (une appli facturée 9,99€/mois), donc la règle est pertinente et correctement signalée, sans être sur-affirmée.

Aucune régression détectée : les points historiquement validés (rétractation, remboursement, médiation, modification sans préavis) restent identifiés au même niveau de sévérité qu'avant, et le nouveau point s'ajoute sans rien déplacer ni diluer.
