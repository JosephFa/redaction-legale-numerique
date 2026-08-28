# klaro — régression post-correction

## Prompt testé

> Je lance mon SaaS Klaro (outil de gestion de projet pour PME), édité par ma société KLARO SAS, SIREN 913 456 782, siège au 12 rue de la Paix 75002 Paris, capital 5000€, hébergé sur Vercel + Supabase (EU). On facture un abonnement mensuel via Stripe, on utilise Google Analytics 4 et Intercom pour le support client. Je suis directeur de la publication. Peux-tu me rédiger les mentions légales et la politique de confidentialité ?

## Réponse telle que livrée à l'utilisateur

Avant de rédiger, quelques précisions : vous me donnez le SIREN de KLARO SAS, qui peut servir tel quel de numéro RCS (`RCS [ville] 913 456 782`) — mais je n'ai pas la **ville du greffe d'immatriculation**, qui ne se déduit pas automatiquement de l'adresse du siège (une société peut être immatriculée dans un greffe différent, notamment après un déménagement) : je l'ai laissée en blanc à vérifier sur votre Kbis. Je n'ai pas non plus votre nom (pour le directeur de la publication, alors que vous m'indiquez occuper cette fonction), votre email de contact, ni le détail de qui contracte exactement avec Vercel, Supabase, Stripe, Google et Intercom — j'ai laissé ces points en blanc plutôt que de les compléter avec des valeurs plausibles. Vous trouverez la liste complète des points à vérifier en partie B.

### A. Mentions légales

```markdown
# Mentions légales

## Éditeur du site
KLARO SAS, société par actions simplifiée au capital de 5 000 €
Siège social : 12 rue de la Paix, 75002 Paris
RCS [ville du greffe à vérifier — non déductible de l'adresse du siège] 913 456 782
N° TVA intracommunautaire : [à compléter si applicable — non mentionné à ce stade]
Directeur de la publication : [nom à compléter]
Contact : [email à compléter] — [téléphone à compléter]

## Hébergement
[Raison sociale et adresse de l'entité Vercel contractante à compléter]
[Raison sociale et adresse de l'entité Supabase contractante à compléter]

## Propriété intellectuelle
L'ensemble des contenus présents sur ce site (textes, images, logos, éléments graphiques...) est protégé par le droit de la propriété intellectuelle. Toute reproduction, représentation, modification ou adaptation, totale ou partielle, sans autorisation préalable, est interdite.

## Données personnelles
Le traitement des données personnelles collectées via Klaro est décrit dans notre [Politique de confidentialité](lien).

## Médiation de la consommation
[À inclure uniquement si Klaro est souscrit par des consommateurs personnes physiques — à confirmer selon le profil réel de vos clients PME ; le cas échéant : nom du médiateur et adresse à compléter.]
```

### A. Politique de confidentialité

```markdown
# Politique de confidentialité

Dernière mise à jour : [date]

## Qui sommes-nous
KLARO SAS, responsable du traitement des données décrites ci-dessous.
Contact : [email dédié à compléter]
[DPO : à déterminer — voir point B]

## Quelles données nous collectons et pourquoi

| Finalité | Données concernées | Base légale | Durée de conservation |
|---|---|---|---|
| Création et gestion du compte utilisateur | Identité, email, mot de passe | Exécution du contrat | [Durée du compte + durée à déterminer] |
| Facturation de l'abonnement (Stripe) | Données de facturation transmises à Stripe | Exécution du contrat / obligation légale (comptabilité) | [Durée légale de conservation comptable — à confirmer] |
| Mesure d'audience (Google Analytics 4) | Données de navigation, identifiants techniques | [Base légale à confirmer selon le paramétrage retenu — consentement en mode standard, ou exemption si mesure d'audience strictement anonymisée au sens des critères CNIL] | [Durée à déterminer — le paramètre de rétention par défaut de GA4 est un réglage technique, pas une durée légale] |
| Support client (Intercom) | Contenu des échanges avec le support et informations nécessaires à son bon fonctionnement | Exécution du contrat / intérêt légitime | [Durée à déterminer] |

## Avec qui nous partageons vos données
- Stripe — traitement des paiements et de la facturation
- Google (Google Analytics 4) — mesure d'audience
- Intercom — support client
- Vercel — hébergement de l'application
- Supabase — hébergement de la base de données et authentification (infrastructure UE selon vos indications — à confirmer pour l'ensemble des composants, y compris Vercel)

## Transferts hors Union européenne
Stripe, Google (Analytics 4) et Intercom sont des prestataires dont le siège ou une partie de l'infrastructure est situé hors UE/EEE ; un transfert de données hors UE est donc probable pour ces trois outils, mais le mécanisme exact (clauses contractuelles types ou autre) n'a pas été confirmé et doit l'être auprès de chaque prestataire. Concernant Supabase, vous indiquez un hébergement UE : à confirmer que l'ensemble des traitements associés (sauvegardes, sous-traitants ultérieurs) reste également en UE. Le cas de Vercel (hébergement du front) n'est pas précisé comme étant en UE et doit être vérifié séparément.

## Vos droits
Vous disposez des droits suivants sur vos données : accès, rectification, effacement, limitation, portabilité, opposition, et retrait du consentement à tout moment (l'exercice de certains de ces droits dépend de la base légale du traitement concerné). Pour les exercer, contactez-nous à [email]. Nous répondrons dans un délai d'un mois, pouvant être prolongé de deux mois supplémentaires en cas de demande complexe (art. 12 RGPD).
Vous pouvez également introduire une réclamation auprès de la CNIL (www.cnil.fr).

## Sécurité
[Mesures de sécurité effectivement en place — à décrire en termes généraux une fois confirmées, sans détail d'architecture exploitable.]

## Cookies
Voir notre [Politique de cookies](lien).

## Modifications
Cette politique peut être mise à jour ; la date de dernière modification figure en haut de ce document.
```

