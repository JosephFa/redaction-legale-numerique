# Example — SaaS B2B: legal notice + privacy policy

> This is a fictional example created to demonstrate the skill. It does not describe a real company or client.

### User request

> "Je lance mon SaaS Nimbus (outil de gestion de projet pour PME), édité par ma société Nimbus SAS, SIREN 912 345 678, siège au 8 rue des Lilas 69001 Lyon, capital 5 000 €, hébergé sur Vercel + Supabase (UE). On facture un abonnement mensuel via Stripe, on utilise Google Analytics 4 et Intercom pour le support client. Je suis directeur de la publication. Peux-tu me rédiger les mentions légales et la politique de confidentialité ?"

### Skill approach

- **Facts extracted**: legal form (SAS), SIREN, registered address, share capital, hosting providers, payment processor, analytics tool, support tool.
- **Missing information**: the RCS registration city (never inferred from the registered address), the publication director's name, a contact email, and the exact contracting legal entity behind Vercel, Supabase, Stripe, Google, and Intercom.
- **GDPR qualification**: each processing activity is assessed separately — subscription billing (Stripe), audience measurement (GA4), customer support (Intercom) — rather than assigning one legal basis to the whole product.
- **Controller vs. processor**: Nimbus SAS is the controller. Vercel, Supabase, Stripe, Intercom, and Google are potential processors or independent data recipients depending on the exact service used — this is not assumed automatically from the vendor's name.
- **Confirmed vs. to-be-verified**: the SIREN can be reused as-is inside the RCS mention; the registration city cannot. Retention periods, the DPO question, and the cross-border transfer mechanism for non-EU vendors are all flagged as open points rather than filled in.

### Example output

**A. Legal notice (excerpt)**

```markdown
## Éditeur du site
Nimbus SAS, société par actions simplifiée au capital de 5 000 €
Siège social : 8 rue des Lilas, 69001 Lyon
RCS [ville du greffe à vérifier — non déductible de l'adresse du siège] 912 345 678
Directeur de la publication : [nom à compléter]
Contact : [email à compléter]

## Hébergement
[Raison sociale et adresse de l'entité Vercel contractante à compléter]
[Raison sociale et adresse de l'entité Supabase contractante à compléter]
```

**A. Privacy policy (excerpt — processing table)**

| Purpose | Data | Legal basis | Retention |
|---|---|---|---|
| Account management | Identity, email, password | Contract performance | [duration to determine] |
| Subscription billing (Stripe) | Billing data | Contract performance / legal obligation | [statutory accounting retention — to confirm] |
| Audience measurement (GA4) | Browsing data, technical identifiers | [to confirm — depends on consent configuration] | [not GA4's default retention setting] |
| Customer support (Intercom) | Support conversation content | Contract performance / legitimate interest | [duration to determine] |

**B. Points to confirm (summary)**
- RCS registration city.
- Publication director's name and contact email.
- Exact contracting entity for Vercel and Supabase.
- GA4 consent configuration (standard mode vs. exempted audience measurement).
- Non-EU transfer safeguard for Stripe, Google, and Intercom.

The skill closes with its standard reminder: this is a drafted basis, not personalized legal advice, and review by a lawyer or DPO is recommended before publication.
