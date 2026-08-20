# AGENTS.md

## Cursor Cloud specific instructions

### What this repository is
- This is a **documentation-only** repository: an LLM interview Q&A book written in Chinese Markdown.
- Content lives in `chapter1.md` … `chapter6.md` at the repo root. There is **no application source code, build system, package manifest, automated tests, lint config, Dockerfile, or CI**.
- Because there is nothing to compile or run as a service, "development" here means **editing the Markdown chapters**. There are no build/test/lint commands defined by the repo.

### Previewing rendered content (optional dev workflow)
- Nothing is committed to render the docs, so preview tooling is not part of the repo. The one optional dev dependency is the Python `markdown` library (installed by the environment update script).
- Quick single-file render: `python3 -m markdown chapter1.md > /tmp/chapter1.html` (write output outside the repo so you don't commit generated HTML).
- To browse all chapters as a rendered site, generate HTML into a temp dir and serve it, e.g. `python3 -m http.server 8000` from that dir, then open `http://localhost:8000`. Do not serve raw `.md` over HTTP — browsers download it instead of rendering.
- Chinese text renders correctly as long as files are read/written as UTF-8.
