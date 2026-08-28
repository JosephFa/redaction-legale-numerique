# AUD02 — audit de document

## Document soumis

Message utilisateur d'accompagnement :
> Peux-tu auditer notre politique de confidentialité ? On est un SaaS B2C basique.

Document :
```
# Politique de confidentialité

Nous collectons vos données (nom, email, historique d'achats, données de navigation) pour améliorer nos services. Base légale : intérêt légitime.

Vos données sont conservées 2 ans.

Nous utilisons Stripe, Google Analytics, Mailchimp et un hébergeur américain pour faire fonctionner le service.

Vous avez le droit d'accès, de rectification et d'effacement de vos données. Contactez-nous à privacy@example.com.
```

## Réponse telle que livrée à l'utilisateur

Qualification rapide : SaaS B2C, donc des utilisateurs individuels dont les données sont traitées principalement sur la base de la relation de compte/abonnement et de l'usage du service. Voici la grille (🟢 présent et correct — 🟠 présent mais incomplet/à vérifier — 🔴 absent alors qu'obligatoire ou risqué — ⚪ non applicable) :

| Clause / sujet | Statut | Pourquoi |
|---|---|---|
| Identité du responsable de traitement | 🔴 | Le document ne nomme jamais l'entité responsable du traitement ("nous" n'est identifié nulle part) — à corriger indépendamment du reste |
| Données collectées | 🟢 | Catégories listées (nom, email, historique d'achats, données de navigation) |
| Finalité | 🟠 | "Améliorer nos services" est une formulation unique et assez vague pour des données de nature très différente (identité, achats, navigation) — un SaaS a en réalité plusieurs finalités distinctes (gestion de compte, facturation, mesure d'audience...) qui mériteraient d'être séparées |
| Base légale | 🔴 | Une seule base légale ("intérêt légitime") appliquée à l'ensemble des données et finalités. C'est un point explicitement à risque : la gestion du compte et de l'historique d'achats relève normalement de l'exécution du contrat, pas de l'intérêt légitime — qui est en outre la base légale la plus exigeante à justifier (test de mise en balance) et la moins adaptée par défaut. Le RGPD exige une base légale par finalité, pas une base unique "au cas où" |
| Durée de conservation | 🟠 | "2 ans" est annoncé de façon uniforme pour toutes les données, sans distinction par finalité ni justification (comptable, contractuelle...). Une durée doit en principe être adossée à un critère par catégorie de donnée, pas être une valeur unique appliquée à tout |
| Destinataires / sous-traitants | 🟢 | Les outils réels sont nommés (Stripe, Google Analytics, Mailchimp, hébergeur) plutôt qu'une formule vague — bonne pratique, même si le rôle précis de chacun (sous-traitant, responsable conjoint...) n'est pas détaillé |
| Transferts hors Union européenne | 🔴 | Absent alors que les quatre outils cités (Stripe, Google Analytics, Mailchimp, hébergeur américain) sont tous susceptibles d'impliquer un transfert de données hors UE/EEE. Aucun mécanisme (clauses contractuelles types, décision d'adéquation...) n'est mentionné — c'est une lacune significative, pas un détail de forme |
| DPO | 🔴 | Aucune mention de l'existence ou de l'absence d'un DPO. Sur la base des informations communiquées, aucun élément ne permet de conclure à une obligation de désignation, mais le document devrait au moins indiquer explicitement qu'il n'y en a pas (ou qui en tient lieu), plutôt que de rester silencieux sur le sujet |
| Droits des personnes | 🔴 | Liste incomplète : accès, rectification, effacement sont présents, mais il manque la limitation, la portabilité, l'opposition, le droit de retirer son consentement à tout moment, et le droit d'introduire une réclamation auprès de la CNIL |
| Délai de réponse aux demandes | 🔴 | Absent. Le délai de principe d'un mois (prolongeable de deux mois selon la complexité, art. 12 RGPD) n'est pas mentionné |
| Sécurité | ⚪ | Aucune section sur ce sujet dans le document soumis — non évaluable en l'état, mais à ajouter |
| Cookies | 🟠 | Google Analytics est cité comme outil, ce qui implique très probablement des cookies/traceurs, mais aucune politique de cookies ni bandeau de consentement n'est mentionné dans ou à côté de ce document |
| Mineurs | ⚪ | Non applicable en l'état — aucune information ne permet de dire si le service vise ou non des mineurs, non traité comme un manque bloquant faute de contexte |

**Contradictions** : le point le plus problématique n'est pas une contradiction entre deux clauses du texte, mais une incohérence interne à la base légale retenue : "intérêt légitime" comme base unique s'accorde mal avec la nature des données listées (l'historique d'achats relève typiquement de l'exécution d'un contrat) et avec l'usage de Stripe (paiement, donc relation contractuelle). Cette même base légale unique fragilise aussi la mention du droit d'opposition qui, elle, est absente — un droit d'opposition est justement le corollaire attendu d'un traitement fondé sur l'intérêt légitime, et son absence ici est d'autant plus problématique que c'est la base légale choisie.

**Autre document potentiellement concerné** : la présence de Google Analytics suggère fortement l'usage de cookies/traceurs non strictement nécessaires — une politique de cookies (ou une section dédiée) est probablement aussi nécessaire. Je ne l'ai pas rédigée ici, dites-moi si vous voulez que je m'en occupe.

---

Ce retour est une base d'analyse à partir des obligations légales en vigueur, pas un avis juridique personnalisé — une relecture par un avocat ou un DPO est recommandée avant republication, en particulier vu le nombre de mentions obligatoires manquantes (transferts hors UE, droits, délai de réponse). Ce document devra aussi être mis à jour si vos outils ou traitements évoluent.

## Auto-évaluation

Relecture du document original en tant qu'auditeur externe, faille par faille :

1. **Une seule base légale ("intérêt légitime") appliquée à toutes les finalités sans distinction, alors que la gestion de compte/achat relève plutôt de l'exécution du contrat** — **repérée**. La grille marque explicitement ce point en 🔴 et nomme la bonne base légale alternative pour l'historique d'achats.

2. **Durée de conservation unique et uniforme de 2 ans pour toutes les données, sans justification ni distinction par finalité** — **repérée**, mais classée 🟠 plutôt que 🔴 : la grille signale l'absence de distinction par finalité et de justification, ce qui correspond bien à la faille attendue.

3. **Aucune mention d'un mécanisme de transfert hors UE alors que les 4 outils cités sont américains** — **repérée**. Marquée 🔴 avec la liste des quatre outils concernés et la mention explicite de l'absence de mécanisme.

4. **Aucune mention de l'existence ou non d'un DPO** — **repérée**. Marquée 🔴, avec la nuance correcte (absence d'éléments ne veut pas dire absence d'obligation, mais le silence total sur le sujet est lui-même le problème signalé).

5. **Liste des droits incomplète (manque limitation, portabilité, opposition, retrait du consentement, réclamation CNIL)** — **repérée**. La grille énumère précisément les cinq éléments manquants.

6. **Aucun délai de réponse mentionné** — **repérée**. Marquée 🔴 avec la référence à l'article 12 RGPD et au délai d'un mois prolongeable.

Bilan : les 6 failles listées sont repérées et correctement classées. Le point le plus proche d'une sous-évaluation est la durée de conservation (faille 2), classée 🟠 plutôt que 🔴 — un choix défendable puisqu'une durée est bien indiquée (ce n'est pas une absence pure), mais qui pourrait sous-estimer le risque si "2 ans" appliqué sans distinction à des données de navigation est en réalité disproportionné. Aucune faille de la liste n'a été purement manquée.
