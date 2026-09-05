# Contributing to Statistical Replication Gym

Start with the [accepted v0.1 scope](docs/decisions/0001-v0.1-poc-scope.md)
and the relevant GitHub issue. Propose scope changes before implementing them.

## Contributions and review

1. Create a branch from current `main` for the issue being addressed.
2. Keep changes focused and use Conventional Commits, for example
   `docs(rights): record dataset redistribution conditions`.
3. Open a pull request linking the issue. Explain the resulting behavior,
   evidence or checks performed, and remaining limitations. Do not claim a
   check passed if it was not run.
4. Obtain maintainer review before merge. Scientific task packages and
   adjudicated references also need an independent second reviewer who reruns
   the reference and records their evidence. Detailed review, dispute, and
   correction procedures are tracked in
   [issue #4](https://github.com/gle-mini/statistical-replication-gym/issues/4).

Use checks appropriate to the change. Documentation changes need review of
links, consistency, and `git diff --check`. Code changes need relevant execution
checks once the development skeleton exists; there is currently no established
project test command. Statistical reference changes need independently justified
expected results, not snapshots of the implementation under test.

Findings must cite source locations and execution artifacts, distinguish
observations from assumptions, and record unresolved ambiguities. Numerical
agreement is not proof of scientific validity. Describe discrepancies without
unsupported allegations. Corrections must preserve the versions and evidence
underlying earlier published results.

## Contribution rights

Submit only material you created or are authorized to contribute. Identify
third-party content, preserve its notices, and provide evidence of the terms
that permit the intended use. Do not present third-party work as an original
project contribution or remove its license notices.

The project's code and documentation license selection is being completed in
[issue #2](https://github.com/gle-mini/statistical-replication-gym/issues/2).
Until that decision is recorded, this guide does not grant a project license.

## Papers, datasets, author code, and derived assets

Consult the [asset-rights register](docs/asset-rights/README.md) before adding
external material. Papers, datasets, author code, copied figures or tables,
and derived artifacts retain their applicable terms; the project's license
does not automatically cover them.

Public accessibility is not evidence of redistribution permission. Record
access and redistribution separately, including obligations and unresolved
questions. Do not commit assets whose redistribution rights are unresolved
or prohibited, even temporarily: Git history and PR attachments distribute
copies too. Do not upload credentials, personal data, restricted assets, or
hidden evaluator material in commits, issues, logs, or review attachments.

Where access is permitted but redistribution is not, record the source,
version/checksum, and lawful acquisition instructions instead of bundling the
asset. Acquisition must respect authentication, consent, and source terms;
an acquisition script does not confer redistribution rights. Derived outputs
need their own review and are not automatically unrestricted.
