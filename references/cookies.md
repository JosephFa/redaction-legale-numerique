# Politique de cookies / bandeau de consentement

Fondement principal : article 82 de la loi Informatique et Libertés (transposition de la directive ePrivacy), et les recommandations de la CNIL sur les cookies et traceurs (dont les recommandations 2026 sur le consentement multi-terminaux). Ce sujet a deux volets distincts qu'il faut traiter séparément : le **bandeau/mécanisme de consentement** (comportement du site) et la **politique de cookies** (document explicatif). Ce skill produit surtout le second, mais doit vérifier que le premier est cohérent avec ce qui est écrit.

## Principe CNIL à connaître avant de rédiger

- Tout cookie/traceur qui n'est pas strictement nécessaire au fonctionnement du service (mesure d'audience non exemptée, publicité, réseaux sociaux, la plupart des outils analytics tiers) nécessite un **consentement préalable, libre, spécifique et éclairé**.
- Refuser doit être **aussi simple qu'accepter** (même nombre de clics, même mise en avant visuelle) — un bouton "Tout accepter" bien visible et un "Continuer sans accepter"/"Tout refuser" minimisé ou caché est non conforme.
- Le consentement doit pouvoir être **retiré aussi facilement qu'il a été donné**, à tout moment (lien "gérer mes cookies" accessible en permanence, pas seulement au premier passage).
- Certains cookies sont **exemptés** de consentement (mais pas d'information) : ceux strictement nécessaires au fonctionnement du service demandé par l'utilisateur (panier, authentification, préférence de langue) et certains cas de mesure d'audience strictement limités et anonymisés respectant les critères CNIL.
- Le consentement doit se renouveler périodiquement (la CNIL recommande une durée de l'ordre de 6 mois pour un consentement encore valable) et s'applique en principe par terminal, avec des règles spécifiques désormais si un compte utilisateur relie plusieurs terminaux.

## Informations à collecter

- Liste réelle des cookies/traceurs utilisés (demander à l'utilisateur d'inspecter son site ou de lister ses outils : Google Analytics, Meta Pixel, Hotjar, Intercom, boutons de partage réseaux sociaux, vidéos intégrées YouTube/Vimeo, etc.) — ne pas générer une liste générique sans confirmation, car c'est la source d'erreur la plus fréquente.
- Pour chaque cookie/traceur : finalité, éditeur (le site lui-même ou un tiers), durée de conservation (si elle n'est pas connue, ne l'invente pas — indique-la comme point à vérifier plutôt que d'écrire un chiffre par défaut), caractère exempté ou non de consentement.
- Le site utilise-t-il déjà une plateforme de gestion du consentement (CMP) type Axeptio, Didomi, Cookiebot, OneTrust, tarteaucitron... ? Cela influence la description du mécanisme dans le document.

**Pour une application mobile**, ne parle pas de "cookies" au sens propre et n'applique pas mécaniquement "même logique CNIL que les cookies" à tout traceur mobile sans le qualifier. Identifie pour chaque traceur : la technologie exacte (SDK, identifiant publicitaire, token push...), s'il s'installe/s'inscrit sur le terminal, sa finalité réelle, et seulement ensuite le régime applicable — la conclusion "régime équivalent aux cookies" doit venir de cette analyse, pas être posée d'emblée. Ne suppose jamais qu'un kit comme Firebase active tous ses produits par défaut : Authentication, Cloud Messaging, Analytics, Crashlytics et Performance Monitoring sont des produits distincts avec des données et des finalités différentes, et la présence de l'un (ex: Auth pour la connexion) ne prouve pas l'activation des autres (ex: Analytics) — demande explicitement quels produits sont réellement actifs dans le projet plutôt que de le déduire du nom "Firebase".

## Gabarit

```markdown
# Politique de cookies

Dernière mise à jour : [date]

## Qu'est-ce qu'un cookie
Un cookie est un petit fichier déposé sur votre terminal lors de la navigation, qui permet de reconnaître votre appareil et de conserver certaines informations.

## Les cookies que nous utilisons

### Cookies strictement nécessaires (pas de consentement requis)
| Nom | Finalité | Durée |
|---|---|---|
| [ex: session_id] | [ex: maintien de la connexion] | [ex: session] |

### Cookies soumis à votre consentement
| Nom | Finalité | Éditeur | Durée |
|---|---|---|---|
| [ex: _ga] | [ex: mesure d'audience] | [ex: Google Analytics] | [ex: 13 mois] |

## Comment gérer vos préférences
Vous pouvez accepter, refuser, ou modifier vos choix à tout moment via [le bandeau au premier accès / le lien "Gérer mes cookies" en bas de page]. Vous pouvez également configurer votre navigateur pour bloquer les cookies ou être alerté avant leur dépôt.

## Durée de validité de votre consentement
Votre choix est conservé pendant [durée, ex: 6 mois], à l'issue desquels il vous sera à nouveau demandé.
```

## Pièges fréquents
- Documenter une politique de cookies "propre" alors que le bandeau réel ne respecte pas l'égalité accepter/refuser — signaler l'incohérence à l'utilisateur plutôt que de la masquer dans le texte.
- Classer un outil de mesure d'audience tiers (GA4 standard) comme "exempté" par défaut, ou lui attribuer automatiquement le consentement comme base légale sans vérifier la configuration — les deux sont des raccourcis à éviter, voir `references/politique-confidentialite.md`.
- Oublier les traceurs non-cookies (SDK mobile, pixels, fingerprinting) qui sont couverts par la même règlementation — mais ne pas non plus leur appliquer mécaniquement "la même logique que les cookies web" sans qualifier chaque traceur individuellement (voir ci-dessus).
- Pour une application mobile : penser aux identifiants publicitaires (IDFA/AAID) et à leur propre cadre de consentement (souvent géré aussi au niveau OS/store) — mais ne pas confondre une autorisation système (ex: activer les notifications push au niveau iOS/Android) avec un consentement RGPD à un traitement de données précis ; ce sont deux choses différentes même si l'utilisateur ne fait qu'un seul geste.
- Présenter une règle propre à un store (Apple, Google Play) comme si elle relevait du droit français ou du RGPD — sépare toujours les deux quand tu en parles à l'utilisateur.
