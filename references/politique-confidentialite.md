# Politique de confidentialité (RGPD)

Fondement principal : articles 12 à 14 du RGPD (règlement UE 2016/679), et les lignes directrices/recommandations de la CNIL sur la transparence et l'information des personnes. Ce document explique à toute personne dont les données sont traitées (utilisateur, prospect, visiteur...) qui traite ses données, pourquoi, comment, combien de temps, et quels sont ses droits.

C'est le document le plus sensible à "inventer" : contrairement aux mentions légales qui sont des faits d'identification simples, une politique de confidentialité décrit des **traitements réels**. Une politique qui prétend ne pas faire de profilage alors que le produit en fait, ou qui omet un sous-traitant qui reçoit effectivement des données, expose l'entreprise plus qu'elle ne la protège. Pose des questions précises sur ce que le produit fait réellement plutôt que de partir d'une liste générique.

Trois catégories de détails sont particulièrement à risque d'être inventées parce qu'elles rendent le texte plus convaincant — résiste à la tentation :
- **des mesures de sécurité techniques non confirmées** (ex: écrire qu'un mot de passe est "chiffré" — en pratique souvent haché, mais tu ne le sais pas non plus sans confirmation) ;
- **une architecture de paiement ou technique précise** (ex: affirmer que les données de carte "ne transitent jamais par nos serveurs" suppose une intégration Stripe précise — Checkout, Elements, ou autre — que tu ne connais pas ; préfère "les données de paiement sont traitées par Stripe selon les modalités applicables au parcours de paiement utilisé") ;
- **des durées de conservation chiffrées non fournies** (voir plus bas).

Un prestataire nommé par l'utilisateur (Stripe, Google, Intercom, Firebase...) ne te dit pas automatiquement quelle entité juridique exacte le contracte, quelles données précises il reçoit, ni son rôle RGPD : prestataire technique, entité contractante et rôle RGPD (sous-traitant, responsable conjoint, tiers) sont trois questions distinctes à examiner séparément plutôt qu'à déduire les unes des autres.

## Informations à collecter

**Identité du responsable de traitement**
- Qui décide des finalités et moyens du traitement (souvent l'éditeur du produit — reprendre les infos des mentions légales)
- Existe-t-il un DPO désigné ? Coordonnées si oui. L'obligation de désignation dépend de critères précis (autorité publique, suivi régulier et systématique à grande échelle, traitement à grande échelle de données sensibles) que le prompt d'un utilisateur ne renseigne presque jamais complètement (volume d'utilisateurs, nature exacte des traitements, ampleur réelle). **Ne conclus jamais catégoriquement à l'absence d'obligation** faute d'information suffisante — formule plutôt : *"sur la base des informations communiquées, aucun élément ne permet à ce stade d'identifier une obligation de désignation d'un DPO ; cette analyse doit être réévaluée au regard de l'activité et de l'ampleur réelles des traitements."* Une taille d'entreprise ou de projet perçue comme "petite" n'est pas en soi un critère juridique.

**Pour chaque traitement de données réalisé** (à explorer un par un — ne pas supposer qu'il n'y en a qu'un) :
- Quelles données sont collectées ? (identité, contact, données de connexion, données de paiement, contenu généré par l'utilisateur, géolocalisation, données de santé, biométrie...)
- Dans quel but précis ? ("créer et gérer le compte utilisateur", "envoyer la newsletter", "établir des statistiques d'usage", "prévenir la fraude"...)
- Quelle est la base légale ? (consentement, exécution du contrat, obligation légale, intérêt légitime, intérêt public, sauvegarde des intérêts vitaux — le RGPD exige une base légale par finalité, jamais "au cas où")
- La fourniture de la donnée est-elle obligatoire pour utiliser le service, ou optionnelle ?
- Combien de temps la donnée est-elle conservée, et sur quel critère (ex: "durée de la relation contractuelle + 3 ans", "jusqu'à suppression du compte") — **si cette durée n'a pas été fournie ou n'est pas juridiquement établie (ex: obligations comptables), ne l'invente pas parce qu'elle "semble raisonnable"**. Une durée par défaut visible dans la console d'un outil (ex: la fenêtre de rétention configurée dans Google Analytics 4) est un paramètre technique, pas une obligation légale généralisable — ne la présente jamais comme telle ; indique plutôt le paramètre réellement configuré (à confirmer par l'utilisateur) ou signale la durée comme un point à déterminer.

Ne déduis pas non plus la base légale d'un outil à partir de sa seule catégorie. La présence de Google Analytics 4 ne veut pas automatiquement dire "base légale = consentement" : cela dépend de la configuration retenue (mode standard vs mesure d'audience strictement anonymisée exemptée selon les critères CNIL), des finalités réellement activées, et du régime applicable aux traceurs déposés. Vérifie ou demande la configuration avant de trancher.

**Destinataires et sous-traitants**
- Qui reçoit les données en interne (équipes) et en externe (prestataires : hébergeur, emailing, paiement, analytics, support client, CRM...) — lister les catégories, idéalement les outils réels utilisés (Stripe, Mailchimp, Intercom, Google Analytics...) plutôt qu'une formule vague
- Pour chaque outil, distingue ce qui a été confirmé (le nom de l'outil, sa fonction générale) de ce que tu déduis (les données précises qu'il reçoit, ses fonctionnalités activées). Un outil de support comme Intercom peut recevoir des métadonnées techniques variées selon l'intégration — ne les énumère pas comme des faits établis si l'utilisateur ne les a pas confirmées ; formule au niveau de généralité que les faits permettent ("contenu des échanges avec le support et informations nécessaires à son bon fonctionnement" plutôt qu'une liste détaillée inventée).

**Transferts hors Union européenne**
- Un des sous-traitants/outils est-il situé (ou héberge-t-il des données) hors UE/EEE ? Si oui, quel mécanisme encadre le transfert (clauses contractuelles types, décision d'adéquation...) — beaucoup d'outils américains courants (analytics, emailing, hébergement cloud) sont concernés, il faut le demander explicitement.

**Droits des personnes**
- Standard RGPD : droit d'accès, de rectification, d'effacement, à la limitation, à la portabilité, d'opposition, et droit de retirer son consentement à tout moment — mais rappelle (au moins en une phrase) que l'exercice concret de certains droits (opposition, portabilité, retrait du consentement) dépend de la base légale et des conditions applicables à chaque traitement ; ne présente pas une liste uniforme comme s'appliquant identiquement à toutes les données.
- Comment exercer ces droits en pratique (email dédié, formulaire) ?
- Droit d'introduire une réclamation auprès de la CNIL
- Le délai de réponse de principe est d'un mois, mais l'article 12 du RGPD permet une prolongation de deux mois supplémentaires selon la complexité ou le nombre de demandes — mentionne cette possibilité plutôt que d'annoncer un délai d'un mois sans nuance.

**Sécurité**
- Mesures de sécurité mises en place (à décrire simplement, sans détailler l'architecture technique de façon exploitable) — chiffrement, contrôle d'accès, etc.

**Cookies/traceurs**
- Renvoyer vers la politique de cookies dédiée (`references/cookies.md`) plutôt que de tout dupliquer ici, sauf si l'utilisateur préfère un document unique — dans ce cas, fusionner les deux gabarits.

**Mineurs**
- Le service est-il susceptible d'être utilisé par des mineurs ? Si oui, quelles précautions (âge minimum, consentement conjoint du mineur et d'un titulaire de l'autorité parentale en-deçà du seuil applicable en France pour les services de la société de l'information basés sur le consentement — ce seuil, comme les autres seuils réglementaires cités dans ce skill, doit être vérifié à la date de publication plutôt que traité comme définitivement acquis) ?

**Analyse d'impact (AIPD)**
- Certains traitements présentent un risque élevé nécessitant une analyse d'impact relative à la protection des données avant leur mise en œuvre (article 35 RGPD), en particulier quand plusieurs critères de risque se cumulent (traitement à grande échelle de données de santé ou d'autres catégories particulières, suivi systématique et régulier, personnes vulnérables dont des mineurs). Si le produit combine plusieurs de ces critères, signale qu'une AIPD est probablement due comme un point à traiter séparément de la rédaction de la politique elle-même — ne le passe pas sous silence même si l'utilisateur ne l'a pas demandé, et même si tu ne peux pas la réaliser toi-même.

## Gabarit

```markdown
# Politique de confidentialité

Dernière mise à jour : [date]

## Qui sommes-nous
[Nom de l'entité], responsable du traitement des données décrites ci-dessous.
Contact : [email dédié protection des données]
[Le cas échéant : Délégué à la Protection des Données (DPO) : [nom/contact]]

## Quelles données nous collectons et pourquoi

| Finalité | Données concernées | Base légale | Durée de conservation |
|---|---|---|---|
| [ex: Création et gestion du compte] | [ex: nom, email, mot de passe] | [ex: exécution du contrat] | [ex: durée du compte + 1 an] |
| ... | ... | ... | ... |

## Avec qui nous partageons vos données
Nous partageons certaines données avec les prestataires suivants, dans la stricte mesure nécessaire à leur mission :
- [Prestataire, ex: Stripe] — [rôle, ex: traitement des paiements]
- [Prestataire] — [rôle]

## Transferts hors Union européenne
[Décrire les transferts identifiés et le mécanisme juridique applicable, ou indiquer qu'il n'y en a pas.]

## Vos droits
Vous disposez des droits suivants sur vos données : accès, rectification, effacement, limitation, portabilité, opposition, et retrait du consentement à tout moment (l'exercice de certains de ces droits dépend de la base légale du traitement concerné). Pour les exercer, contactez-nous à [email]. Nous répondrons dans un délai d'un mois, pouvant être prolongé de deux mois supplémentaires en cas de demande complexe (art. 12 RGPD).
Vous pouvez également introduire une réclamation auprès de la CNIL (www.cnil.fr).

## Sécurité
[Mesures de sécurité en place, en termes généraux.]

## Cookies
Voir notre [Politique de cookies](lien).

## Modifications
Cette politique peut être mise à jour ; la date de dernière modification figure en haut de ce document.
```

## Pièges fréquents
- Lister une base légale unique pour tout le document au lieu d'une base légale par finalité.
- Oublier les outils tiers "invisibles" (Google Analytics, Meta Pixel, Intercom, Sentry, Mixpanel) qui sont pourtant des destinataires de données et souvent hors UE.
- Mentionner un droit à la portabilité pour des données qui ne sont pas fournies par la personne elle-même ou pas traitées sur base contractuelle/consentement (le droit à la portabilité a un champ plus restreint que les autres droits — ne pas s'y attarder si le cas ne s'applique pas, mais ne pas non plus l'omettre par principe).
- Rédiger une politique statique alors que les traitements évoluent souvent (nouvel outil analytics, nouvelle fonctionnalité) — rappeler à l'utilisateur que ce document doit vivre avec le produit.
- **Qualifier "toute donnée client = sous-traitance"** dans un SaaS B2B sans regarder traitement par traitement. Si l'éditeur détermine lui-même les finalités de certains traitements portant sur les données de ses clients (sécurité, prévention de la fraude, statistiques internes, obligations légales), il en reste responsable de traitement pour ceux-là — seule la partie où il exécute des instructions du client sur les données que celui-ci lui confie relève du régime sous-traitant (art. 28, avec DPA). Applique cette distinction traitement par traitement, jamais en bloc.
- Ajouter en fin de document un bloc "informations manquantes à compléter avant publication" ou une "note de livraison" : ce type de note de production **n'a pas sa place dans le document juridique lui-même**. Utilise des blancs explicites (`[à compléter]`) directement dans le texte pour les données ponctuelles manquantes, et mets la liste des points à vérifier dans ta réponse à l'utilisateur, pas dans le fichier livré.
