# AUD01 — audit de document

## Document soumis

Message utilisateur d'accompagnement :
> Peux-tu auditer nos mentions légales ? On est une boutique en ligne qui vend des accessoires à des particuliers en France.

Document :
```
# Mentions légales

## Éditeur
BrightApp SAS, SIREN/RCS 812345678 Paris
Siège social : 10 rue de Rivoli, 75004 Paris
Contact : contact@brightapp.fr
N° TVA : FR12812345678

## Propriété intellectuelle
Tous les contenus de ce site sont protégés.

## Données personnelles
Voir notre politique de confidentialité.
```

## Réponse telle que livrée à l'utilisateur

Avant la grille, une qualification rapide : vous vendez des accessoires en ligne à des particuliers en France — c'est donc une activité de vente à distance en B2C, ce qui déclenche notamment l'obligation d'indiquer un dispositif de médiation de la consommation, en plus des mentions LCEN classiques.

Voici la grille d'audit (🟢 présent et correct — 🟠 présent mais incomplet/à vérifier — 🔴 absent alors qu'obligatoire ou risqué — ⚪ non applicable) :

| Clause / sujet | Statut | Pourquoi |
|---|---|---|
| Dénomination sociale et forme juridique | 🟢 | "BrightApp SAS" présent |
| Capital social | 🔴 | Absent. Pour une société, le montant du capital social fait partie des mentions attendues sous LCEN/Code de commerce |
| Siège social | 🟢 | Adresse complète présente |
| SIREN / RCS | 🔴 | La ligne "SIREN/RCS 812345678 Paris" fusionne deux informations distinctes comme s'il s'agissait d'un seul numéro. Le SIREN et le numéro RCS ne sont pas la même donnée, et la ville du greffe d'immatriculation ne doit jamais être déduite de l'adresse du siège (une société peut être immatriculée dans un greffe différent, notamment après un déménagement). À vérifier séparément sur un extrait Kbis/Infogreffe et à présenter sous la forme "RCS [ville] [numéro RCS]" distincte du SIREN |
| Numéro de TVA intracommunautaire | 🟢 | Renseigné (FR12812345678), format cohérent avec un SIREN français |
| Directeur de la publication | 🔴 | Absent. Mention obligatoire (LCEN art. 6-III) — doit être une personne physique identifiée (souvent le représentant légal) |
| Contact email | 🟢 | Présent |
| Téléphone | 🟠 | Absent — recommandé mais pas systématiquement obligatoire selon l'activité |
| Hébergeur | 🔴 | Section entièrement absente du document. C'est une mention obligatoire distincte de l'éditeur : raison sociale, adresse et téléphone de l'hébergeur du site |
| Propriété intellectuelle | 🟢 | Clause générique présente et cohérente avec l'usage habituel |
| Données personnelles | 🟠 | Renvoi vers la politique de confidentialité présent, ce qui est la bonne pratique (éviter la duplication) — mais rien n'indique si un DPO existe ; si c'est le cas, son point de contact est souvent repris ici aussi |
| Médiation de la consommation | 🔴 | Absente. Pour une activité de vente à distance en B2C, cette mention est due (art. L.616-1 et R.616-1 du Code de la consommation) : nom du médiateur retenu et ses coordonnées |

**Contradictions** : je n'ai pas identifié de clause existante qui entre en contradiction directe avec une autre ou avec une règle impérative — le problème ici tient surtout à des absences (hébergeur, directeur de publication, médiation, capital social) plutôt qu'à un conflit entre deux passages du texte.

**Autres documents potentiellement concernés** : puisque vous vendez à des particuliers, des CGV (conditions générales de vente) sont vraisemblablement nécessaires en plus des mentions légales — je n'en ai pas vu trace dans ce que vous partagez, mais je ne les rédige pas ici sans confirmation de votre part que vous en avez besoin. Idem pour la politique de confidentialité elle-même : le document actuel n'en fait que le renvoi, donc son contenu réel n'a pas pu être audité.

---

Ce retour est une base d'analyse à partir des obligations légales en vigueur, pas un avis juridique personnalisé — une relecture par un avocat est recommandée avant republication, d'autant que ce document présente plusieurs mentions obligatoires manquantes. Pensez aussi à vérifier la version en vigueur du dispositif de médiation de la consommation au moment de la publication.

## Auto-évaluation

Relecture du document original en tant qu'auditeur externe, faille par faille :

1. **SIREN et RCS fusionnés en une seule ligne comme si c'était le même numéro** — **repérée**. La grille identifie explicitement le problème et exige de vérifier les deux informations séparément.

2. **Absence de section hébergeur** — **repérée**. Marquée 🔴 avec la liste des informations attendues.

3. **Absence de directeur de publication** — **repérée**. Marquée 🔴 avec la référence à la base légale.

4. **Numéro de TVA affiché sans que sa base/justification soit interrogée** — **manquée**. La grille marque cette ligne 🟢 "présent, format cohérent" et se contente de vérifier la forme du numéro (structure FR + SIREN), sans jamais se demander si l'assujettissement à la TVA de BrightApp est réellement établi ni si ce numéro doit figurer par défaut. C'est exactement le type de vérification que le document de référence demande de faire ("ne le traite pas par défaut comme une mention universellement obligatoire, l'assujettissement dépend de la situation fiscale de l'entreprise") — la réponse ci-dessus ne pose pas cette question et traite la présence du numéro comme suffisante en soi.

5. **Absence de clause de médiation de la consommation malgré une activité B2C de vente à distance** — **repérée**. Marquée 🔴, avec la référence légale et le contexte B2C explicitement relié à cette obligation.

Bilan : 4 failles sur 5 correctement repérées et classées ; une (la question de la justification du numéro de TVA déjà affiché) a été traitée superficiellement — la grille valide sa présence sur la seule base de son format, sans interroger le fond, ce qui est précisément le type d'angle mort que ce document est censé éviter.
