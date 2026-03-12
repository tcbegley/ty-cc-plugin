# ty-lsp

A [Claude Code](https://claude.com/claude-code) plugin that integrates
[ty](https://docs.astral.sh/ty/) (Astral's Python type checker) as an LSP
server. Based on the official
[pyright-lsp](https://github.com/anthropics/claude-plugins-official/tree/main/plugins/pyright-lsp)
plugin, but using Astral's ty instead of pyright.

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

Install from the [tcbegley-cc-plugins](https://github.com/tcbegley/tcbegley-cc-plugins) marketplace:

```sh
/plugin marketplace add tcbegley/tcbegley-cc-plugins
/plugin install ty-lsp@tcbegley-cc-plugins
```

### Development

```sh
claude --plugin-dir /path/to/ty-cc-plugin
```

## What it provides

- Real-time Python type checking diagnostics as Claude edits code
- Code navigation (go to definition, find references)
- Hover information with type details

## Configuration

ty is configured via `ty.toml` or the `[tool.ty]` section of `pyproject.toml`.
See the [ty configuration docs](https://docs.astral.sh/ty/configuration/) for
details.
