## Syed Muhammad Nafay Hassan Rizvi

Cybersecurity enthusiast and software developer. Most of what I build has to do
with trust boundaries — a proxy forwarding data it never checked, an admin panel
believing a value from the browser.

### Open source

**9 pull requests merged** into projects other people maintain. Each one started
with reproducing a bug or fuzzing the code to find one.

| Project | Merged fix |
|---|---|
| [TheAlgorithms/Python](https://github.com/TheAlgorithms/Python) | [`tree_sort` silently dropped duplicate values](https://github.com/TheAlgorithms/Python/pull/15381) · [`stalin_sort` raised `IndexError` on an empty list](https://github.com/TheAlgorithms/Python/pull/15382) · [`exponential_search` recursed forever below the first element](https://github.com/TheAlgorithms/Python/pull/15384) |
| [vadimdemedes/ink](https://github.com/vadimdemedes/ink) | [PTY tests spawned the wrong Node executable](https://github.com/vadimdemedes/ink/pull/1010) |
| [mampfes/hacs_waste_collection_schedule](https://github.com/mampfes/hacs_waste_collection_schedule) | Broken scrapers repaired after providers changed their sites: [Sjöbo](https://github.com/mampfes/hacs_waste_collection_schedule/pull/7468) · [Lindau](https://github.com/mampfes/hacs_waste_collection_schedule/pull/7469) · [RESO](https://github.com/mampfes/hacs_waste_collection_schedule/pull/7470) · [CIDIU](https://github.com/mampfes/hacs_waste_collection_schedule/pull/7471) · [Borlänge](https://github.com/mampfes/hacs_waste_collection_schedule/pull/7248) |

**Security tooling, under review**

- [microsoft/DevSkim#789](https://github.com/microsoft/DevSkim/pull/789) —
  a rule regex (DS440011) backtracked catastrophically: a 200 KB line took 51 s
  to scan. Rewrote it with a bounded quantifier and added a timing test.
- [github/codeql#22630](https://github.com/github/codeql/pull/22630) —
  the `actions/unpinned-tag` query trusted floating tags like `@v4` on
  "immutable" Actions. Only full versions and SHAs are immutable, so the query
  now flags the rest. Fixes [#22414](https://github.com/github/codeql/issues/22414).

**Bug reports that pinned down a root cause**

- [gradio-app/gradio#13781](https://github.com/gradio-app/gradio/issues/13781) —
  traced missing type stubs to a packaging path where the `.pyi` files are only
  generated as a side effect of importing the package, so a clean build ships
  `py.typed` with no stubs behind it
- [microsoft/playwright#42402](https://github.com/microsoft/playwright/issues/42402) —
  reproduced a libuv teardown crash on Windows and narrowed it to the update
  check's `fetch()` call

### llm-shield

[![tests](https://github.com/Darkslayer3324j/llm-Sheild/actions/workflows/tests.yml/badge.svg)](https://github.com/Darkslayer3324j/llm-Sheild/actions/workflows/tests.yml)
[![License: Apache 2.0](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/Darkslayer3324j/llm-Sheild/blob/main/LICENSE)

A local, zero-trust LLM proxy. Point an OpenAI SDK, LangChain, or any HTTP
client at `localhost:8000/v1` instead of the provider, and every request gets
PII-scrubbed, cost-tracked, rate-limited and cached — streaming included —
whether it's headed to OpenAI, Anthropic, Gemini or a local Ollama model.

Python · FastAPI · SQLite · Docker

The interesting part is the sanitizer: reversible placeholders, Luhn-validated
card detection, and structurally-validated SSNs, so it redacts without
mangling order numbers. Nothing leaves the machine except the sanitized
request.

### What I work on

**Security** — redaction engines, auth boundaries, and the general problem of
code that checks something in the browser and calls it authentication. Mostly
this means checking whether a tool actually does what it says, and adding a
test once it does — including tools that do the checking for other people
(DevSkim, CodeQL).

**Backends** — Python and FastAPI mostly. Provider adapters, streaming, caching,
usage accounting.

**Web** — ordering systems and admin tooling in HTML/JS, plus TypeScript.

### Toolbox

`Python` `FastAPI` `SQLite` `Docker` `JavaScript` `TypeScript` `HTML/CSS` `Git`

---

<sub>Reach me at nafayhassan3324j@gmail.com</sub>
