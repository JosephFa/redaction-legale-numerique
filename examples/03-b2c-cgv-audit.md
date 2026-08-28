# Example — B2C terms-of-sale audit

> This is a fictional example created to demonstrate the skill. It does not describe a real company or client.

### User request

> "Peux-tu relire mes CGV et me dire ce qui manque ? Voici le texte : 'CGV de LumiApp. En utilisant LumiApp vous acceptez ces conditions. Le prix est de 9,99 €/mois. Aucun remboursement possible. Nous pouvons modifier ces conditions à tout moment sans préavis. Pour tout litige, tribunaux de Paris exclusivement compétents.' C'est un service B2C pour des particuliers en France."

### Skill approach

Following `references/audit.md`, the skill first qualifies the contract (B2C, French consumers, monthly subscription, most likely subscribed online) before judging any clause, then classifies each existing clause instead of only listing what's missing, and actively looks for contradictions between clauses and mandatory consumer rights.

Status legend: 🟢 present/consistent · 🟠 present but incomplete / to verify · 🔴 legally risky or potentially contrary to a mandatory rule · ⚪ not applicable

### Example output

| Clause / topic | Status | Why |
|---|---|---|
| Seller identity | 🔴 | Absent — without it, the whole document is hard to enforce. |
| Price | 🟠 | Present (9.99 €/month) but doesn't state whether it's VAT-inclusive, nor billing terms. |
| Withdrawal right | 🔴 | Absent — a mandatory 14-day withdrawal right applies by default in B2C; no confirmed exception is documented here. |
| "No refund" clause | 🔴 | Directly contradicts the withdrawal right and the statutory conformity guarantee, neither of which can be excluded by contract in B2C. A digital-content exception exists only with an explicit, distinct consumer waiver — nothing here shows that condition is met. |
| Online cancellation | 🔴 | Absent. For an online-subscribed service, French law (Art. L.215-1-1 Consumer Code) requires an easily accessible online cancellation feature — to confirm the subscription is indeed concluded online. |
| Change of terms "at any time without notice" | 🔴 | High risk of being deemed an unfair term in B2C — a substantial change without notice or a resulting right to cancel is generally sanctioned. |
| Exclusive jurisdiction (Paris courts) | 🔴 | Not enforceable against a consumer, who retains the right to sue in their place of residence. |
| Consumer mediation | 🔴 | Absent — mandatory in B2C; if added later, the mediator/platform reference should be checked against its current version. |

**Contradictions flagged**: "no refund" + absent withdrawal right + absent conformity guarantee are treated as one connected risk (the same mandatory consumer rights bypassed in three places), not three isolated remarks. The unrestricted change clause and the exclusive jurisdiction clause add to the same unfair-terms risk profile.

The skill does not rewrite the document unless asked, and closes with its standard reminder: this audit is a drafted basis, not personalized legal advice, and review by a lawyer is recommended before any publication — particularly given the number of risk items identified here.
