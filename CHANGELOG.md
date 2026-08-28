# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

This project has no official release or version tag yet. The items below describe the current state of the repository as an ongoing development version, not a versioned release.

### Added

- Initial version of the `redaction-legale-numerique` Agent Skill for drafting and reviewing French/EU legal documents for digital products, described in `SKILL.md`.
- Support for drafting and auditing the following document types, each with its own reference file in `references/`: legal notice (*mentions légales*), privacy policy, cookies/trackers policy, terms of use / terms of sale (CGU/CGV), and a data processing agreement (DPA).
- Core behavioral principles built into the skill: fact-first drafting with no invention of missing facts, and legal qualification before applying a rule (avoiding legal over-interpretation).
- A fixed workflow covering facts extraction, legal qualification, identification of applicable obligations, information collection, drafting or audit, consistency checking, and a currentness check for rules that may need re-verification.
- A dedicated clause-by-clause audit path (`references/audit.md`) for reviewing an existing document instead of rewriting it.
- Test suites documenting the skill's evaluation so far:
  - An adversarial test suite, with prompts and expected behavior recorded in `adversarial/manifest.json` and per-test results in `adversarial/results/`.
  - A red-team test suite, with scenarios recorded in `redteam/manifest.json`, results in `redteam/results/`, and grading notes in `redteam/grading/`.
  - Regression scenario results in `redteam/results/regression-after/`.
  - Written summaries of the testing process in `tests/PHASE1-AUDIT.md`, `tests/TEST-REPORT.md`, and `tests/FINAL-RED-TEAM-REPORT.md`.
- `README.md` documenting the skill's scope, supported documents, workflow, output model, testing approach, and limitations.
- `LICENSE` file (MIT License).

### Notes

- These test suites are internal, AI-assisted evaluation artifacts produced during development of this skill. They are not an independent legal audit, a compliance certification, or a guarantee of correctness in every scenario.
