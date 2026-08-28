# AUD04 — audit de document

## Document soumis

Message utilisateur d'accompagnement :
> Peux-tu auditer nos CGU ? C'est une plateforme où les utilisateurs publient du contenu créatif (dessins, textes).

Document :
```
CGU de CreativeHub. En créant du contenu sur la plateforme, vous cédez immédiatement et intégralement tous vos droits de propriété intellectuelle sur ce contenu à CreativeHub, pour le monde entier et pour toujours. CreativeHub ne pourra en aucun cas être tenu responsable, pour quelque raison que ce soit, y compris en cas de faute grave. CreativeHub peut suspendre ou supprimer votre compte à tout moment, sans préavis ni justification. En cas de résiliation de votre côté, un préavis de 3 mois est exigé.
```

## Réponse telle que livrée à l'utilisateur

Point de qualification préalable : vous décrivez une plateforme grand public où des utilisateurs publient des créations (dessins, textes) — donc a priori des consommateurs B2C, auteurs au sens du droit d'auteur sur leurs propres contenus. C'est important, parce que les clauses ci-dessous sont d'autant plus sensibles que le public visé est composé de particuliers créateurs, pas de professionnels contractant en connaissance de cause. Cette hypothèse conditionne la lecture qui suit ; dites-moi si une partie de vos utilisateurs sont en réalité des professionnels (agences, studios), le régime des clauses abusives ne s'appliquant pas de la même façon.

### Grille d'audit

| Clause / sujet | Statut | Pourquoi |
|---|---|---|
| Objet / description du service | 🔴 | Absente du document — il n'y a aucune présentation de ce qu'est la plateforme avant d'entrer directement dans la cession de droits |
| Cession de propriété intellectuelle (totale, immédiate, monde entier, perpétuelle) | 🔴 | Une cession intégrale et perpétuelle de tous les droits est disproportionnée par rapport aux besoins réels de l'éditeur (héberger, afficher, promouvoir le contenu) ; une licence limitée à l'exploitation du service est l'usage recommandé pour ce type de plateforme, et un tel déséquilibre est à risque d'être qualifié de clause abusive pour des utilisateurs particuliers |
| Droits moraux de l'auteur | 🔴 | Non évoqués — en droit français, le droit moral (paternité, respect de l'œuvre) est inaliénable et ne peut pas être cédé, même par une clause aussi large que celle-ci ; le texte laisse penser à tort que "tous les droits" incluent ce qui ne peut juridiquement pas l'être |
| Limitation de responsabilité de l'éditeur | 🔴 | Exonération totale, y compris pour faute grave : ce type de clause est nul en droit français (les clauses excluant la responsabilité pour faute lourde ou dolosive ne peuvent être stipulées), indépendamment de la qualification B2B/B2C |
| Suspension/suppression de compte par l'éditeur (à tout moment, sans préavis ni justification) | 🟠 | Présent, mais l'absence totale de justification et de préavis, à mettre en regard de la clause suivante, pose un problème d'équilibre (voir contradictions) |
| Résiliation par l'utilisateur (préavis de 3 mois) | 🔴 | Un préavis de 3 mois imposé à l'utilisateur pour quitter le service, alors que l'éditeur peut agir immédiatement et sans justification, crée un déséquilibre significatif entre les parties — à risque d'être une clause abusive en B2C |
| Règles de comportement / contenu interdit | 🔴 | Absentes |
| Conditions d'accès (âge minimum, création de compte) | 🔴 | Absentes |
| Modalités d'acceptation des CGU | 🔴 | Absentes — aucun mécanisme d'acceptation décrit |
| Renvoi vers la politique de confidentialité | 🔴 | Absent, alors que la plateforme a nécessairement des comptes utilisateurs et donc des données personnelles à traiter |
| Droit applicable et juridiction | ⚪ | Non mentionné — à ajouter, en tenant compte des règles impératives protectrices si des consommateurs européens sont visés |
| Modification des CGU (préavis, notification) | 🔴 | Absente |

### Contradictions identifiées

- **Cession totale de PI vs besoin réel de l'éditeur** : la clause va bien au-delà de ce qu'exige l'exploitation normale du service (héberger, afficher, promouvoir). Une cession de "tous les droits, pour le monde entier et pour toujours" prive l'utilisateur de toute possibilité de réexploiter, vendre ou republier ailleurs ses propres créations — pour un public de créateurs particuliers, ce déséquilibre est le cœur du risque de ce document.
- **Asymétrie de résiliation** : la clause de résiliation côté éditeur ("à tout moment, sans préavis ni justification") et celle côté utilisateur ("préavis de 3 mois exigé") figurent l'une à côté de l'autre dans le même texte et créent un déséquilibre direct et visible entre les droits de chaque partie — c'est exactement le type de contradiction interne que ce document doit résoudre en premier, indépendamment de toute autre lacune.
- **Exonération totale de responsabilité y compris faute grave** : cette clause est en elle-même contraire à un principe d'ordre public (la faute lourde ou dolosive ne peut jamais être exonérée), donc invalide quelle que soit la qualification des parties.

### Autres points

- Le document ne mentionne aucune politique de confidentialité alors qu'une plateforme avec comptes utilisateurs traite nécessairement des données personnelles — un document séparé (ou une section dédiée) est probablement nécessaire, je ne l'ai pas rédigé ici puisque seules les CGU ont été transmises.
- Si la plateforme vend un abonnement ou des fonctionnalités payantes, des CGV distinctes seraient également concernées — non traité ici faute d'indication en ce sens dans le message ou le document.

Ce document concentre plusieurs clauses 🔴 qui, prises ensemble, dessinent un déséquilibre systématique en faveur de l'éditeur (droits, responsabilité, résiliation) — un profil de risque élevé pour un service ouvert à des utilisateurs particuliers.

---

Ceci est une base d'analyse à partir des exigences légales en vigueur, pas un avis juridique personnalisé. Une relecture par un avocat est recommandée avant toute publication ou correction, en particulier compte tenu du nombre et de la nature des clauses à risque identifiées ici. Les règles citées doivent être vérifiées dans leur version en vigueur à la date de publication.

## Auto-évaluation

Relecture du document original en tant qu'auditeur externe, faille par faille :

1. **Cession totale et perpétuelle de la propriété intellectuelle de l'utilisateur (au lieu d'une licence limitée aux besoins du service), disproportionnée et probablement abusive pour des utilisateurs particuliers** — **Repérée.** Signalée en 🔴 avec l'explication du déséquilibre, et reprise en tête de la section contradictions comme le point central du document.

2. **Clause de responsabilité totalement exonératoire y compris pour faute grave/dol, nulle en droit français quel que soit B2B ou B2C** — **Repérée.** Signalée en 🔴, avec la précision correcte que la nullité ne dépend pas de la qualification des parties.

3. **Asymétrie forte entre le droit de résiliation de l'éditeur (immédiat, sans justification) et celui de l'utilisateur (3 mois de préavis) — déséquilibre significatif potentiellement qualifiable de clause abusive en B2C** — **Repérée.** Signalée à la fois dans la grille (deux lignes distinctes mises en regard) et explicitement formulée comme contradiction interne au document.

Bilan : les trois failles réelles sont repérées et correctement expliquées, avec le lien de cohérence attendu entre les clauses qui se contredisent (résiliation asymétrique) plutôt qu'un simple constat isolé. Aucune lacune identifiée sur ces trois points pour cet audit.
