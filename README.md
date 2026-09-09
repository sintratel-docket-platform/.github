# Organisation defaults

GitHub applies the files in this repository to any repository in the
organisation that does not carry its own.

| File | Applies to |
|---|---|
| [`.github/CONTRIBUTING.md`](.github/CONTRIBUTING.md) | Public repositories without their own contribution guide |
| [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) | Public repositories without their own pull request template |
| [`profile/README.md`](profile/README.md) | The organisation's public profile page |

> **This repository is public, so its defaults reach public repositories only.**
> GitHub does not apply a public `.github` repository's community health files
> to private ones. Ten of the twelve project repositories are private and
> therefore keep their own copies of both files.
>
> Making this repository private would invert the problem: private repositories
> would inherit, and the organisation profile would disappear. Both are kept as
> copies at the source in `docket-architecture/standards/templates`, so there is
> one place to change them either way.

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
