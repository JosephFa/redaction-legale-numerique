# COH01 — cohérence inter-documents

## Prompt testé

« Rédige en une seule fois les mentions légales, la politique de confidentialité, les CGU et les CGV de notre société. Nom commercial : 'NovaBooks'. Raison sociale exacte : Nova Books Technologies SAS. SIREN 901234567. On est hébergés chez OVH pour le site, mais le SaaS lui-même tourne sur AWS. Abonnement à 19€/mois. »

## Réponse telle que livrée à l'utilisateur

Avant les quatre documents, deux remarques rapides :

1. Vous ne précisez pas si vos clients sont des particuliers (B2C) ou des professionnels (B2B) — cela change le régime du droit de rétractation et des clauses abusives dans les CGV. Je rédige ci-dessous en couvrant les deux hypothèses par des crochets à trancher, plutôt que de choisir une hypothèse à votre place.
2. Vous distinguez vous-même deux hébergements différents — OVH pour le site, AWS pour le SaaS. Je les ai traités comme deux prestataires distincts plutôt que de les fondre en un seul "hébergeur", parce que la mention légale d'hébergement (LCEN) porte sur qui héberge le service de communication au public en ligne, alors que l'infrastructure qui héberge réellement les données de vos utilisateurs (ici AWS) est aussi un sous-traitant au sens RGPD à faire apparaître dans la politique de confidentialité.

