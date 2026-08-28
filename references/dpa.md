# DPA / Accord de sous-traitance (article 28 RGPD)

Ce document s'applique dans une situation précise : l'utilisateur (ou son entreprise) traite des données personnelles **pour le compte d'un tiers** — typiquement un SaaS B2B qui héberge, dans son produit, des données personnelles appartenant aux clients de ses clients (ex: un CRM qui stocke les contacts des clients de l'entreprise abonnée). Dans ce schéma, le client de l'utilisateur est "responsable de traitement", et l'utilisateur est "sous-traitant" au sens RGPD — l'article 28 RGPD impose alors un contrat spécifique entre eux, distinct des CGU/CGV.

Vérifie d'abord si ce cas s'applique réellement : si l'utilisateur traite des données uniquement pour ses propres finalités (ex: gérer ses propres clients, sa propre newsletter), il est responsable de traitement et n'a pas besoin d'un DPA pour cette relation — le DPA concerne la relation où il agit lui-même *pour le compte* d'un tiers, ou (à l'inverse) où il fait appel à ses propres sous-traitants (hébergeur, emailing...) et doit alors s'assurer qu'*eux* lui offrent les garanties de l'article 28.

Fais cette analyse **traitement par traitement**, pas globalement au niveau du produit. Un SaaS B2B est souvent responsable de traitement pour certains traitements (comptes, facturation, sécurité, statistiques qu'il détermine lui-même) et sous-traitant pour d'autres (le contenu que ses clients professionnels y stockent sur leurs propres équipes/contacts) — ne conclus jamais "toutes les données de nos clients relèvent de la sous-traitance" en bloc.

## Informations à collecter

- Qui est responsable de traitement et qui est sous-traitant dans la relation concernée
- Quelles catégories de données personnelles sont traitées dans ce cadre
- Quelles catégories de personnes concernées (clients du client, employés du client, utilisateurs finaux...)
- Quelle est la finalité et la durée du traitement réalisé par le sous-traitant pour le compte du responsable
- Le sous-traitant fait-il lui-même appel à des sous-traitants ultérieurs ("sous-traitants ultérieurs") ? Lesquels ? (hébergeur cloud, service d'email transactionnel, etc.)
- Y a-t-il des transferts hors UE dans la chaîne de sous-traitance ?
- Quelles mesures de sécurité techniques et organisationnelles sont mises en œuvre ?
- Comment le responsable de traitement est-il informé en cas de violation de données (délai, canal) ?
- Comment se déroule la restitution/suppression des données à la fin du contrat ?

## Clauses obligatoires selon l'article 28 RGPD

Le contrat doit prévoir que le sous-traitant :
1. Ne traite les données que sur instruction documentée du responsable de traitement (y compris pour les transferts hors UE, sauf obligation légale contraire — à signaler alors)
2. Garantit que les personnes autorisées à traiter les données sont engagées à la confidentialité
3. Met en œuvre des mesures de sécurité appropriées (article 32 RGPD)
4. Respecte les conditions pour recourir à un autre sous-traitant (autorisation écrite préalable, spécifique ou générale avec droit d'opposition)
5. Aide le responsable de traitement à répondre aux demandes d'exercice des droits des personnes concernées
6. Aide le responsable à respecter ses obligations en matière de sécurité, notification de violations, analyses d'impact
7. Supprime ou restitue toutes les données à la fin de la prestation, selon le choix du responsable
8. Met à disposition du responsable les informations nécessaires pour démontrer le respect de ces obligations, et permet/contribue aux audits

## Gabarit

```markdown
# Accord de traitement des données (DPA)

Entre [Responsable de traitement] et [Sous-traitant], annexé au contrat principal du [date].

## 1. Objet et durée
Le présent accord encadre le traitement de données personnelles réalisé par le Sous-traitant pour le compte du Responsable de traitement, dans le cadre de [description du service], pour la durée du contrat principal.

## 2. Nature et finalité du traitement
[Description précise.]

## 3. Catégories de données et de personnes concernées
Données : [liste]
Personnes concernées : [liste]

## 4. Obligations du Sous-traitant
Le Sous-traitant s'engage à :
- traiter les données uniquement sur instruction documentée du Responsable ;
- garantir la confidentialité des personnes autorisées à traiter les données ;
- mettre en œuvre les mesures de sécurité décrites en Annexe [X] ;
- ne recourir à un sous-traitant ultérieur qu'avec autorisation [écrite préalable / générale avec droit d'opposition] du Responsable, et lui imposer des obligations équivalentes ;
- assister le Responsable pour répondre aux demandes d'exercice des droits des personnes concernées ;
- notifier le Responsable de toute violation de données dans un délai de [délai, ex: 48h] après en avoir eu connaissance ;
- supprimer ou restituer, au choix du Responsable, l'ensemble des données à l'issue de la prestation ;
- mettre à disposition du Responsable les informations nécessaires pour démontrer le respect du présent accord.

## 5. Sous-traitants ultérieurs
Liste des sous-traitants ultérieurs autorisés à la date de signature : [liste, ex: hébergeur cloud, service d'emailing].

## 6. Transferts hors Union européenne
[Description des transferts identifiés et du mécanisme juridique applicable, ou absence de transfert.]

## 7. Sécurité
Voir Annexe [X] — Mesures techniques et organisationnelles.
```

## Pièges fréquents
- Confondre le DPA avec les CGU/CGV — c'est un document technique entre professionnels, pas destiné à l'utilisateur final grand public.
- Inventer la liste des sous-traitants ultérieurs ou les mesures de sécurité en Annexe faute d'information — laisse ces sections comme gabarits explicitement à compléter par l'utilisateur plutôt que de les remplir avec des exemples plausibles présentés comme réels.
- Oublier de lister les sous-traitants ultérieurs réels (souvent l'infrastructure cloud et les outils tiers utilisés en interne) — leur absence de mention n'exonère pas de l'obligation de les gérer conformément à l'article 28.
- Rédiger un DPA générique sans vérifier s'il doit s'insérer dans un contrat-cadre déjà existant avec le client — demander si un DPA-type standard doit être adapté à un client précis ou rédigé comme modèle générique à faire signer par tous les clients.
