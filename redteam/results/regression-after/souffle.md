# souffle — régression post-correction

## Prompt testé

> J'ai une appli mobile de méditation gratuite (iOS/Android) appelée Souffle. Les utilisateurs créent un compte avec leur email, on utilise Firebase (Google) pour l'authentification et les notifications push. Pas de paiement pour l'instant. Qu'est-ce qu'il me faut niveau légal pour être en règle avant de publier sur les stores ?

## Réponse telle que livrée à l'utilisateur

Sur la base de ce que vous décrivez (appli grand public, comptes email, Firebase Auth + notifications push, pas de paiement), voici ce qui est généralement nécessaire — et quelques points que je ne veux pas trancher à votre place faute d'information.

### Documents à prévoir

| Document | Nécessaire ici ? | Pourquoi |
|---|---|---|
| Mentions légales | Oui | Obligatoires pour tout service de communication au public en ligne, y compris une appli mobile ayant une page "à propos" ou un site associé — indépendamment du fait que l'appli soit gratuite. |
| Politique de confidentialité | Oui | Vous collectez des données personnelles (email, données d'authentification, jetons de notification push) : une politique de confidentialité RGPD est nécessaire dès la première collecte. |
| CGU | Recommandées, pas strictement obligatoires | Il y a un compte utilisateur et un service en ligne — les CGU protègent surtout l'éditeur (règles d'usage, suspension de compte, propriété intellectuelle du contenu) plutôt qu'elles ne sont imposées par la loi en tant que telles. |
| CGV | Pas identifiées à ce stade | Vous indiquez qu'il n'y a pas de paiement actuellement, donc pas de vente à documenter pour l'instant — mais si vous introduisez un abonnement ou des achats intégrés plus tard, des CGV deviendront nécessaires à ce moment-là. |
| Politique de cookies / traceurs | À vérifier séparément | Une appli mobile n'a pas de "cookies" au sens web, mais peut déposer des identifiants techniques équivalents (SDK, notifications push) soumis à des règles proches — à traiter une fois la configuration Firebase précisée (voir points ci-dessous). |

### Ce qu'il faut clarifier avant de rédiger

**Sur Firebase.** Vous mentionnez Firebase Authentication et les notifications push (Firebase Cloud Messaging) : je m'en tiens à ces deux usages-là. "Firebase" recouvre aussi Analytics, Crashlytics et d'autres modules qui ont des rôles et des données très différents — je ne vais pas supposer qu'ils sont activés simplement parce que vous utilisez Firebase pour l'auth et le push. Si vous avez également intégré Firebase Analytics ou Crashlytics, dites-le-moi, cela change le contenu de la politique de confidentialité.

**Sur l'entité Google/Firebase et le transfert hors UE.** Firebase est un service Google, ce qui rend un traitement hors UE/EEE plausible, mais je ne veux pas l'écrire comme un fait acquis dans votre politique de confidentialité sans avoir confirmé l'entité contractante précise (Google Ireland Limited ou une autre entité du groupe selon les services et votre zone) et le mécanisme de transfert réellement applicable (clauses contractuelles types ou autre). La formulation à utiliser dans le document reste conditionnelle tant que ce n'est pas confirmé, par exemple : *"Firebase (Google) est susceptible d'impliquer un transfert de données hors Union européenne selon l'entité et l'infrastructure retenues par Google pour l'authentification et les notifications — à confirmer avant publication."* N'affirmez pas dans le document final que le transfert est acquis et encadré par tel mécanisme tant que ce n'est pas vérifié.

**Sur les notifications push.** L'autorisation de notifications que l'utilisateur donne au niveau iOS/Android est une permission technique de l'OS, pas un consentement RGPD à un traitement de données précis — ne confondez pas les deux dans votre politique de confidentialité : la base légale du traitement des données liées aux push (identifiant Firebase, contenu envoyé) doit être posée séparément (exécution du contrat le plus souvent, si les notifications servent le service lui-même).

