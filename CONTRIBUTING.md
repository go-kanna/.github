# Contributing to kanna

Thank you for helping. Each generator, the kanna CLI, and go-kanna/internal live in a repository of their own; open an issue or a pull request on the one a change belongs to.

## Before you start

- For a bug, open an issue with the generator, its version, the declaration, and what it wrote or said. The bug report form asks for each.
- For a feature or a change in behavior, open an issue first. kanna decides each one against its [principles](https://github.com/go-kanna/go-kanna.github.io#principles): a convention follows from a name in one way, what the conventions do not cover is written by hand in Go or SQL rather than set by an option, and one thing has one way to write it. A proposal that says what it saves and what rule it adds is the easiest to weigh.
- A change across repositories, such as one to go-kanna/internal and the generators using it, follows [DEVELOPING.md](https://github.com/go-kanna/kanna/blob/main/DEVELOPING.md) of the kanna CLI: checking out the family, its Go workspace, and the order of releases.

## Pull requests

- Run `make test` and `make lint` in the repository, as its CI does.
- If the change alters what a generator writes, regenerate its examples with `make example` in the same pull request.
- Each `README.md` has a `README.ja.md` beside it. Change both in the same pull request; if you cannot write one of them, say so, and it will be translated before the merge.
- Write commit messages as [Conventional Commits](https://www.conventionalcommits.org/), in English, one line (`fix: …`, `feat: …`, `docs: …`). Mark a change that stops a declaration that used to pass with `!` (`fix!: …`), even before v1.
