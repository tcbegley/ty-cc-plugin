# ty-lsp

A [Claude Code](https://claude.com/claude-code) plugin that integrates
[ty](https://docs.astral.sh/ty/) (Astral's Python type checker) as an LSP
server.

## Prerequisites

Install ty globally so that `ty` is available on your `PATH`. The recommended
approach is with [uv](https://docs.astral.sh/uv/):

```sh
uv tool install ty
```

Any other method of globally installing ty should also work, such as
[pipx](https://pipx.pypa.io/), the
[Astral install script](https://docs.astral.sh/ty/getting-started/installation/),
or even a global `pip install ty` (though that's not a great idea).

## Installation

### From local directory (development)

```sh
claude --plugin-dir /path/to/ty-cc-plugin
```

### From a marketplace (once published)

```sh
claude plugin install ty-lsp
```

## What it provides

- Real-time Python type checking diagnostics as Claude edits code
- Code navigation (go to definition, find references)
- Hover information with type details

## Configuration

ty is configured via `ty.toml` or the `[tool.ty]` section of `pyproject.toml`.
See the [ty configuration docs](https://docs.astral.sh/ty/configuration/) for
details.
