## Syed Muhammad Nafay Hassan Rizvi

Cybersecurity enthusiast and software developer. Most of what I build sits at
the point where a system trusts something it shouldn't — a proxy that forwards
data it never checked, an admin panel that believes a value from the browser.

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
code that checks something in the browser and calls it authentication. I like
finding the gap between what a tool claims and what it actually does, then
writing the test that keeps it closed.

**Backends** — Python and FastAPI mostly. Provider adapters, streaming, caching,
usage accounting.

**Web** — ordering systems and admin tooling in HTML/JS, plus TypeScript.

### Open source

I contribute where I can reproduce something others can't, which usually means
Windows-specific behaviour:

- [gradio-app/gradio#13781](https://github.com/gradio-app/gradio/issues/13781) —
  traced missing type stubs to a packaging path where the `.pyi` files are only
  generated as a side effect of importing the package, so a clean build ships
  `py.typed` with no stubs behind it
- [microsoft/playwright#42402](https://github.com/microsoft/playwright/issues/42402) —
  reproduced a libuv teardown crash on Windows and isolated it to the CLI's
  update check

### Toolbox

`Python` `FastAPI` `SQLite` `Docker` `JavaScript` `TypeScript` `HTML/CSS` `Git`

---

<sub>Reach me at nafayhassan3324j@gmail.com</sub>
