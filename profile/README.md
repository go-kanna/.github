<img src="https://go-kanna.github.io/assets/logo/mark-kon-rounded.svg" width="96" height="96" alt="The kanna mark: a wood shaving, flat and then curled">

# You write the declaration. kanna writes the Go you would have.

kanna is a family of seven code generators for what every Go service repeats. You declare what you need under the names the conventions expect, and each writes the plain Go you would otherwise write by hand: no reflection, nothing hidden from review. Where the conventions do not fit, you write that part in Go or SQL. Each is a module of its own, so use one, or all seven together.

**[Site](https://go-kanna.github.io/)** · **[日本語](https://go-kanna.github.io/ja/)** · **[See them work together](https://github.com/go-kanna/showcase)**

| Tool | What it writes |
|---|---|
| [kanna-validate](https://go-kanna.github.io/validate/) | `Validate` methods from struct tags, with error codes keyed by JSON names |
| [kanna-value](https://go-kanna.github.io/value/) | Value types held to their rule, and enums to their constants |
| [kanna-orm](https://go-kanna.github.io/orm/) | The implementation of your repository interfaces, and a chainable scope per table |
| [kanna-mapper](https://go-kanna.github.io/mapper/) | The functions you declare between domain and wire types |
| [kanna-i18n](https://go-kanna.github.io/i18n/) | Typed message constructors, the translations compiled in |
| [kanna-di](https://go-kanna.github.io/di/) | The constructor of a container struct, from the functions next to your types |
| [kanna-fixture](https://go-kanna.github.io/fixture/) | A constructor for every struct, every field filled |

## Run them together

The [kanna CLI](https://github.com/go-kanna/kanna) runs the generators registered as tools in your module, using your existing `//go:generate go tool kanna-*` lines. It works out the order from what each generator reads and writes, so there is no package list to maintain.

```sh
go get -tool github.com/go-kanna/kanna@latest
go tool kanna gen -plan  # see what will run and why
go tool kanna gen        # generate in dependency order
go tool kanna gen -check # check the output without writing it
```

Each generator still works on its own. The CLI coordinates the kanna generators; tools such as buf and sqlc remain separate steps.

## Check the code that calls them

kanna-value, kanna-orm, and kanna-i18n each come with a vet, which finds what the compiler lets through in the code calling what they write: a string constant none of an enum's constants holds, a scope a repository fails on every time, and an error code that renders as its key or with a placeholder unfilled. The kanna CLI runs the vet of each generator your module runs that has one:

```sh
go tool kanna vet
```

Each vet still runs on its own, as `go tool kanna-orm vet ./...`. The vets read the generated code as it is on disk, so run `go tool kanna gen -check` beside them in CI.

## Sponsor

kanna is free and MIT licensed. If it saves you time, you can support its development on [GitHub Sponsors](https://github.com/sponsors/mickamy).

[![Sponsor](https://img.shields.io/badge/Sponsor-mickamy-ea4aaa?logo=githubsponsors&logoColor=white)](https://github.com/sponsors/mickamy)
