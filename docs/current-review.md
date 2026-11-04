# Review guide: Catholic Doctrinal Fidelity Index

The [current research account](research-summary.md) identifies CDFI as evolving. Review the [translation method](../TRANSLATION-METHOD.md) and [source map](../TRACEABILITY.md) as a proposal with recorded design judgments. Scoring-contract reconciliation and human theological validation remain open.

## Versions and publication

| Artifact | Recorded identity | Review boundary |
| :--- | :--- | :--- |
| Archived publication | v1.5, May 31, 2026. DOI 10.5281/zenodo.20475185. [Snapshot record](../PUBLICATION_SNAPSHOT.md) | The fixed source commit is `5e81799c6bc030b2ce5736cc8f9af2aaec0dbdb6`. |
| Active development | Later changes on the current branch. [Provenance](../PUBLICATION_SNAPSHOT.md) | Cite an exact commit when discussing those changes. |
| Earlier claim packs | Some retain v1.4 metadata. [Example pack](../claims/pub3-statistical-rigor.json) | Preserve the older identity when tracing a historical claim. |
| Calculator package | Package version 1.0.0. [Package entry](../engine/__init__.py) | This component label has a separate scope from the archive version. |

The citation file and historical records remain unchanged. The [preserved license](../LICENSE) declares Apache-2.0; this documentation work makes no finding about its conformity to the standard license text.

## Known limits

### Scoring contract

The formula describes metric inputs on a 0 to 10 scale. The calculator documents 0 to 5 inputs and multiplies the weighted sum by 20. Their weighting tables also differ. These artifacts require a governing contract before their outputs can be treated as equivalent. [Formula](specifications/CDFI-formula.md), [configuration](../configs/authority_matrix.json), [calculator](../engine/cdfi_calculator.py).

The configuration includes `relativism_resistance` in two authority-level columns. The calculator excludes that gate metric from the weighted sum. It consequently leaves different effective weight totals across columns. A corrected contract needs its own reviewed implementation change. [Configuration](../configs/authority_matrix.json), [weighted-sum code](../engine/cdfi_calculator.py).

Missing gate values produce warnings and leave the gate unfired. Missing numeric values are treated as zero with a warning. The calculator also falls back to a default authority level for an unknown value. These behaviors are implementation choices requiring review. [Calculator](../engine/cdfi_calculator.py).

### Reported results and human review

The public results summaries report work performed in a separate production pipeline. The public repository lacks the underlying production dataset and judge-reliability test implementation needed to reproduce those reports. [Project record](../README-2026-11-03.md#the-saicred-project), [validation status](governance/cdcf-compliance/c4-validation-status.md).

Reported cap totals and statistical summaries differ across retained files. A reviewer should retain their source versions and request reconciliation against the underlying records. The entry page therefore gives no consolidated ranking or certification claim. [Results summary](../examples/saicred-v2/results-summary.md), [traceability table](../TRACEABILITY.md), [statistical translation](translations/04-statistical-rigor.md), [change history](../CHANGELOG.md).

The limitation register records default authority classification, pending human theological review and a fixed stability score in the reported run. These conditions limit interpretation even if a calculation reproduces. [Limitations](../LIMITATIONS.md), [current research account](research-summary.md).

### Source interpretation and institutional use

A source-linked design choice still requires a reasoned account of its transfer to a new domain. Review source findings, domain interpretation, measurement rules and evidence of effectiveness separately. [Translation method](../TRANSLATION-METHOD.md), [current limits](research-summary.md#limits-and-next-evidence).

The governance files contain proposed controls and institutional mappings. They should be read alongside the current provisional research status. A mapped provision or completed document leaves actual applicability and effective implementation for separate assessment. [Research account](research-summary.md), [responsibility boundary](governance/cdcf-compliance/c3-c7-responsibility-boundary.md).

## People and AI roles

Filip Ponulak leads SAICRED. Naveen Kumar Puppala built the production pipeline. Mark Julius Banasihan developed CDFI's scoring architecture and evaluation governance methodology. William J. Benjamin joined for future work. [Preserved contribution record](../README-2026-11-03.md#the-saicred-project).

The AI disclosure distinguishes Claude-assisted development, Gemini automated judging, reported technical checks and qualified human theological review. A complete retrospective task/model log and uniform human-verification record remain unavailable. [Disclosure](ai-use-disclosure.md).

## Public reproduction boundary

The [verification guide](reference-verification.md) runs the four built-in calculator demonstrations. It checks the behavior of the preserved code. Reproducing model rankings or judge certification requires the separate production artifacts, a reconciled scoring contract and appropriate human review. [Calculator](../engine/cdfi_calculator.py), [current research account](research-summary.md).
