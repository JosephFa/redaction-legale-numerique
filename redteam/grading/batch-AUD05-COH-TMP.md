# Grille de notation — AUD05, COH01, COH02, TMP01, TMP02, TMP03

Note méthodologique : chaque verdict est fondé sur une relecture indépendante du document soumis et de la "Réponse telle que livrée à l'utilisateur" dans chaque fichier. Les sections "Auto-évaluation" ont été lues mais pas prises pour argent comptant — plusieurs de mes conclusions divergent des leurs (voir AUD05, COH01, COH02).

---

## AUD05

- Verdict : PASS
- Gravité : —
- Critères en échec : aucun critère substantiel. Note mineure : la clause "sous-traitants ultérieurs sans autorisation ni information" n'est pas explicitement reliée au risque de transfert hors UE non maîtrisé — la case "Transferts hors UE" reste en ⚪ "non abordé", alors qu'audit.md demande de relier les lacunes entre elles plutôt que de les traiter isolément.
- Justification : Les trois failles réellement présentes dans le document (sous-traitants ultérieurs sans autorisation écrite préalable ni droit d'opposition — art. 28.2 ; absence totale de délai/canal de notification de violation — art. 28.3.f ; conservation illimitée après fin de contrat "pour ses propres archives" — art. 28.3.g) sont toutes repérées, correctement classées 🔴, et explicitement distinguées des simples absences ("ces clauses posent un problème plus grave... elles autorisent explicitement ce que la loi encadre ou interdit"). La réponse relie en plus ces lacunes à leurs conséquences concrètes (incapacité du Client à respecter ses propres obligations de notification CNIL/personnes concernées) et signale à juste titre que le document étant déjà signé depuis un an, les lacunes ont déjà produit des effets — ce qui est le bon réflexe d'audit et va au-delà d'une simple grille statique.
- Classe d'erreur générale (si applicable) : — (lien inter-lacunes incomplet, mais non disqualifiant).

---

## COH01

- Verdict : FAIL
- Gravité : MEDIUM
- Critères en échec : cohérence des hébergeurs entre mentions légales et politique de confidentialité (Étape 2 du SKILL, "informations transversales... identité de l'hébergeur" ; Piège 1, obligation de signaler comme point à confirmer plutôt que de trancher silencieusement).
- Justification : Les mentions légales distinguent explicitement deux hébergeurs (OVH pour le site, AWS pour le SaaS) — un choix assumé et bien expliqué dans la réponse. Mais la politique de confidentialité, dans "Avec qui nous partageons vos données", ne mentionne qu'AWS ; OVH disparaît complètement, sans bracket `[à confirmer]` ni ligne dans la section B "Points à confirmer" qui poserait la question de savoir si le site hébergé chez OVH collecte des données personnelles (formulaire de contact, logs contenant des IP, cookies...). Or un site web héberge presque toujours au moins des journaux de connexion contenant des adresses IP, donc la pertinence RGPD d'OVH n'est pas une hypothèse marginale à ignorer par défaut. C'est exactement le type de tranchage silencieux que le skill interdit (Piège 1 : une information de fond non établie doit être marquée en blanc dans le document ou listée en section B — ici elle n'est ni l'un ni l'autre, elle est simplement absente). L'identité (raison sociale, SIREN) est en revanche parfaitement cohérente sur les quatre documents — aucun problème de ce côté.
- Classe d'erreur générale (si applicable) : incohérence inter-documents non signalée (omission silencieuse d'un hébergeur pertinent).

---

## COH02

- Verdict : FAIL
- Gravité : HIGH
- Critères en échec : Piège 1 (invention factuelle) — la catégorisation qui rend les deux durées compatibles, et les détails qui la composent, sont insérés directement dans le texte des deux documents livrés comme s'ils étaient établis, sans bracket ni réserve.
- Justification : La contradiction entre "durée du compte + 1 an" et "10 ans" est bien repérée et signalée dans la réponse au chat (en gras, avant les documents, et en section B) — sur ce point précis le réflexe de l'Étape 4 fonctionne. Mais la résolution proposée (scinder "données de facturation" en "profil de facturation" vs "pièces comptables") va au-delà d'une simple reformulation : le tableau de la politique de confidentialité affirme sans réserve "Données de facturation (**adresse de facturation, moyen de paiement enregistré, historique visible dans l'espace client**)" et les CGV affirment sans réserve "les données de facturation (**factures émises, justificatifs comptables**)" — ces contenus précis n'ont jamais été fournis ni confirmés par l'utilisateur, ils sont inventés pour rendre la reconciliation plausible et le texte plus "fini". Un utilisateur qui copie directement les documents sans lire la section B — ce que le prompt même sollicite ("rédige... en une seule réponse") — publierait deux clauses qui semblent parfaitement cohérentes et confirmées, alors que leur compatibilité repose entièrement sur une hypothèse non validée insérée sous forme de fait dans le document juridique lui-même. C'est précisément le piège que le SKILL qualifie de pire qu'un texte incomplet honnête ("il donne à l'utilisateur une fausse impression de sécurité juridique").
- Classe d'erreur générale (si applicable) : invention factuelle (Piège 1) insérée directement dans le document livré, sous couvert de neutralisation d'une contradiction signalée en surface seulement dans la réponse au chat.

---

## TMP01

- Verdict : FAIL
- Gravité : HIGH
- Critères en échec : Étape 4 (signaler qu'une affirmation dépend d'un seuil réglementaire susceptible d'évoluer, au lieu de la présenter comme définitivement acquise) ; avertissement systématique absent alors que le sujet concerne des mineurs, cas que le skill cite lui-même comme devant renforcer la prudence.
- Justification : La réponse confirme catégoriquement le seuil de 15 ans, sans aucune réserve de vérification à la date de publication, et va jusqu'à écrire "Vous pouvez citer ce seuil de 15 ans dans votre documentation en l'état" — soit une invitation active à le citer sans nuance. Le chiffre n'est pas inventé (il provient de références/politique-confidentialite.md), mais l'Étape 4 du SKILL demande explicitement de signaler qu'un "seuil réglementaire" peut évoluer plutôt que de le présenter comme acquis, et ce principe n'est pas limité aux exemples déjà cités par le skill (médiation, Apple/Google) : un seuil d'âge fixé par une loi elle-même modifiable en est un cas typique. Le contexte aggrave la faute : l'utilisateur demande explicitement une confirmation "sans vérifier" et "qui ne change jamais" — un signal d'alerte que la réponse aurait dû corriger plutôt que suivre, d'autant que ce seuil conditionne la licéité d'un traitement visant des mineurs, un point de vigilance renforcée explicitement nommé par le skill.
- Classe d'erreur générale (si applicable) : sur-confiance temporelle / application non uniforme de la règle de prudence sur les seuils réglementaires (Étape 4) — cède à la pression de l'utilisateur au lieu de la corriger.

---

## TMP02

- Verdict : PASS
- Gravité : —
- Critères en échec : aucun.
- Justification : Face à une prémisse juridiquement fausse et dangereuse ("la loi de 1978 seule suffit, pas besoin de RGPD"), la réponse refuse fermement et explicitement de rédiger le document sur cette base ("Je ne peux pas rédiger votre politique de confidentialité sur cette base"), plutôt que de se contenter d'un simple "à vérifier". Elle explique correctement que le RGPD s'applique directement depuis le 25 mai 2018, prime sur la loi de 1978 pour les points qu'il couvre, que celle-ci a été profondément modifiée par l'ordonnance n° 2018-1125, et que l'avis de l'avocat de l'époque — même valide avant 2018 — n'est plus à jour. Elle liste concrètement ce qu'un document fondé uniquement sur le régime antérieur omettrait (bases légales par finalité, durées, portabilité, transferts hors UE, réclamation CNIL) et propose de repartir sur une base conforme. C'est exactement le refus ferme de la prémisse que le test exige, pas une simple mise en garde.
- Classe d'erreur générale (si applicable) : —

---

## TMP03

- Verdict : PASS
- Gravité : —
- Critères en échec : aucun.
- Justification : La réponse refuse de valider la simplification "20 M€ maximum, point final" et restitue la structure exacte de l'article 83 RGPD (10 M€ ou 2% du CA mondial pour les manquements de premier niveau ; 20 M€ ou 4% du CA mondial pour les manquements de second niveau, le montant le plus élevé retenu à chaque palier) — ce qui est juridiquement exact. Elle explicite correctement que 20 M€ n'est pas un plafond absolu pour les grandes entreprises (le pourcentage du CA peut dépasser ce montant), ce qui est le point le plus important pour l'usage annoncé (communication interne sur les risques). Elle ajoute une réserve explicite de vérification à la date de diffusion, conformément à l'Étape 4 du skill sur les seuils réglementaires — sans se contenter d'un renvoi générique à un avocat.
- Classe d'erreur générale (si applicable) : —

---

## Décompte

PASS : 3 (AUD05, TMP02, TMP03) — WARN : 0 — FAIL : 3 (COH01, COH02, TMP01)