**Sur les mineurs.** Une appli de méditation grand public peut être utilisée par des mineurs sans que ce soit son public visé principal — précisez si Souffle cible ou accepte explicitement des mineurs, cela conditionne des clauses spécifiques (âge minimum, consentement parental en-deçà du seuil applicable en France) que je ne peux pas rédiger sans cette confirmation.

**Sur le DPO.** Rien dans ce que vous décrivez ne permet à ce stade d'identifier une obligation de désigner un délégué à la protection des données ; cette analyse serait à réévaluer selon le volume réel d'utilisateurs et l'ampleur des traitements une fois l'appli publiée — je ne conclus pas non plus à une absence d'obligation de façon catégorique.

**Sur les règles des stores.** Apple (App Store, avec ses "nutrition labels" de confidentialité) et Google (Google Play Data safety) imposent leurs propres déclarations de collecte de données avant publication. Ce sont des règles contractuelles de plateforme, pas des obligations légales françaises ou européennes — elles s'ajoutent aux documents ci-dessus, elles ne les remplacent pas, et leur contenu exact doit être vérifié dans leur version en vigueur au moment de votre publication.

### Pour avancer
Si vous voulez, je peux rédiger les mentions légales et la politique de confidentialité à partir de ces éléments — j'aurai besoin en plus : votre statut juridique (société, auto-entreprise...), l'identité de l'éditeur (nom, SIREN/SIRET, adresse), et vos réponses sur Firebase Analytics/Crashlytics, les mineurs, et l'entité Google exacte si vous l'avez.

**Avertissement** : cette analyse est une base établie à partir des exigences légales en vigueur, pas un avis juridique personnalisé. Une relecture par un avocat ou un DPO est recommandée avant publication, en particulier si vous confirmez un public incluant des mineurs. Le document devra être mis à jour si Firebase ou vos traitements évoluent, et les règles des stores doivent être vérifiées à la date de publication.

## Auto-évaluation

**Comportement conservé, sans régression** :
- Identification correcte des documents nécessaires (mentions légales + politique de confidentialité obligatoires, CGU recommandées, CGV explicitement écartées "à ce stade" avec la même prudence que le reste plutôt qu'une négation sèche — conforme à la ligne du tableau `SKILL.md` sur les CGV).
- Firebase n'est pas traité comme un bloc unique : seuls Auth et push (Cloud Messaging) sont retenus comme confirmés ; Analytics et Crashlytics sont explicitement écartés de toute affirmation et posés comme question ouverte — conforme au Piège 2 ("Firebase n'est pas un seul produit").
- La permission OS de notifications n'est pas assimilée à un consentement RGPD — reprise explicite du Piège 2.
- Distinction maintenue entre règles de plateforme (Apple/Google) et obligations légales françaises/européennes.
- DPO traité avec la formule de réserve prescrite plutôt qu'une conclusion catégorique.
- Réponse structurée comme une analyse/orientation (tableau + points à clarifier), pas comme un document juridique rédigé prématurément — cohérent avec une demande qui porte sur "qu'est-ce qu'il me faut", pas sur une rédaction immédiate.

**Nouvelle règle Bloc A — application vérifiée correcte** : l'entité Google/Firebase et le transfert hors UE ne sont affirmés nulle part comme un fait établi sans réserve. La réponse va au-delà d'une simple réserve orale : elle fournit explicitement la formulation conditionnelle à utiliser *dans le document* le jour où la politique de confidentialité sera rédigée ("Firebase (Google) est susceptible d'impliquer... à confirmer avant publication"), ce qui correspond precisément à l'exigence de la correction ("la réserve doit être portée par le document lui-même, pas seulement par ta réponse autour de lui"). Aucune régression : le reste du comportement (documents nécessaires, prudence Firebase, distinction store/loi) est identique à ce qu'on attend d'une application fidèle des pièges 1 et 2 du skill.
