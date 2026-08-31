# French Legal Drafting & Review

A Claude Agent Skill that assists with drafting and reviewing standard legal documents for digital products under French and EU law.

## Overview

This skill helps produce or review the legal documents a website, mobile app, SaaS product, or e-commerce site typically needs to operate under French law and the GDPR: a legal notice (*mentions légales*), a privacy policy, a cookies policy, terms of use / terms of sale (*CGU/CGV*), and a data processing agreement (*DPA*, GDPR Article 28).

It is built as a drafting and review **assistant**, not a document generator that fills in every blank on its own. Two principles drive its behavior, and are documented in `SKILL.md`:

- **Fact-first, no invention** — the skill is instructed never to silently complete a missing fact (a retention period, a hosting provider's legal entity, a consent mechanism) with a plausible-looking value. Missing information is left as an explicit blank in the document, or listed separately as a point to confirm.
- **No legal over-interpretation** — the skill is instructed to qualify a contract, a party, or a data processing activity before applying a rule to it, and to distinguish clearly between a legal obligation, a recommendation, and a platform rule (e.g. an App Store or Google Play requirement).

The skill targets **digital products and services** specifically (websites, mobile apps, SaaS, e-commerce) rather than French/EU legal drafting in general, and it produces documents in French, matching the legal texts it is designed to draft.

## What it can do

Based strictly on what is implemented in `SKILL.md` and `references/`:

- Draft a **legal notice** (*mentions légales*) under LCEN Article 6-III, for companies, sole traders, and associations.
- Draft a **privacy policy** under GDPR Articles 12–14, including a per-processing table of purposes, legal bases, and retention.
- Draft a **cookies / tracker policy**, aligned with CNIL guidance, including the distinction between cookies and non-cookie trackers (mobile SDKs, push tokens, advertising identifiers).
- Draft **terms of use (CGU)** and **terms of sale (CGV)**, including withdrawal rights, statutory guarantees, and consumer-protection clauses under the French Consumer Code.
- Draft a **data processing agreement (DPA)** under GDPR Article 28, for processor/controller relationships.
- **Audit an existing document** clause by clause rather than rewriting it outright, flagging what is present and compliant, present but incomplete, missing or legally risky, or not applicable.
- **Check consistency** across a response or across multiple documents produced together (e.g. the same company details, hosting provider, or retention period should not diverge between documents).
- **Flag missing information explicitly**, rather than filling it in, using inline blanks in the document and a separate list of points to confirm.
- **Distinguish GDPR roles** (controller vs. processor) on a per-processing basis rather than assigning a single role to an entire product or relationship.
- **Distinguish legal obligations from recommendations and from platform rules** — for example, separating what French/EU law requires from what Apple's or Google's store guidelines require.

What it does **not** do: it does not perform legal research or check current case law, it does not verify facts against external sources, it does not itself carry out a GDPR impact assessment (it can flag that one is probably required), and it does not replace review by a qualified professional.

## Core principles

1. **Fact-first / no invention** — never complete a missing legal or technical fact with a plausible value; use an explicit blank instead.
2. **Legal qualification before conclusion** — identify what is actually being sold or processed (a good, a digital service, a subscription, a mix) before applying a rule that depends on that qualification.
3. **Explicit uncertainty** — when the available information is not enough to reach a conclusion, say so, rather than producing a confident but unsupported answer.
4. **Treatment-by-treatment GDPR analysis** — determine the legal basis, retention, and controller/processor role separately for each data processing activity, not once for an entire product.
5. **Legal rules vs. platform rules** — never present an app store or platform requirement as a French or EU legal obligation, or vice versa.
6. **Temporal awareness** — flag that regulatory thresholds, mediation platforms, and store rules can change, instead of presenting them as permanently fixed.
7. **Consistency checking** — before delivering, check that clauses do not contradict each other, a mandatory consumer right, or another document produced in the same response.
8. **Separation between publishable document and internal analysis** — keep the delivered document free of production notes; conditional or unconfirmed points are marked inline in the document text itself, and the reasoning, risks, and open questions are kept in the surrounding response.

## Supported documents

| Document | Legal basis | Reference file |
|---|---|---|
| Legal notice (*mentions légales*) | LCEN art. 6-III, French Commercial Code | `references/mentions-legales.md` |
| Privacy policy (*politique de confidentialité*) | GDPR art. 12–14, CNIL guidance | `references/politique-confidentialite.md` |
| Cookies / trackers policy | French "Informatique et Libertés" law art. 82, CNIL guidance | `references/cookies.md` |
| Terms of use (CGU) / Terms of sale (CGV) | French Consumer Code, French Commercial Code | `references/cgu-cgv.md` |
| Data processing agreement (DPA) | GDPR art. 28 | `references/dpa.md` |
| Review of an existing document | Methodology only (clause-by-clause audit) | `references/audit.md` |

## How it works

The skill follows a fixed sequence, described in `SKILL.md`:

```
Facts extraction
  → Legal qualification (contract type, B2B/B2C, editor's legal status, jurisdiction)
  → Applicable obligations (which document(s) the product actually needs)
  → Information collection (per-document checklist, transversal identity/hosting facts)
  → Drafting or audit (from the matching reference file's template and checklist)
  → Consistency check (internal contradictions, cross-document consistency)
  → Currentness check (flag rules and thresholds that may need re-verification)
  → Delivery (document, points to confirm, and analysis kept separate)
```

For a review of an existing document, the skill follows a different path described in `references/audit.md`: it classifies each clause instead of drafting new text, and does not rewrite the document unless explicitly asked to.

## Output model

When the skill drafts or audits a document, its response is structured in three parts:

1. **Publishable document** — the text intended for the user's actual legal page or file, with explicit blanks (e.g. `[hosting provider address to confirm]`) for missing point-in-time facts, and inline conditional wording (e.g. `[applies only if X — to confirm]`) for clauses that depend on something not yet confirmed.
2. **Points to confirm** — the list of facts, durations, architectures, or qualifications that could not be established from the information given.
3. **Analysis / risks** — the reasoning, identified risks, and alternatives considered.

Internal notes, open questions, and reasoning are not mixed into the publishable document itself — they belong in parts 2 and 3 of the response, not in part 1.

## Examples

The [`examples/`](examples/) folder contains three fictional, synthetic walkthroughs showing the skill's behavior on a representative request. They use invented companies and data throughout, are not full legal templates, and are meant to illustrate the skill's approach rather than to be copied as-is:

- [`examples/01-saas-b2b.md`](examples/01-saas-b2b.md) — drafting a legal notice and privacy policy for a fictional B2B SaaS.
- [`examples/02-mobile-app.md`](examples/02-mobile-app.md) — scoping the legal documents needed for a fictional free mobile app.
- [`examples/03-b2c-cgv-audit.md`](examples/03-b2c-cgv-audit.md) — a clause-by-clause audit of a fictional B2C terms-of-sale document.

## Testing

The skill has been tested through several rounds of self-conducted, AI-assisted evaluation rather than by independent professional legal review:

- A small **regression suite** of three end-to-end scenarios (a SaaS legal notice and privacy policy, a mobile app's document scoping, and a terms-of-sale audit), checked against a fixed criteria list.
- An **adversarial test suite** of 18 scenarios designed to probe specific failure modes: fact invention, legal over-interpretation, confusing a platform rule with a legal obligation, confirming an outdated rule, and resisting pressure to skip verification or fill in unconfirmed information.
- An **independent red-team audit** of 52 new scenarios, deliberately built to avoid reusing the earlier tests, covering contract qualification, GDPR analysis, technical-provider handling, legal-identity edge cases, consumer law, platform-vs-law confusion, manipulative prompts, multi-issue combined cases, false claims from the user, and document audits. This round found a meaningful number of failures — including cases where a provider's address had been invented outright — traced to a small set of recurring root causes and corrected through general rules rather than case-specific patches. A follow-up pass re-tested the affected scenarios and a sample of previously passing ones to check for regressions.

These results are internal test artifacts — scenarios and per-test transcripts in [`adversarial/`](adversarial/) and [`redteam/`](redteam/), written summaries in [`tests/`](tests/) — produced and evaluated by the same AI-assisted process used to build the skill. They indicate that a specific, documented set of failure modes has been tested for and addressed — they are not an independent legal audit, a compliance certification, or a guarantee that the skill will handle every scenario correctly.

## Installation / Usage

This repository follows the Agent Skills format: a `SKILL.md` file (with a YAML description used to decide when the skill should activate) plus a `references/` folder of documents loaded on demand for the specific document being drafted or reviewed.

To use it, make the skill available to an Agent Skills-compatible environment (for example by placing this folder where that environment looks for skills, or by installing the [`redaction-legale-numerique.skill`](redaction-legale-numerique.skill) archive it provides — note that this packaged archive is a work-in-progress build, not yet a finalized published release) — the exact installation step depends on the platform you are using, so refer to that platform's own documentation. Once available, the skill activates when a request matches its description (drafting, generating, checking, or reviewing a legal notice, privacy policy, cookies policy, terms, or DPA for a digital product), and it will ask for the information it needs rather than assume it.

The [`adversarial/`](adversarial/) and [`redteam/`](redteam/) folders (test scenarios and per-test results) and the [`tests/`](tests/) folder (written summary reports) document how the skill has been evaluated so far; none of them are required to use the skill.

## Scope and limitations

- This skill does not replace a lawyer or a data protection officer. It is a drafting and review aid, not a source of legal advice.
- The quality of its output depends entirely on the information it is given — an incomplete or inaccurate description of the product leads to an incomplete or inaccurate document.
- Some legal qualifications (B2B vs. B2C, controller vs. processor, whether an exception to the right of withdrawal applies) require information the skill cannot infer and will ask for; when it cannot be determined, the skill is designed to say so rather than assume.
- French and EU legal and regulatory rules change over time (thresholds, mediation schemes, consumer-protection rules); the skill flags rules that should be re-verified at the time of publication, but cannot verify them itself.
- App Store, Google Play, and similar platform rules also change, and are kept distinct from legal obligations — a platform requirement should not be read as a statement of French or EU law.
- Any technical or factual information supplied by the user (hosting provider, third-party tools, data actually collected) should be verified against the product's real configuration before publication.
- Human review — by a lawyer or DPO — is recommended before publishing any document produced or audited with this skill, particularly for regulated activities, sensitive data, or products aimed at minors.

## Legal disclaimer

This repository and the documents it helps produce are provided for informational and drafting-assistance purposes only. They do not constitute legal advice, and using this skill does not create an attorney-client relationship. Legal documents produced or reviewed with this skill should be checked by a qualified lawyer or data protection officer before publication or use.

## Contributing

Contributions are welcome, in particular:

- **Reporting an error** — open an issue describing the incorrect or missing rule, ideally with the relevant legal source (article, CNIL guidance, etc.).
- **Proposing a test** — new adversarial, regression, or edge-case scenarios are useful, especially ones that reveal a reproducible failure rather than a one-off phrasing issue.
- **Proposing an improvement** — suggestions to a reference file or to `SKILL.md` are welcome; general rules are preferred over patches specific to a single case.

Please do not include real personal data, confidential business information, or real company identifiers in issues, test cases, or examples — use fictional companies and data throughout.

## License

This project is licensed under the [MIT License](LICENSE).

## Version

Current release: **v1.0.0**.
See [`CHANGELOG.md`](CHANGELOG.md) for the project's release history and changes.

