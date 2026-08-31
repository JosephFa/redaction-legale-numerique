# Contributing

Thank you for your interest in contributing to **French Legal Drafting & Review**.

This project is an open-source Agent Skill designed to assist with the drafting and review of legal documents for digital products under French and EU law.

Contributions are welcome, especially when they improve factual discipline, legal qualification, clarity, testing, and the overall reliability of the skill.

## Before contributing

Please keep the core principles of the project in mind:

- Do not invent missing facts.
- Do not silently replace uncertainty with plausible assumptions.
- Qualify the legal situation before applying a rule.
- Do not present a platform requirement as a legal obligation.
- Distinguish legal obligations, recommendations, and platform rules.
- Analyse GDPR roles and obligations according to the specific processing activity.
- Prefer explicit uncertainty over unsupported conclusions.
- Prefer general improvements over patches designed for a single test case.

This project is a drafting and review aid. Contributions should not present the skill as providing legal advice or guaranteeing legal compliance.

## Ways to contribute

### Report an issue

If you identify an incorrect, incomplete, misleading, or outdated rule or behaviour, please open an issue.

When possible, include:

- a clear description of the problem;
- the expected behaviour;
- the relevant document or part of the skill;
- a reproducible example;
- the relevant legal or regulatory source, where applicable.

Please distinguish clearly between:

- a factual error;
- a legal interpretation that should be reconsidered;
- an outdated reference;
- a missing scenario;
- a behaviour or reasoning issue.

## Propose a test case

New test cases are particularly valuable.

Useful scenarios include cases designed to test whether the skill:

- invents missing facts;
- over-interprets legal information;
- confuses legal obligations with platform rules;
- assigns GDPR roles too broadly;
- fails to identify missing information;
- produces contradictory conclusions;
- treats outdated information as current;
- follows misleading or manipulative user instructions.

Prefer reproducible scenarios that reveal a general failure mode rather than a one-off wording problem.

## Propose an improvement

Improvements to `SKILL.md` or files in `references/` are welcome.

When proposing a change:

1. Explain the problem the change addresses.
2. Identify the relevant legal, factual, or methodological basis.
3. Explain why the change should apply generally.
4. Avoid introducing unsupported facts or assumptions.
5. Update or propose relevant test cases when appropriate.

General rules are preferred over patches designed to fix a single example.

## Legal sources and currentness

French and EU legal and regulatory rules can change over time.

If your contribution relies on a legal or regulatory source, please provide enough information to identify and verify it.

Do not assume that a rule, threshold, authority guidance, platform policy, or mediation mechanism remains current simply because it appears in an older document.

## Privacy and confidential information

Please do not include:

- real personal data;
- confidential business information;
- API keys, credentials, or secrets;
- private contracts or documents;
- real company identifiers unless they are necessary and publicly available.

Use fictional companies, names, addresses, and data in examples and test cases whenever possible.

## Pull requests

Before submitting a pull request:

- ensure the proposed change is consistent with the project's core principles;
- check that references and paths remain valid;
- avoid unrelated formatting or structural changes;
- include or update tests when the change affects behaviour;
- make sure no confidential information or secrets are included.

Keep pull requests focused. Smaller and clearly scoped contributions are easier to review.

## Questions and discussion

If you are unsure whether an idea fits the project, open an issue first and describe the proposed change.

Constructive discussion, criticism, edge cases, and alternative approaches are welcome.

## Disclaimer

Contributing to this project does not create a lawyer-client relationship.

This project is provided as an open-source drafting and review tool and does not constitute legal advice. Legal content and documents should be reviewed by an appropriately qualified professional before publication or use.
