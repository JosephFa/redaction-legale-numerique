# AUD05 — audit de document

## Document soumis

Message utilisateur d'accompagnement :
> Peux-tu auditer cet accord de sous-traitance ? On l'a fait signer à nos clients il y a un an.

Document :
```
Accord de sous-traitance entre le Client et DataSync (sous-traitant), pour le traitement des données de facturation.

DataSync peut faire appel aux sous-traitants ultérieurs de son choix sans en informer le Client. DataSync s'engage à mettre en œuvre des mesures de sécurité raisonnables. En cas de fin de contrat, DataSync conserve les données pendant une durée illimitée pour ses propres archives.
```

## Réponse telle que livrée à l'utilisateur

Avant la grille, une qualification rapide : ce document encadre une relation où DataSync traite, pour le compte du Client, des données de facturation — DataSync est donc bien sous-traitant au sens de l'article 28 du RGPD, et le Client responsable de traitement. Le texte est très court (trois phrases) : l'essentiel des obligations de l'article 28 en est simplement absent, plutôt qu'insuffisamment rédigé.

Voici la grille d'audit (🟢 présent et correct — 🟠 présent mais incomplet/à vérifier — 🔴 absent alors qu'obligatoire ou risqué — ⚪ non applicable) :

| Clause / sujet | Statut | Pourquoi |
|---|---|---|
| Identification des parties et de l'objet | 🟠 | Les parties et la finalité (traitement des données de facturation) sont identifiées, mais sans durée du traitement, ni catégories précises de personnes concernées, ni description du service dans le cadre duquel le traitement a lieu |
| Traitement sur instruction documentée du Client | 🔴 | Absent — aucune clause n'impose à DataSync de ne traiter les données que sur instruction documentée du Client (art. 28.3.a) |
| Engagement de confidentialité du personnel de DataSync | 🔴 | Absent — rien ne garantit que les personnes autorisées à traiter les données chez DataSync sont engagées à la confidentialité (art. 28.3.b) |
| Mesures de sécurité (art. 32 RGPD) | 🟠 | Une clause existe ("mesures de sécurité raisonnables") mais reste générique — aucun renvoi à une annexe ni description des mesures techniques et organisationnelles réellement mises en œuvre |
| Recours à des sous-traitants ultérieurs | 🔴 | La clause autorise DataSync à y recourir "sans en informer le Client" — ceci contredit directement l'art. 28.2 du RGPD, qui exige une autorisation écrite préalable (spécifique ou générale, avec droit d'opposition du responsable) avant tout recours à un sous-traitant ultérieur. Ce n'est pas une simple lacune : la clause affirme l'inverse de ce que la loi impose |
| Assistance pour les demandes d'exercice des droits des personnes concernées | 🔴 | Absent (art. 28.3.e) |
| Notification en cas de violation de données | 🔴 | Absent — aucun délai ni canal de notification au Client n'est prévu, alors que l'art. 28.3.f impose au sous-traitant d'aider le responsable à respecter ses propres obligations de notification |
| Sort des données à la fin du contrat | 🔴 | DataSync "conserve les données pendant une durée illimitée pour ses propres archives" — ceci contredit directement l'obligation de suppression ou de restitution des données à l'issue de la prestation, au choix du responsable (art. 28.3.g). Là encore, la clause énonce l'inverse de l'obligation légale plutôt que de simplement l'omettre |
| Mise à disposition des informations nécessaires / droit d'audit du Client | 🔴 | Absent (art. 28.3.h) |
| Transferts hors Union européenne | ⚪ | Non abordé dans le document ; aucune information communiquée ne permet de dire s'il y en a — à vérifier séparément, notamment auprès des éventuels sous-traitants ultérieurs |

**Deux clauses existantes posent un problème plus grave qu'une simple absence — elles autorisent explicitement ce que la loi encadre ou interdit :**

1. **Sous-traitants ultérieurs sans autorisation ni information** : DataSync peut aujourd'hui confier tout ou partie des données de facturation à un tiers de son choix sans même en informer le Client, ce qui prive ce dernier de toute maîtrise sur la chaîne de sous-traitance — à l'inverse de ce qu'exige l'art. 28.2.
2. **Conservation illimitée en fin de contrat** : cette clause entre frontalement en conflit avec l'obligation de suppression/restitution des données à l'issue du contrat (art. 28.3.g). "Pour ses propres archives" ne constitue pas une base valable de conservation par le sous-traitant après la fin de la prestation — c'est une conservation pour les finalités propres de DataSync, ce qui sort du cadre de la sous-traitance.

À cela s'ajoute l'absence totale de clause de notification de violation de données : combinée à la liberté totale laissée à DataSync sur ses sous-traitants ultérieurs, le Client n'a aujourd'hui aucun moyen contractuel d'être informé si un incident survient plus bas dans la chaîne — ce qui l'empêche à son tour de respecter ses propres obligations (notification à la CNIL sous 72h le cas échéant, information des personnes concernées si nécessaire).