Un cinquième document n'a pas été demandé et n'est pas rédigé ici : si votre site ou votre app dépose des cookies ou traceurs non strictement nécessaires (mesure d'audience, publicité...), une politique de cookies dédiée sera probablement aussi nécessaire — dites-le-moi si c'est le cas.

### A. Les documents

```markdown
# Mentions légales

## Éditeur du site
Nova Books Technologies SAS (nom commercial : NovaBooks), société par actions simplifiée (SAS) au capital de [capital social à compléter] €
SIREN : 901234567
RCS : [ville d'immatriculation à compléter] [numéro RCS à compléter — distinct du SIREN, à vérifier sur un extrait Kbis/Infogreffe]
Siège social : [adresse du siège à compléter]
N° TVA intracommunautaire : [à compléter, si applicable]
Directeur de la publication : [nom à compléter]
Contact : [email à compléter] — [téléphone à compléter]

## Hébergement

**Hébergement du site web**
OVH — [raison sociale exacte, adresse et téléphone de l'entité OVH contractante à compléter]

**Hébergement de la plateforme SaaS**
L'application NovaBooks elle-même (le service et les données qui y sont traitées) est hébergée sur l'infrastructure Amazon Web Services (AWS). [Entité AWS exacte contractante — par exemple Amazon Web Services EMEA SARL ou une autre entité du groupe selon la région choisie — et son adresse à confirmer ; le nom du produit "AWS" ne suffit pas à identifier l'entité juridique contractante.]

## Propriété intellectuelle
L'ensemble des contenus présents sur ce site et sur l'application NovaBooks (textes, images, logos, éléments graphiques...) est protégé par le droit de la propriété intellectuelle. Toute reproduction, représentation, modification ou adaptation, totale ou partielle, sans autorisation préalable, est interdite.

## Données personnelles
Le traitement des données personnelles collectées via ce site et l'application NovaBooks est décrit dans notre [Politique de confidentialité](lien).

## Médiation de la consommation
[À inclure si votre clientèle est composée de consommateurs (B2C) — voir points à confirmer.] Conformément aux articles L.616-1 et R.616-1 du Code de la consommation, [nom du médiateur choisi] peut être saisi en cas de litige, à l'adresse suivante : [adresse/site du médiateur — vérifier que le dispositif cité est toujours en vigueur à la date de publication].
```

```markdown
# Politique de confidentialité

Dernière mise à jour : [date]

## Qui sommes-nous
Nova Books Technologies SAS (« NovaBooks »), SIREN 901234567, [adresse du siège à compléter], est responsable du traitement des données décrites ci-dessous.
Contact : [email dédié protection des données à compléter]
[Délégué à la Protection des Données (DPO) : existence à confirmer — voir points à confirmer]

## Quelles données nous collectons et pourquoi

| Finalité | Données concernées | Base légale | Durée de conservation |
|---|---|---|---|
| Création et gestion du compte | nom, email, mot de passe | Exécution du contrat | [durée à compléter, ex: durée du compte + délai à déterminer] |
| Gestion de l'abonnement et facturation | données de facturation, historique de paiement | Exécution du contrat / obligation légale pour les pièces comptables | [durée du compte + délai à déterminer] pour le profil de facturation ; 10 ans pour les pièces comptables elles-mêmes (obligation légale, art. L.123-22 du Code de commerce) |
| Statistiques d'usage de l'application | données d'utilisation, identifiants techniques | [à déterminer selon l'outil et sa configuration réelle — voir points à confirmer] | [à compléter] |
| Support client | contenu des échanges avec le support et informations nécessaires à son bon fonctionnement | Exécution du contrat / intérêt légitime | [à compléter] |

## Avec qui nous partageons vos données
Nous partageons certaines données avec les prestataires suivants, dans la stricte mesure nécessaire à leur mission :
- Amazon Web Services (AWS) — hébergement de l'infrastructure applicative et des données traitées par le service NovaBooks
- [Prestataire de paiement, ex: Stripe — à confirmer] — traitement des paiements
- [Autres prestataires (emailing, support, analytics...) à compléter selon les outils réellement utilisés]

## Transferts hors Union européenne
Selon la région AWS effectivement utilisée pour héberger la plateforme, un transfert de données hors UE/EEE est possible. [Région AWS retenue et mécanisme de transfert applicable (clauses contractuelles types ou autre) à confirmer.]

## Vos droits
Vous disposez des droits suivants sur vos données : accès, rectification, effacement, limitation, portabilité, opposition, et retrait du consentement à tout moment (l'exercice de certains de ces droits dépend de la base légale du traitement concerné). Pour les exercer, contactez-nous à [email]. Nous répondrons dans un délai d'un mois, pouvant être prolongé de deux mois supplémentaires en cas de demande complexe (art. 12 RGPD).
Vous pouvez également introduire une réclamation auprès de la CNIL (www.cnil.fr).

## Sécurité
[Mesures de sécurité en place, en termes généraux — à compléter.]

## Cookies
[Voir notre Politique de cookies, si applicable — non rédigée à ce stade.]

## Modifications
Cette politique peut être mise à jour ; la date de dernière modification figure en haut de ce document.
```

```markdown
# Conditions Générales d'Utilisation

Dernière mise à jour : [date]

## 1. Objet
Les présentes Conditions Générales d'Utilisation (CGU) régissent l'accès et l'utilisation du service NovaBooks, édité par Nova Books Technologies SAS, SIREN 901234567, ci-après « NovaBooks » ou « la Société ».

## 2. Acceptation
[Mécanisme d'acceptation à confirmer — case à cocher, création de compte... Non décrit ici comme existant faute de confirmation ; si aucune case à cocher explicite n'est en place au moment de la souscription, une case dédiée serait une pratique plus solide que l'acceptation implicite — recommandation, pas description de l'existant.]

## 3. Accès au service / Compte utilisateur
[Conditions d'accès, création et sécurité du compte à compléter.]

## 4. Règles d'usage
[Ce qui est interdit, comportements attendus, à compléter selon la nature réelle du service.]

## 5. Propriété intellectuelle
[Répartition des droits sur le contenu de la plateforme et le contenu éventuellement généré par l'utilisateur, à compléter.]

## 6. Disponibilité du service
NovaBooks met en œuvre les moyens raisonnables pour assurer la disponibilité du service, dont l'infrastructure technique repose en tout ou partie sur des prestataires tiers. [Détail de l'engagement de disponibilité — SLA le cas échéant — à compléter ; voir la politique de confidentialité pour l'identification des prestataires d'hébergement.]

## 7. Résiliation par NovaBooks
[Modalités de suspension/résiliation de compte par l'éditeur, à compléter.]

## 8. Responsabilité
[Limitation de responsabilité dans les limites permises par la loi — à rédiger avec l'utilisateur, sans exonérer NovaBooks de ses obligations essentielles.]

## 9. Données personnelles
Voir notre [Politique de confidentialité](lien).

## 10. Droit applicable et litiges
[Droit français, juridiction compétente, sous réserve des règles impératives protectrices du consommateur si votre clientèle est B2C.]

## 11. Modification des CGU
[Modalités de notification en cas de changement, à compléter.]
```

```markdown
# Conditions Générales de Vente

Dernière mise à jour : [date]

## 1. Objet
Les présentes Conditions Générales de Vente (CGV) régissent la souscription à l'abonnement au service NovaBooks, édité par Nova Books Technologies SAS, SIREN 901234567, ci-après « NovaBooks » ou « la Société ».

## 2. Description de l'offre et prix
Abonnement mensuel au service NovaBooks, au prix de 19 € [TTC pour une clientèle B2C / HT à préciser pour une clientèle B2B — voir points à confirmer] par mois.

## 3. Souscription et paiement
[Modalités de commande/souscription et moyens de paiement à compléter.]

## 4. Durée, renouvellement
L'abonnement est souscrit pour une durée de [durée à compléter] et se renouvelle ensuite par tacite reconduction. [Si votre clientèle est B2C : obligation d'informer le consommateur avant la date limite de dénonciation, art. L215-1 du Code de la consommation, à intégrer précisément selon le préavis retenu.]

## 5. Droit de rétractation
[Qualification B2B/B2C non tranchée — voir points à confirmer. Si B2C : délai de 14 jours à compter de la souscription (art. L221-18 et suivants du Code de la consommation), sauf si le Client a expressément demandé l'exécution immédiate du service et renoncé à son droit de rétractation selon des modalités de recueil à confirmer comme existantes avant d'écrire cette exception comme acquise. Si B2B : pas de droit de rétractation légal, sauf concession contractuelle de votre part.]

## 6. Résiliation et remboursement
[Modalités de résiliation par le Client, politique de remboursement — à compléter, en cohérence avec ce qui est réellement configuré dans votre outil de facturation.]

## 7. Garanties légales
NovaBooks étant un service numérique, la garantie de conformité applicable est celle prévue pour les services numériques (articles issus de l'ordonnance n°2021-1247 du 29 septembre 2021), et non le régime des biens. [Ne peut être supprimée par contrat pour un Client consommateur.]

## 8. Médiation de la consommation
[Si clientèle B2C : nom du médiateur retenu et ses coordonnées, à compléter — vérifier que le dispositif cité reste en vigueur à la date de publication.]

## 9. Droit applicable et litiges
[Droit français, juridiction compétente, sous réserve des règles impératives protectrices du consommateur si B2C.]
```

### B. Points à confirmer

- Identité complète : capital social, adresse du siège, numéro RCS et ville d'immatriculation (distincts du SIREN, à obtenir séparément), TVA intracommunautaire le cas échéant, directeur de la publication, email/téléphone de contact.
- Entité contractante exacte et adresse pour OVH et pour AWS — le nom du produit ne suffit pas à identifier l'entité juridique à citer dans les mentions légales (par exemple, AWS peut être contracté via différentes entités du groupe Amazon selon la région).
- **B2B ou B2C ?** C'est la question la plus structurante restée ouverte : elle conditionne le droit de rétractation, la clause de médiation de la consommation, et le régime des clauses abusives. Les documents ci-dessus sont rédigés avec des crochets pour les deux hypothèses plutôt qu'en tranchant à votre place.
- Existence d'un DPO désigné.
- Région(s) AWS effectivement utilisée(s) pour héberger la plateforme et le mécanisme de transfert applicable si hors UE/EEE.
- Mécanisme d'acceptation réel des CGU/CGV au moment de la souscription (case à cocher ou autre) — non décrit comme existant faute de confirmation.
- Outils réellement utilisés pour le paiement, l'emailing, le support, les statistiques — non déduits du seul fait qu'il s'agit d'un SaaS.
- Durées de conservation non légalement fixées (compte, statistiques, support) — aucune n'a été inventée.
- Si le service dépose des cookies/traceurs non strictement nécessaires, une politique de cookies dédiée sera probablement nécessaire en plus de ces quatre documents.

### C. Analyse / pourquoi

J'ai traité l'hébergement du site (OVH) et l'hébergement de l'application/des données (AWS) comme deux informations distinctes plutôt que de les fusionner sous un seul intitulé "hébergeur", parce qu'elles ne répondent pas à la même obligation : la mention légale d'hébergement (LCEN) identifie qui héberge le service de communication au public en ligne, tandis que l'identification d'AWS dans la politique de confidentialité répond à l'obligation de transparence RGPD sur les destinataires des données et les transferts hors UE. Je n'ai en revanche pas fait figurer nommément AWS ou OVH dans les CGU/CGV : ces documents renvoient à la politique de confidentialité pour l'identification des prestataires plutôt que de la dupliquer, ce qui évite un risque de désynchronisation si un hébergeur change à l'avenir.

Sur les durées de conservation des données de facturation, j'ai distingué le profil de facturation du Client (durée à déterminer avec vous) des pièces comptables elles-mêmes, dont la durée de conservation de 10 ans découle d'une obligation légale (Code de commerce) plutôt que d'un choix — cette distinction n'a pas été demandée explicitement mais évite d'annoncer une durée unique pour deux réalités différentes.

---

Ces documents sont une base rédigée à partir des exigences légales en vigueur, pas un avis juridique personnalisé. Une relecture par un avocat ou un DPO est recommandée avant publication, en particulier pour trancher la qualification B2B/B2C qui structure une bonne partie des CGV. Ces textes devront être mis à jour si votre activité, vos sous-traitants ou vos traitements de données évoluent, et les règles citées (médiation de la consommation, seuils DPO) doivent être vérifiées à la date de publication.

## Auto-évaluation

Vérification systématique, document par document, de la présence et de la forme exacte de la raison sociale, du SIREN, et des deux infrastructures d'hébergement.

**Raison sociale "Nova Books Technologies SAS"** : présente à l'identique dans les quatre documents — mentions légales ("Éditeur du site"), politique de confidentialité ("Qui sommes-nous"), CGU (article 1er), CGV (article 1er). Aucune variante fautive relevée (pas de "Novabooks Technologies", pas d'inversion de l'ordre des mots) ; le nom commercial "NovaBooks" est utilisé comme raccourci après la première mention dans chaque document, ce qui est la pratique attendue plutôt qu'une incohérence.

**SIREN "901234567"** : présent à l'identique (même chaîne de dix chiffres, sans espace ni reformatage) dans les quatre documents — mentions légales, politique de confidentialité, CGU, CGV. Pas de divergence de format relevée.

**OVH (hébergement du site)** : présent dans les mentions légales ("Hébergement du site web"). **Absent de la politique de confidentialité.** C'est une divergence réelle que je note ici sans la corriger dans le document livré : la politique de confidentialité ne mentionne qu'AWS dans "Avec qui nous partageons vos données", alors que si le site hébergé chez OVH comporte le moindre formulaire collectant des données personnelles (contact, newsletter, page de connexion redirigeant vers l'app...), OVH devient lui aussi un destinataire de données à faire apparaître à ce titre. Je n'ai pas posé la question de savoir si le site OVH collecte des données personnelles avant d'en tirer la conclusion silencieuse qu'il n'a pas sa place dans la politique de confidentialité — j'ai supposé, sans le vérifier ni le signaler comme hypothèse, que seul AWS était pertinent pour le volet RGPD. C'est exactement le type de simplification que le skill demande d'éviter : traiter "hébergeur du site" et "sous-traitant RGPD" comme automatiquement disjoints sans l'avoir vérifié.

**AWS (hébergement du SaaS)** : présent dans les mentions légales ("Hébergement de la plateforme SaaS") et dans la politique de confidentialité (destinataires + transferts hors UE), avec la même réserve sur l'entité contractante exacte reprise aux deux endroits. Absent, par choix explicite et assumé, des CGU (où seule une clause générique de "disponibilité du service" y fait indirectement référence sans nommer AWS) et des CGV (aucune mention). Ce choix est défendable — les CGU/CGV n'ont pas d'obligation de nommer les sous-traitants techniques — mais il n'a pas été soumis à l'utilisateur comme un arbitrage : je l'ai tranché seul, sans le signaler explicitement en section B ou C comme un choix de rédaction plutôt qu'une évidence.

**Bilan** : la raison sociale et le SIREN sont strictement identiques et complets dans les quatre documents où ils sont pertinents — aucune divergence trouvée sur ce point. En revanche, sur les deux infrastructures d'hébergement, une vraie omission ressort : OVH n'apparaît que dans les mentions légales et pas dans la politique de confidentialité, alors que sa pertinence RGPD dépend d'une question (le site OVH collecte-t-il des données personnelles ?) que je n'ai jamais posée à l'utilisateur ni signalée comme non résolue. C'est un oubli de cohérence, pas une invention de fait, mais il aurait dû être soit corrigé dans le document, soit explicitement signalé en section B — il ne l'est dans aucun des deux.
