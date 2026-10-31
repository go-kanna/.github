<img src="https://go-kanna.github.io/assets/logo/mark-kon-rounded.svg" width="96" height="96" alt="The kanna mark: a wood shaving, flat and then curled">

# Generated Go, not magic Go

kanna is a family of seven code generators for what every Go service repeats. Each one reads what you have already written, from struct tags to your schema, and writes the plain Go you would otherwise write by hand: no reflection, nothing hidden from review. Each is a module of its own, so use one, or all seven together.

**[Site](https://go-kanna.github.io/)** · **[日本語](https://go-kanna.github.io/ja/)** · **[See them work together](https://github.com/go-kanna/showcase)**

| Tool | What it writes |
|---|---|
| [kanna-validate](https://go-kanna.github.io/validate/) | `Validate` methods from struct tags, with Rails' error codes |
| [kanna-value](https://go-kanna.github.io/value/) | Value types held to their rule, and enums to their constants |
| [kanna-orm](https://go-kanna.github.io/orm/) | The implementation of your repository interfaces, and a chainable scope per table |
| [kanna-mapper](https://go-kanna.github.io/mapper/) | The functions you declare between domain and wire types |
| [kanna-i18n](https://go-kanna.github.io/i18n/) | Typed message constructors, the translations compiled in |
| [kanna-di](https://go-kanna.github.io/di/) | The constructor of a container struct, from the functions next to your types |
| [kanna-fixture](https://go-kanna.github.io/fixture/) | A constructor for every struct, every field filled |

## Sponsor

kanna is free and MIT licensed. If it saves you time, you can support its development on [GitHub Sponsors](https://github.com/sponsors/mickamy).

[![Sponsor](https://img.shields.io/badge/Sponsor-mickamy-ea4aaa?logo=githubsponsors&logoColor=white)](https://github.com/sponsors/mickamy)
