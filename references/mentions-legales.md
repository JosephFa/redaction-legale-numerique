# Mentions légales

Fondement principal : article 6-III de la loi n°2004-575 du 21 juin 2004 pour la confiance dans l'économie numérique (LCEN), complété par le Code de commerce (identification des sociétés) et le RGPD pour le point contact données personnelles.

Les mentions légales identifient qui est responsable du contenu du site/de l'appli, et sont obligatoires pour **tout** service de communication au public en ligne, qu'il soit commercial ou non — un site vitrine, un blog, une appli mobile qui a une page "à propos" ou un site associé, entrent tous dans le champ. Leur absence ou inexactitude est sanctionnée pénalement (jusqu'à 75 000 € pour une personne physique, 375 000 € pour une personne morale).

## Informations à collecter

**Si l'éditeur est une société :**
- Dénomination sociale ou raison sociale
- Forme juridique (SAS, SARL, etc.)
- Montant du capital social
- Adresse du siège social
- Numéro SIREN/SIRET
- Numéro RCS et ville d'immatriculation — le numéro qui figure dans la mention "RCS [Ville] [numéro]" est, en pratique, le SIREN de la société (ex: `RCS Paris 812 345 678`) : ce n'est donc pas une invention de le reprendre tel quel s'il a été fourni. Ce qui reste une information distincte, à obtenir séparément et à **ne jamais déduire de l'adresse du siège social**, c'est la **ville du greffe d'immatriculation** — une société peut être immatriculée dans un greffe différent de son siège actuel, notamment après un déménagement. Si la ville n'est pas donnée, demande-la ou signale-la comme à vérifier sur un extrait Kbis/Infogreffe plutôt que de la déduire. Si seul un numéro SIRET (14 chiffres) est fourni, les 9 premiers chiffres correspondent au SIREN : c'est une extraction technique fiable (pas une déduction risquée), mais signale-la comme telle plutôt que de présenter le SIRET et le SIREN comme un seul et même numéro.
- Numéro de TVA intracommunautaire — à mentionner seulement s'il a été fourni ou confirmé comme applicable ; ne le traite pas par défaut comme une mention universellement obligatoire, l'assujettissement dépend de la situation fiscale de l'entreprise.
- Nom du directeur ou de la directrice de la publication (représentant légal, ou toute personne désignée à cet effet)

**Si l'éditeur est une personne physique (auto-entrepreneur, profession libérale...) :**
- Nom, prénom
- Adresse (le domicile personnel peut être remplacé par l'adresse professionnelle si elle existe)
- Numéro SIREN/SIRET — obligatoire dès lors qu'une activité professionnelle est exercée (y compris en auto-entreprise), demande-le fermement plutôt que de le traiter comme optionnel

**Si l'éditeur est une association (loi 1901 ou équivalente) :**
- Dénomination et objet de l'association
- Adresse du siège social
- Numéro RNA (répertoire national des associations) si l'association y est inscrite — ce n'est pas un numéro SIREN/RCS, ne les confonds pas
- Nom du représentant légal (souvent le président) comme directeur de la publication
- Si l'association vend des biens/services/billets à titre habituel : elle peut être soumise aux mêmes règles de Code de la consommation qu'une société dès lors que la vente s'adresse à des consommateurs — ne pars pas du principe qu'un statut associatif exonère des obligations applicables aux CGV (voir `references/cgu-cgv.md`)

**Avant de choisir l'un de ces trois gabarits**, confirme le statut juridique réel de l'éditeur — ne le déduis pas du seul type de numéro communiqué (un SIRET n'est pas réservé aux sociétés commerciales).

**Coordonnées de contact :**
- Email de contact
- Téléphone (recommandé, pas toujours strictement obligatoire selon l'activité)

**Hébergeur du site/de l'application :**
- Raison sociale de l'hébergeur
- Adresse
- Numéro de téléphone
(Pour une appli mobile distribuée via un store, il est d'usage d'indiquer aussi l'hébergeur du backend/site associé s'il y en a un.)

**Si le site traite des données personnelles :**
- Renvoi vers la politique de confidentialité (ne pas dupliquer tout le contenu RGPD ici — un simple lien suffit, mais le point de contact "délégué à la protection des données" si un DPO existe est souvent repris ici aussi)

**Si activité réglementée** (professions libérales réglementées, activités financières, etc.) : numéro d'agrément, autorité de tutelle, référence aux règles professionnelles applicables — demande à l'utilisateur si son activité est concernée, ne le suppose pas.

## Gabarit

```markdown
# Mentions légales

## Éditeur du site
[Dénomination sociale], [forme juridique] au capital de [montant] €
Siège social : [adresse]
RCS [ville] [numéro SIREN]
N° TVA intracommunautaire : [numéro]
Directeur de la publication : [nom]
Contact : [email] — [téléphone]

## Hébergement
[Raison sociale de l'hébergeur]
[Adresse]
[Téléphone]

## Propriété intellectuelle
L'ensemble des contenus présents sur ce site (textes, images, logos, éléments graphiques...) est protégé par le droit de la propriété intellectuelle. Toute reproduction, représentation, modification ou adaptation, totale ou partielle, sans autorisation préalable, est interdite.

## Données personnelles
Le traitement des données personnelles collectées via ce site est décrit dans notre [Politique de confidentialité](lien).

## Médiation de la consommation
(à inclure si l'activité est une vente/prestation de services en B2C)
Conformément aux articles L.616-1 et R.616-1 du Code de la consommation, [nom du médiateur choisi] peut être saisi en cas de litige, à l'adresse suivante : [adresse/site du médiateur].
```

## Pièges fréquents
- Oublier que les mentions légales sont dues même pour un site non marchand (blog, site vitrine, association).
- Confondre "directeur de la publication" (personne physique identifiée, souvent le dirigeant) avec la société elle-même.
- Ne pas mettre à jour l'hébergeur après un changement de prestataire (Vercel, OVH, AWS, Netlify...) — demander explicitement le nom actuel plutôt que de le supposer inchangé.
- Pour une SASU/EURL à associé unique, le nom du dirigeant reste requis comme directeur de publication, même petit.
- Déduire la ville du greffe RCS de l'adresse actuelle du siège social plutôt que de la vérifier séparément — voir la remarque ci-dessus, seule la ville est une information distincte à confirmer, pas le numéro lui-même.
- Traiter un prestataire technique (hébergeur cloud, CDN) comme automatiquement identifiable par son seul nom de produit — le nom légal et l'adresse de l'entité contractante (souvent différente du nom commercial du service, et parfois différente selon que le client est établi en UE ou non) doivent être confirmés, pas déduits. Ne complète jamais une adresse ou une raison sociale complète "plausible" pour rendre le document plus fini en apparence, même à partir d'exemples réalistes — utilise un blanc explicite (`[adresse de l'hébergeur à compléter]`) si l'information n'est pas confirmée.