### B. Points à confirmer
- Ville du greffe d'immatriculation RCS (à vérifier sur Infogreffe/Kbis — ne pas la déduire de l'adresse du siège à Paris).
- Votre nom, en tant que directeur de la publication, et l'email/téléphone de contact à afficher.
- Numéro de TVA intracommunautaire, si applicable.
- Raison sociale et adresse exactes des entités contractantes pour Vercel et Supabase (le nom du produit ne suffit pas à les identifier juridiquement), et confirmation que l'hébergement Vercel est également localisé en UE.
- Profil réel de vos clients (PME en tant que personnes morales uniquement, ou souscription possible par des indépendants/particuliers assimilés consommateurs ?) — cela conditionne si la clause de médiation de la consommation doit figurer dans les mentions légales.
- Configuration exacte de Google Analytics 4 (mode standard avec consentement, ou mesure d'audience exemptée) — la base légale du traitement en dépend directement.
- Mécanisme de transfert hors UE applicable pour Stripe, Google/GA4 et Intercom (clauses contractuelles types généralement, mais à confirmer prestataire par prestataire).
- Durées de conservation réelles par finalité (compte, facturation, support).
- Existence ou non d'un DPO désigné.
- CGU et CGV : non demandées ici, mais probablement nécessaires puisque Klaro facture un abonnement — à traiter séparément si vous le souhaitez.

### C. Analyse
Sur le point RCS/SIREN : la nouvelle règle du skill s'applique correctement ici — le SIREN que vous fournissez (913 456 782) peut être repris tel quel comme numéro figurant dans la mention RCS, ce n'est pas une invention. Ce qui manque et reste un blanc explicite, c'est uniquement la **ville du greffe**, qui est une information distincte de l'adresse du siège et ne doit jamais en être déduite.

Le point le plus significatif à traiter en priorité reste les **transferts hors UE** : trois prestataires (Stripe, Google, Intercom) sont concernés potentiellement, et Vercel n'est pas confirmé comme purement UE malgré votre mention "(EU)" qui semble ne viser que Supabase — c'est le risque RGPD le plus concret pour Klaro à ce stade, davantage que les blancs d'identité qui sont de simples formalités à compléter.

Aucun élément dans votre message ne permet à ce stade de conclure à une obligation de désigner un DPO ; cette analyse serait à réévaluer si le volume d'utilisateurs ou l'ampleur du traitement augmentaient significativement.

**Avertissement** : ce texte est une base rédigée à partir des exigences légales en vigueur, pas un avis juridique personnalisé. Une relecture par un avocat ou un DPO est recommandée avant publication. Le document devra être mis à jour si vos sous-traitants ou traitements évoluent, et les règles citées (seuils, plateformes de médiation) doivent être vérifiées à la date de publication.

## Auto-évaluation

**Comportement conservé, sans régression** :
- Les trois documents (mentions légales, politique de confidentialité) restent structurés en blocs A/B/C conformément à l'Étape 5 — aucune note de production n'est collée dans le texte juridique lui-même.
- Aucune invention sur l'entité contractante exacte de Vercel/Supabase/Stripe/Intercom : blancs explicites conservés, conformément au Piège 1.
- Le tableau des traitements RGPD distingue bien Stripe/GA4/Intercom, avec bases légales différenciées et durées non inventées.
- Les transferts hors UE sont signalés comme probables mais avec mécanisme à confirmer, sans affirmation catégorique — conforme au Piège 1 et à la checklist "Transferts hors Union européenne" de `politique-confidentialite.md`.
- L'avertissement standard est repris en fin de réponse, hors du document.

**Nouvelle règle RCS/SIREN — application vérifiée correcte** : le SIREN fourni (913 456 782) est repris directement comme numéro RCS, sans que cela soit traité comme une invention — exactement ce que prescrit la correction de `mentions-legales.md` ("le numéro qui figure dans la mention RCS Ville numéro est, en pratique, le SIREN de la société [...] ce n'est donc pas une invention de le reprendre tel quel"). Seule la ville du greffe, absente du prompt, est isolée comme blanc explicite distinct — la règle "à ne jamais déduire de l'adresse du siège social" est respectée : la réponse ne complète pas silencieusement "Paris" pour la ville du greffe alors que le siège est à Paris, ce qui aurait été l'erreur classique que la correction vise à éviter.

Aucune régression détectée sur le reste du comportement attendu (tableau des traitements, réserve sur les transferts, structuration A/B/C, avertissement).
