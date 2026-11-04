# Reference verification: Catholic Doctrinal Fidelity Index

This guide runs the public calculator at the audited source revision. The demonstration has four built-in examples and prints their results. It performs no model calls. [Calculator source](../engine/cdfi_calculator.py).

## Environment and exact commands

Use Git, a POSIX shell and Python 3.12. The public calculator uses the standard library; no dependency installation is needed for this command. Python 3.12.16 was used for the local documentation check. The source supplies no broader supported-version declaration. [Imports and demonstration](../engine/cdfi_calculator.py).

```sh
(
  set -eu
  review_dir="$(mktemp -d)"
  git clone https://github.com/node-and-norm/cdfi-framework.git "$review_dir/repository"
  cd "$review_dir/repository"
  git checkout --detach b2d635c803a0ce4ee1be3839a7d7c251adc2d60a
  git rev-parse HEAD
  python3.12 --version
  python3.12 engine/cdfi_calculator.py
  git diff --exit-code
  git status --short
)
```

## Expected demonstration output

The preserved four examples produce these numeric fields. The sequence follows the built-in cases in [the calculator](../engine/cdfi_calculator.py).

| Built-in example | Computed score | Final score | Cap applied |
| :--- | ---: | ---: | :--- |
| Defined dogma, no gate failure | 91.00 | 91.00 | False |
| Relativism gate failure | 71.40 | 40.00 | True |
| Both gate failures | 46.80 | 40.00 | True |
| Legitimate opinion, no gate failure | 69.20 | 69.20 | False |

The command should exit with status 0. Its printed tier names are labels assigned by the code's thresholds. Their display supplies no approval for an institutional use. The demonstration includes no assertion-based validation suite. [Calculator](../engine/cdfi_calculator.py), [current research limits](research-summary.md#limits-and-next-evidence).

## Write effects and interpretation

The command prints to standard output and has no file-write operation. Cloning creates the disposable checkout. Record the source commit, Python version, command, numeric outputs and exit status. [Calculator implementation](../engine/cdfi_calculator.py).

Matching these outputs reproduces the current implementation's arithmetic on its example inputs. The [scoring-contract differences](current-review.md#scoring-contract) remain unresolved. The private production pipeline, reported benchmark results and human theological review require their own evidence. [Publication boundary](../PUBLICATION_SNAPSHOT.md), [AI and verification limits](ai-use-disclosure.md).
