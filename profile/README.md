<p align="center">
  <a href="https://docattest.github.io/docattest/">
    <img src="https://docattest.github.io/docattest/img/social-card.png" alt="docattest: your docs are lying to you" width="720">
  </a>
</p>

<h3 align="center">Documentation that CI can fail.</h3>

<p align="center">
  Markdown pages carry their own proof: examples that run, values in the prose that are
  compared with your code, tables whose rows are tests. When the code changes and a sentence
  stops being true, the build fails at that page and line.
</p>

<p align="center">
  <a href="https://docattest.github.io/docattest/playground.html"><b>Try it in the playground</b></a>
  ·
  <a href="https://docattest.github.io/docattest/">Website</a>
  ·
  <a href="https://github.com/docattest/docattest">Repository</a>
  ·
  <a href="https://github.com/marketplace/actions/docattest">GitHub Action</a>
</p>

<p align="center">
  <a href="https://www.npmjs.com/package/docattest"><img src="https://img.shields.io/npm/v/docattest?label=npm&color=cb3837" alt="npm"></a>
  <a href="https://pypi.org/project/docattest/"><img src="https://img.shields.io/pypi/v/docattest?label=PyPI&color=3775a9" alt="PyPI"></a>
  <a href="https://crates.io/crates/docattest"><img src="https://img.shields.io/crates/v/docattest?label=crates.io&color=e57300" alt="crates.io"></a>
  <a href="https://pkg.go.dev/github.com/docattest/docattest/adapters/go"><img src="https://img.shields.io/badge/go-install-00add8" alt="Go"></a>
  <a href="https://github.com/docattest/docattest/blob/main/LICENSE"><img src="https://img.shields.io/github/license/docattest/docattest?color=17a35e" alt="MIT licence"></a>
</p>

---

A page says what the code does, and a comment says where the truth lives:

```md
A failing call is tried at most `3` times. <!-- fact: RETRY_DEFAULTS.maxAttempts -->
```

Someone raises the limit to 5 and forgets the docs:

```console
$ docattest check
docs/retries.md
  ✗ L1 fact: expected 3, got 5 from RETRY_DEFAULTS.maxAttempts
FAILED
```

| Language | Install |
|---|---|
| TypeScript, JavaScript | `npm install --save-dev docattest typescript` |
| Python | `pip install docattest` |
| Go | `go install github.com/docattest/docattest/adapters/go/cmd/...@latest` |
| Rust | `cargo install docattest` |

Works on the docs you already have, one page at a time. No generated files, no model calls.
