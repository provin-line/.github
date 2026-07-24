# Contributing (provin-line organization default)

Thanks for your interest in the provin / dPLaaX stack. This is the default
contribution guide for repositories in the `provin-line` organization; a
repository's own `CONTRIBUTING.md`, where present, takes precedence.

## Before you start

- **Bugs / questions**: open an issue on the affected repository. For a
  suspected security flaw, do **not** open a public issue — see
  [SECURITY.md](SECURITY.md).
- **Larger changes**: open an issue first to discuss the design before
  writing code. The specs that bind wire behavior live in
  [dplaax/spec](https://github.com/dplaax/spec) and
  [provin-line/profile.spec](https://github.com/provin-line/profile.spec);
  changes that touch wire semantics start there, not in an implementation.

## Pull requests

- Keep PRs focused; unrelated changes go in separate PRs.
- Each repository's `AGENTS.md` (where present) states its layer rules and
  conventions — they are enforced in review.
- CI must pass. Run the repository's documented build/test targets locally
  (`make test`, `pnpm -r test`, or as the README says) before pushing.
- New behavior comes with tests; wire-visible behavior comes with
  conformance vectors where the spec defines them.

## Licensing

All repositories are licensed under Apache-2.0 unless stated otherwise. By
contributing, you agree that your contributions are licensed under the same
license as the repository you contribute to.

## Code of conduct

All community spaces follow our [Code of Conduct](CODE_OF_CONDUCT.md).