Comme ce document a déjà été signé par vos clients il y a un an, ces lacunes ne sont pas qu'un risque théorique pour l'avenir : elles décrivent potentiellement la relation contractuelle réellement en vigueur depuis un an, y compris pour des données déjà éventuellement confiées à des sous-traitants ultérieurs non identifiés et pour des données de clients dont le contrat a peut-être déjà pris fin sans suppression. Une correction impliquera vraisemblablement un avenant à faire signer par chaque client, pas seulement une mise à jour du modèle pour les signatures futures.

**Autre document potentiellement concerné** : je n'ai pas vu trace ici d'une description des mesures de sécurité en annexe (souvent un document séparé) — si elle existe, elle mériterait le même type de relecture, mais je ne la rédige ni ne l'audite ici sans que vous me la transmettiez.

---

Ce retour est une base d'analyse à partir des exigences de l'article 28 RGPD, pas un avis juridique personnalisé. Une relecture par un avocat ou un DPO est recommandée avant toute correction ou nouvelle signature, en particulier compte tenu de l'ancienneté de la version actuellement en vigueur chez vos clients et du fait qu'elle a déjà produit des effets pendant un an.

## Auto-évaluation

Relecture du document original en tant qu'auditeur externe, faille par faille, en confrontant ma grille aux trois failles réellement présentes.

1. **Recours à des sous-traitants ultérieurs sans autorisation écrite préalable ni droit d'opposition (art. 28.2)** — **repérée**. Marquée 🔴, avec la référence à l'article exact, et reprise dans le paragraphe "deux clauses existantes posent un problème plus grave" pour souligner qu'il ne s'agit pas d'une simple lacune mais d'une clause qui contredit la loi.

2. **Absence de délai de notification en cas de violation de données** — **repérée**. Marquée 🔴 avec la référence à l'art. 28.3.f, et son impact concret sur les propres obligations du Client (notification CNIL/personnes concernées) est explicité.

3. **Conservation illimitée après la fin du contrat pour les "propres archives" du sous-traitant (viole l'art. 28.3.g)** — **repérée**. Marquée 🔴, identifiée explicitement comme contradiction directe avec l'obligation de suppression/restitution, et distinguée d'une simple lacune de rédaction.

Les trois failles attendues sont donc toutes repérées et correctement rattachées à leur base légale. Deux points restent cependant, à mon sens, insuffisamment traités dans la réponse livrée :

- **Le lien entre l'absence d'encadrement des sous-traitants ultérieurs et un risque de transfert hors UE non maîtrisé n'est pas fait.** Ma grille marque "Transferts hors Union européenne" en ⚪ ("non abordé... à vérifier séparément"), traité comme un point isolé et sans information. Or `audit.md` demande explicitement de relier les points entre eux plutôt que de les traiter comme des remarques isolées : puisque DataSync peut choisir librement ses sous-traitants ultérieurs sans en informer le Client, rien ne garantit que ces sous-traitants soient situés dans l'UE — la clause 🔴 sur les sous-traitants ultérieurs devrait logiquement faire passer la case "transferts hors UE" d'un simple "non applicable/à vérifier" à un risque concret et aggravé par l'absence de contrôle, pas à une case neutre. Je ne fais pas ce lien dans la réponse livrée.
- **Le piège propre au DPA signalé dans `references/dpa.md`** — vérifier si ce document doit rester un modèle générique à adapter à chaque client ou s'il est destiné à être personnalisé — **n'est pas posé à l'utilisateur**. C'est pourtant explicitement listé comme un piège fréquent du document de référence, et il est directement pertinent ici puisque l'utilisateur précise que ce même texte "a été fait signer" à plusieurs clients : je recommande un "avenant à faire signer par chaque client" en conclusion, mais je ne demande jamais si ce futur avenant doit être un modèle unique standardisé ou nécessite une adaptation contractuelle propre à chacun des clients déjà engagés. C'est une question de méthode de correction que la réponse laisse de côté alors que le contexte fourni par l'utilisateur (documenr déjà signé par "nos clients", au pluriel) la rendait pertinente.

Bilan : les trois failles substantielles demandées sont correctement repérées, classées 🔴 et reliées à l'article exact du RGPD qu'elles violent — l'essentiel de l'audit est solide. Mais l'exercice de mise en relation des lacunes entre elles (sous-traitants ultérieurs non encadrés → risque de transfert hors UE non maîtrisé) n'est fait qu'à moitié, et une question de méthode propre au DPA (modèle générique vs adapté par client) explicitement signalée dans le fichier de référence n'est pas posée à l'utilisateur alors que le contexte du cas l'appelait directement.
