# Example — Mobile app: legal document scoping

> This is a fictional example created to demonstrate the skill. It does not describe a real company or client.

### User request

> "J'ai une appli mobile de méditation gratuite (iOS/Android) appelée Respire. Les utilisateurs créent un compte avec leur email, on utilise Firebase (Google) pour l'authentification et les notifications push. Pas de paiement pour l'instant. Qu'est-ce qu'il me faut niveau légal pour être en règle avant de publier sur les stores ?"

### Skill analysis

| Document | Needed here? | Why |
|---|---|---|
| Legal notice | Yes | Required for any public online service, regardless of the app being free. |
| Privacy policy | Yes | Personal data is collected (email, authentication data, push tokens). |
| Terms of use | Recommended, not strictly mandatory | There is a user account and an online service, but no sale. |
| Terms of sale | Not identified at this stage | No payment currently — would become necessary if a subscription or in-app purchase is introduced later. |

Key points the skill does **not** assume:

- **Firebase scope**: only Firebase Authentication and push notifications (Cloud Messaging) are treated as confirmed. Firebase Analytics or Crashlytics are not assumed to be active just because "Firebase" is used — the skill asks explicitly whether those modules are also integrated.
- **Push permission ≠ GDPR consent**: the OS-level push authorization is a technical permission, not consent to a specific data processing; the legal basis for processing push-related data (Firebase token, message content) is assessed separately.
- **Legal obligation vs. platform rule**: Apple's and Google's own data-disclosure requirements (App Store privacy labels, Google Play Data safety) are presented as platform/contractual rules, not as French or EU legal obligations — they apply in addition to, not instead of, the documents above.
- **No assumed health data**: the app being about meditation does not, by itself, make the data processed "health data" under Article 9 GDPR. This is flagged as a point to clarify (e.g., is mood, sleep, or condition tracking involved?) rather than concluded either way.

### Example output

> Sur la base de ce que vous décrivez (appli grand public, comptes email, Firebase Auth + notifications push, pas de paiement), voici ce qui est généralement nécessaire — et quelques points que je ne veux pas trancher à votre place faute d'information. [...] Firebase recouvre aussi Analytics, Crashlytics et d'autres modules qui ont des rôles et des données différents — je ne vais pas supposer qu'ils sont activés simplement parce que vous utilisez Firebase pour l'auth et le push.

### Points to confirm

- Whether Firebase Analytics or Crashlytics are also integrated.
- The exact Google/Firebase contracting entity and the applicable cross-border transfer safeguard.
- Whether the app targets or knowingly accepts minors as users.
- The publisher's legal status and identity details (legal form, SIREN/SIRET, address) needed to draft the legal notice.

The skill does not conclude on a DPO obligation either way at this stage, and closes with the standard reminder that a lawyer/DPO review is recommended, especially if a minors' audience is confirmed.
