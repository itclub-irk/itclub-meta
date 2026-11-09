# AGENTS.md — instructions for AI agents

Workspace `~/itclub` is **not** a mono-repo: it is a meta-repository with independent
git repos in `repos/`.

## Workspace structure

```
/home/maxp/itclub
├── .git                     # root repo git@github.com:itclub-irk/itclub-meta.git (branch main)
├── .gitignore               # ignores /repos/*
├── AGENTS.md
└── repos/                   # independent projects, its own .git in each, NOT tracked by the root
    ├── community/           # project of community rules (rules.md) + QR
    ├── itclub-irk.github.io/# Hugo (PaperMod) website of the club https://itclub-irk.ru
    ├── itclub_chat_bot/     # Telegram chat bot in Clojure
    └── microfest/           # festival rules "Useful Microelectronics" (rules.md)
```

## Key rules

- **Each dir in `repos/` is a separate git repo.** `cd` into it; commits/pushes are done there.
  Do not commit `repos/*` into the root repo — the root tracks only `README.md`, `AGENTS.md`
  (and `.gitignore`); materials live outside git.
- Remote of the root repo — `git@github.com:itclub-irk/itclub-meta.git`
  (itclub-meta, branch `main`).
- READMEs of `itclub_chat_bot` and `microfest` have `?TBD?` — documentation not written.
- Markdown: max line length — 100 chars in all `.md` files of the workspace *and* its repos
  (`MD013` in `.markdownlint.json`); keep lines shorter.
- Table separators use the spaced style `| --- | --- |`, matching the header row (`MD060`).
- There is `.env` in `itclub_chat_bot` with `TELEGRAM_APIKEY` — do not read, print,
  or commit its value.

## Repositories

### repos/itclub_chat_bot — Telegram chat bot (Clojure)

- Stack: Clojure 1.12, deps.edn; key libs: http-kit, mount, malli, jsonista, telemere, portal/nrepl.
- Entry point: `src/itbot/main.clj` (`itbot.main`), config — `src/itbot/config.clj`,
  helper libraries in `src/mlib`.
- Run in dev: `make dev` (starts nrepl with portal; loads `.env` implicitly).
- Build: `make build` (uberjar `target/itbot.jar`), `make clean`,
  dependency check — `make outdated`.
- Deploy: `make deploy` (scp to prod; PROD_HOST in the Makefile is a placeholder `XXX_myhost_XXX`).

### repos/itclub-irk.github.io — website (Hugo)

- Theme PaperMod — a submodule in `themes/PaperMod` (pin is a submodule with `master` head).
- Config: `hugo.yaml`; content in `content/` (about, news, events, projects, resources,
  rules, community); language `ru`.
- Local check: `hugo server`; publication — via GitHub Pages, `.github/workflows/`
  (workflow `gh-pages.yml_tmp` is a draft).
- PRs are made in the upstream repo https://github.com/itclub-irk/itclub-irk.github.io
  (contribution process in README).
