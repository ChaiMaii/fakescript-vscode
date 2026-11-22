# FakeScript for VS Code

Syntax highlighting, language configuration, and code snippets for **FakeScript (`.fks`)** — the strictly zero-symbol Ahead-of-Time compiled programming language.

## Features

- **Full FakeScript v3.0 syntax highlighting**:
  - `note` line comments
  - `say ... end` string literals
  - Types (`num`, `text`, `flag`, `list of`, `empty list of`, `action`)
  - Control flow (`if`, `else if`, `else`, `loop when`, `loop from`, `for each`, `do`, `end`, `give back`, `stop`, `skip`)
  - Plain-English operators (`is`, `is not`, `is under`, `is over`, `is at least`, `is at most`, `plus`, `minus`, `times`, `divided by`, `over`, `mod`, `negative`, `not`, `and`, `or`)
  - Functions (`fn`, `exec`), imports, and standard library module calls (`print`, `math`, `text`, `file`, `time`)
  - **Zero-symbol enforcement**: highlights stray punctuation symbols outside comments and `say ... end` strings as illegal syntax
- **Language configuration**: `Ctrl+/` toggles `note ` comments, automatic indentation after `do` / outdent on `end` & `else`, and `do` / `end` code folding.
- **Snippets**: `main`, `fn`, `fnr`, `pln`, `if`, `ife`, `loopw`, `loopr`, `each`, `ask`.

## Install Locally in VS Code

Copy (or symlink) this folder into your VS Code extensions directory and reload VS Code:

**Windows (PowerShell):**
```powershell
Copy-Item -Recurse -Force . "$env:USERPROFILE\.vscode\extensions\chaimaii.fakescript-vscode-0.1.0"
```

**Linux / macOS:**
```bash
cp -r . ~/.vscode/extensions/chaimaii.fakescript-vscode-0.1.0
```

### Package as `.vsix`

```bash
npx @vscode/vsce package
code --install-extension fakescript-vscode-0.1.0.vsix
```

## Links

- **Compiler**: https://github.com/ChaiMaii/fakescript
- **Website**: https://chaimaii.github.io/fakescript-website/
- **Documentation**: https://chaimaii.github.io/fakescript-docs/

## License

Licensed under the [WTFPL](./LICENSE).
