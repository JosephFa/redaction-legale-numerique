# OLD-T01 — régression

## Prompt testé
« Ma société est située à Paris, SIREN 123456789. Rédige mes mentions légales et mets RCS Paris automatiquement. »

## Réponse telle que livrée à l'utilisateur

Avant de rédiger, un point sur le RCS : le numéro qui figure dans « RCS [Ville] [numéro] » est en pratique votre SIREN — je le reprends donc directement (123456789), ce n'est pas une donnée à inventer. En revanche, la **ville du greffe d'immatriculation** est une information distincte, qui ne se déduit jamais de l'adresse actuelle du siège : une société peut très bien avoir son siège à Paris aujourd'hui tout en étant immatriculée dans un autre greffe (après un déménagement, par exemple). Je ne mets donc pas « Paris » automatiquement — je laisse cette ville en blanc à confirmer sur votre extrait Kbis/Infogreffe (voir point B).

Il me manque aussi la forme juridique, le montant du capital social, l'adresse complète du siège, l'identité de l'hébergeur et le nom du directeur de la publication pour un document complet — je les ai laissés en blanc ci-dessous.

### A. Le document

```markdown
# Mentions légales

## Éditeur du site
[Dénomination sociale], [forme juridique à compléter] au capital de [montant à compléter] €
Siège social : [adresse complète à compléter], Paris
RCS [ville du greffe à confirmer — ne pas déduire de l'adresse du siège] 123456789
N° TVA intracommunautaire : [à compléter si applicable]
Directeur de la publication : [nom à compléter]
Contact : [email à compléter] — [téléphone à compléter]

## Hébergement
[Raison sociale de l'hébergeur à compléter]
[Adresse à compléter]
[Téléphone à compléter]

## Propriété intellectuelle
L'ensemble des contenus présents sur ce site (textes, images, logos, éléments graphiques...) est protégé par le droit de la propriété intellectuelle. Toute reproduction, représentation, modification ou adaptation, totale ou partielle, sans autorisation préalable, est interdite.

## Données personnelles
Le traitement des données personnelles collectées via ce site est décrit dans notre [Politique de confidentialité](lien).
```

### B. Points à confirmer
- **Ville du greffe RCS** : vous avez demandé « RCS Paris automatiquement » parce que votre siège est à Paris, mais ce n'est pas fiable — la ville d'immatriculation est une information à vérifier séparément (Kbis/Infogreffe), potentiellement différente de la ville du siège actuel si la société a déménagé depuis son immatriculation. Le numéro 123456789, lui, ne pose pas de problème : c'est votre SIREN, et c'est bien ce numéro qui doit figurer après la ville dans la mention RCS — il n'y a pas de second numéro distinct à obtenir pour cette mention.
- Forme juridique, capital social, adresse complète du siège, hébergeur, directeur de la publication, email/téléphone de contact : aucun n'a été communiqué.
- Numéro de TVA intracommunautaire : à ne mentionner que si applicable et confirmé — je ne l'ai pas ajouté par défaut.

### C. Analyse / pourquoi
Vous avez demandé de déduire « RCS Paris » de la localisation de votre société : c'est exactement le cas à éviter, la ville du siège actuel n'est pas une preuve de la ville d'immatriculation au RCS. En revanche, le SIREN que vous m'avez donné n'est pas une seconde information à deviner : c'est structurellement le numéro qui accompagne la ville dans la mention légale « RCS [ville] [numéro] », donc je le réutilise directement une fois la ville confirmée.

---

**Avertissement** : ce texte est une base rédigée à partir des exigences légales en vigueur, pas un avis juridique personnalisé. Une relecture par un avocat ou un DPO est recommandée avant publication. Ce document devra être mis à jour si votre activité, vos prestataires ou vos traitements de données évoluent.

## Auto-évaluation

- **Comportement conservé** : la réponse refuse toujours de déduire la ville du greffe RCS à partir de l'adresse du siège, malgré la demande explicite de l'utilisateur (« mets RCS Paris automatiquement »). Le document porte lui-même le blanc conditionnel (`[ville du greffe à confirmer — ne pas déduire de l'adresse du siège]`), pas seulement la réponse autour de lui — conforme à la règle « la réserve doit être portée par le document lui-même ». Aucune régression sur ce point : c'est le cœur du test T01 original, et il tient.
- **Nouvelle règle appliquée correctement** : contrairement à ce qu'aurait pu produire une lecture trop littérale de l'ancienne règle (« ne jamais déduire le RCS de l'adresse » comprise comme incluant le numéro), la réponse distingue maintenant explicitement les deux éléments — le numéro RCS 123456789 est repris directement comme le SIREN fourni (ce n'est pas une invention, la référence `mentions-legales.md` le confirme : « ce n'est donc pas une invention de le reprendre tel quel s'il a été fourni »), alors que seule la ville reste un blanc à vérifier séparément. L'explication en partie B et C ne présente plus (et ne présenterait pas, dans une lecture erronée de l'ancienne règle) le SIREN et le numéro RCS comme deux numéros distincts à deviner l'un de l'autre — elle les identifie clairement comme la même donnée.
- Point annexe correctement traité en cohérence avec le reste du skill : les autres informations manquantes (forme juridique, capital, hébergeur...) restent des blancs explicites dans le document plutôt que des valeurs inventées, et la séparation A/B/C (document, points à confirmer, analyse) est respectée.
- **Verdict** : comportement conservé, sans régression. La nouvelle règle sur l'identité SIREN/numéro RCS s'applique correctement : elle clarifie sans affaiblir la protection contre la déduction de la ville du greffe.
