<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0b1120,50:1e3a8a,100:0ea5e9&height=190&section=header&text=Nafay%20Hassan%20Rizvi&fontSize=44&fontColor=ffffff&fontAlignY=36&desc=Security%20%C2%B7%20Backend%20%C2%B7%20Finding%20bugs%20other%20people%20ship&descSize=16&descAlignY=57" alt="Syed Muhammad Nafay Hassan Rizvi" />

<a href="mailto:nafayhassan3324j@gmail.com"><img src="https://img.shields.io/badge/Email-nafayhassan3324j@gmail.com-0ea5e9?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://github.com/Darkslayer3324j"><img src="https://img.shields.io/badge/GitHub-Darkslayer3324j-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
<img src="https://img.shields.io/badge/Open%20to-Backend%20%26%20Security%20roles-22c55e?style=for-the-badge" alt="Open to work" />

<br/><br/>

<img src="https://img.shields.io/badge/12-pull%20requests%20merged-1e3a8a?style=flat-square&labelColor=0b1120" alt="12 merged" />
<img src="https://img.shields.io/badge/311k%2B-stars%20on%20the%20projects%20I%20fixed-1e3a8a?style=flat-square&labelColor=0b1120" alt="311k stars" />
<img src="https://img.shields.io/badge/in%20review-GitHub%20%C2%B7%20Google-1e3a8a?style=flat-square&labelColor=0b1120" alt="In review at GitHub and Google" />

</div>

---

## Who I am

I'm a security-minded backend developer. Most of what I build lives on a trust
boundary — a proxy forwarding data it never inspected, an admin panel believing
a value straight from the browser — and most of what I fix upstream starts the
same way: **I reproduce the bug first, then write the test that proves it.**

I co-founded and lead the backend at **NoMansAi** (Node.js, Express, Redis,
n8n), and I spend the rest of my time finding real bugs in code that millions of
people depend on.

---

## What I've shipped upstream

**12 pull requests merged** into projects with **311,000+ combined stars**. No
typo fixes — every one is a behavioural bug, with a regression test that fails
without the patch.

