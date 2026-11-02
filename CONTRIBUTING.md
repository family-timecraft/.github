# Contributing to Family TimeCraft

Thank you for your interest in TimeCraft.

## Code contributions are not currently accepted

**Code contributions are not currently accepted; suggestions, bug reports,
and comments are welcome.**

TimeCraft is maintained by a small maintainer team during active development.
Pull requests carrying unsolicited code will not be merged; maintainers may
convert such a pull request into an issue so the idea behind it is not lost.

In this organization, "contributing" means feedback: bug reports, suggestions,
and comments. How to file feedback that maintainers can act on quickly — what
a good bug report contains and how to write an effective suggestion — is
documented in the [support guide](./SUPPORT.md).

Use the issue tracker of the affected repository; every published repository
accepts bug reports and suggestions through issue forms. Security-sensitive
reports must follow the [security policy](./SECURITY.md) instead of public
issue filing.

## Maintainer working agreements

The following apply to maintainer-initiated changes and describe how the
project is built. They are documented here so feedback can be evaluated
against them.

### Commits

Commit messages follow [Conventional Commits](https://www.conventionalcommits.org/):
`type(scope): summary`, with `type` one of `feat`, `fix`, `docs`, `refactor`,
`test`, `chore`, or `build`. Keep commits small and scoped to one logical
change.

### Review hygiene

- No development-process artifacts in code reviews: planning documents,
  research notes, and agent instructions never enter code or its
  documentation.
- Changes are minimal and incremental — no speculative refactoring or
  unsolicited feature additions rides along with a fix.

### Code comments

- Every exported symbol documents itself in the language's native doc-comment
  dialect (rustdoc for Rust, TSDoc for TypeScript, PEP 257 docstrings for
  Python, JSDoc for JavaScript/GJS).
- Comments explain *why*, not *what*. The code is the source of truth for the
  what.
- Task markers use the fully qualified form
  `TODO(family-timecraft/<repo>#N)` so references resolve across repository
  boundaries. Public code and documentation never point at private issues.

### Documentation and links

- Every repository keeps its own `README.md`, `LICENSE`, `CONTRIBUTING.md`,
  and a `docs/` directory scoped to that component only.
- Within a repository, documentation links are relative. Across repositories,
  links use absolute canonical GitHub URLs
  (`https://github.com/family-timecraft/<repository>`), and only published
  repositories may be linked from published documentation. Documentation
  never replicates content owned by another document; it links to the source.
- Legal texts and standard policy boilerplate are the only sanctioned
  duplicates.

## Review etiquette

Be kind and precise (see the [Code of Conduct](./CODE_OF_CONDUCT.md)).
Disagreement about behavior and design is welcome; personal remarks are not.
When a suggestion cannot be accepted, expect an explanation of why so the
underlying need can be addressed another way.
