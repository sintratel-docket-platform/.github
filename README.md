# Organisation defaults

GitHub applies the files in this repository to any repository in the
organisation that does not carry its own.

| File | Applies to |
|---|---|
| [`.github/CONTRIBUTING.md`](.github/CONTRIBUTING.md) | Every repository without its own contribution guide |
| [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) | Every repository without its own pull request template |
| [`profile/README.md`](profile/README.md) | The organisation's public profile page |

## What is deliberately not here

**`AGENTS.md`.** An agent reads the file in the repository it is working in; it
does not read organisation-level files. The constitution therefore has to exist
in each repository, and its canonical copy lives in
[docket-architecture/standards](https://github.com/sintratel-docket-platform/docket-architecture/tree/main/standards).
A drift check in each repository compares its copy against that source.

**`CODEOWNERS`.** The rules that matter are path-specific — the CI identity
module, the bootstrap stack, the production overlay — so they live in the
repositories that have those paths.

**Workflows.** GitHub does not inherit them. Each repository carries its own.

Change the contribution guide or the pull request template
[at the source](https://github.com/sintratel-docket-platform/docket-architecture/tree/main/standards/templates)
first, then copy it here.