| Project | ⭐ | What I fixed |
|---|---:|---|
| [**TheAlgorithms/Python**](https://github.com/TheAlgorithms/Python) | 224k | Four sorting and search bugs: [`tree_sort` dropped duplicates](https://github.com/TheAlgorithms/Python/pull/15381) · [`stalin_sort` crashed on empty input](https://github.com/TheAlgorithms/Python/pull/15382) · [`exponential_search` recursed forever](https://github.com/TheAlgorithms/Python/pull/15384) · [`flash_sort` crashed on repeats](https://github.com/TheAlgorithms/Python/pull/15380) |
| [**faif/python-patterns**](https://github.com/faif/python-patterns) | 43k | [The flyweight metaclass shared one instance across different arguments](https://github.com/faif/python-patterns/pull/495) |
| [**vadimdemedes/ink**](https://github.com/vadimdemedes/ink) | 39k | [PTY tests spawned the wrong Node executable](https://github.com/vadimdemedes/ink/pull/1010) |
| [**mampfes/hacs_waste_collection_schedule**](https://github.com/mampfes/hacs_waste_collection_schedule) | 2.2k | Five scrapers repaired after providers changed their sites: [Sjöbo](https://github.com/mampfes/hacs_waste_collection_schedule/pull/7468) · [Lindau](https://github.com/mampfes/hacs_waste_collection_schedule/pull/7469) · [RESO](https://github.com/mampfes/hacs_waste_collection_schedule/pull/7470) · [CIDIU](https://github.com/mampfes/hacs_waste_collection_schedule/pull/7471) · [Borlänge](https://github.com/mampfes/hacs_waste_collection_schedule/pull/7248) |
| [**microsoft/DevSkim**](https://github.com/microsoft/DevSkim) | 1k | [A security rule backtracked catastrophically](https://github.com/microsoft/DevSkim/pull/789) — one 200 KB line took **51 seconds** to scan. I rewrote the regex with a bounded quantifier and added a timing test. |

### In review at GitHub and Google

<img src="https://img.shields.io/badge/github%2Fcodeql-%2322630-181717?style=flat-square&logo=github&logoColor=white" alt="codeql PR" />

I fixed the `actions/unpinned-tag` query trusting floating tags like `@v4` on
"immutable" Actions. Only full versions and commit SHAs are actually immutable —
floating tags get moved — so the query now flags the rest.
[#22630](https://github.com/github/codeql/pull/22630), fixing
[#22414](https://github.com/github/codeql/issues/22414).

<img src="https://img.shields.io/badge/google%2Foss--fuzz-%2316170-4285F4?style=flat-square&logo=google&logoColor=white" alt="oss-fuzz PR" />

I found CIFuzz writing its SARIF report from whatever the *last* fuzz target
returned. In batch mode a crash found by any earlier target failed the build but
reached GitHub code scanning as an empty report — a silently missed finding.
[#16170](https://github.com/google/oss-fuzz/pull/16170).

---

## How I find them

> Most of these weren't reported by anyone. I went looking.

**Differential fuzzing** — I run reference implementations against the real ones
on random inputs. That's how I found the `interpolationSearch` infinite loop and
a linked-list corruption in
[trekhleb/javascript-algorithms](https://github.com/trekhleb/javascript-algorithms/pull/2219)
(196k ⭐).

**Measuring, not guessing** — for the DevSkim ReDoS I timed the real .NET engine
rather than trusting a Python regex model that over-reported it.

**Cross-platform reproduction** — I work on Windows, so I catch what Linux-only
CI never runs: a
[TypeScript path-separator bug](https://github.com/styled-components/styled-components/pull/5820)
in styled-components, a
[missing audio codec](https://github.com/ManimCommunity/manim/pull/5025) in
Manim, a
[libuv teardown crash](https://github.com/microsoft/playwright/issues/42402) in
Playwright, and a
[packaging path that ships `py.typed` with no stubs](https://github.com/gradio-app/gradio/issues/13781)
in Gradio.

---

## Projects

### llm-shield

[![tests](https://github.com/Darkslayer3324j/llm-Sheild/actions/workflows/tests.yml/badge.svg)](https://github.com/Darkslayer3324j/llm-Sheild/actions/workflows/tests.yml)
[![License: Apache 2.0](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/Darkslayer3324j/llm-Sheild/blob/main/LICENSE)

I built a local, zero-trust LLM proxy. Point an OpenAI SDK, LangChain or any
HTTP client at `localhost:8000/v1` instead of the provider, and every request
gets PII-scrubbed, cost-tracked, rate-limited and cached — streaming included —
whether it's headed to OpenAI, Anthropic, Gemini or a local Ollama model.

The part I care most about is the sanitizer: reversible placeholders,
Luhn-validated card detection and structurally-validated SSNs, so it redacts
without mangling order numbers. **Nothing leaves the machine except the
sanitized request.**

---

## Toolbox

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)

![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Godot](https://img.shields.io/badge/Godot-478CBF?style=for-the-badge&logo=godotengine&logoColor=white)

</div>

---

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Darkslayer3324j&show_icons=true&hide=stars&hide_border=true&theme=tokyonight&count_private=true&custom_title=My%20GitHub%20activity" alt="GitHub stats" height="165" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Darkslayer3324j&layout=compact&hide_border=true&theme=tokyonight&langs_count=6" alt="Top languages" height="165" />

<br/><br/>

**Looking for backend or security engineering work.** The fastest way to judge
me is the pull request list above — open any one of them.

<a href="mailto:nafayhassan3324j@gmail.com"><img src="https://img.shields.io/badge/Get%20in%20touch-nafayhassan3324j@gmail.com-0ea5e9?style=for-the-badge&logo=minutemailer&logoColor=white" alt="Contact" /></a>

<sub>Assisted with Claude.</sub>

</div>
