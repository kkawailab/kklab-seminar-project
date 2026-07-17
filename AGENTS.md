# Repository Guidelines

## Project Structure & Module Organization

This is a documentation repository for kklab graduation-project reports; it contains no application source code. `graduation_project_template.md` is the canonical 20-section Japanese report template. `graduation_project_example.md` demonstrates a completed fictional submission and should stay aligned with the template. `CLAUDE.md` records repository-specific editing rules. Place report images in `images/` when needed, using descriptive lowercase names such as `images/main-screen.png`.

## Development and Validation Commands

There is no build system, package manager, linter, or automated test suite. Use lightweight checks before submitting changes:

```bash
git diff --check
git diff --stat
rg -n '^#{1,6} ' graduation_project_*.md
```

`git diff --check` catches whitespace errors, `git diff --stat` confirms the intended scope, and the heading search helps verify section numbering. Preview edited files in a GitHub-compatible Markdown renderer so tables, image links, and Mermaid diagrams render correctly.

## Writing Style & Naming Conventions

Write report content and instructions in Japanese. Match the existing direct `〜である` and instructional `〜してください` styles. Preserve the template’s numbered hierarchy, horizontal separators, GitHub Flavored Markdown tables, and fenced `mermaid` blocks. Use spaces rather than tabs and keep one blank line around headings, lists, tables, and code fences. Name new Markdown files and assets with clear lowercase snake-case or kebab-case names; avoid spaces. Keep SF prototyping and generative-AI usage records intact when revising the template.

## Review Guidelines

Treat the rendered document as the test target. Confirm that headings remain sequential, template placeholders are intentional, internal links resolve, image paths use `images/`, and the example still covers the template’s applicable sections. If changing a prompt or section, update the corresponding example where necessary. Do not publish student IDs, API keys, credentials, or real personal data; example people, URLs, and metrics must be clearly fictional or properly sourced.

## Commit & Pull Request Guidelines

Recent commits use concise Japanese summaries without prefixes, ending in an action such as `追加` or `変更` (for example, `テンプレートの記入例を追加`). Keep each commit focused on one documentation concern. Pull requests should summarize the affected sections, explain structural changes, link an issue when applicable, and include screenshots for meaningful Mermaid, table, or layout changes. State which manual checks were completed.
