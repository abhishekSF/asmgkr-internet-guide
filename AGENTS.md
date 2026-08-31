# AGENTS.md

## Cursor Cloud specific instructions

This repo is a single, self-contained static website (`index.html`) — an internet/broadband guide for Hyderabad ("HyderabadNet"). All HTML, CSS, and JavaScript are inlined in `index.html`, and all data (ISP plans, router picks, comparison rows) is hard-coded in the page. `PLAN.md` is product/roadmap documentation.

- No dependencies, package manager, or build step. There is nothing to install, compile, or bundle; the deployable artifact is `index.html` itself.
- No backend, database, or external runtime services. Outbound `<a target="_blank">` links to ISP sites are informational only.
- No lint or automated test tooling is configured in the repo. Testing is manual (exercise the interactive features in a browser).

### Run it (development preview)

Serve the folder with any static file server and open it in a browser:

```
python3 -m http.server 8000   # then visit http://localhost:8000
```

Opening `index.html` via `file://` also works, but serving over HTTP is closer to the GitHub/Cloudflare Pages deployment target described in `PLAN.md`.

### Interactive features to smoke-test

- Router Recommender ("Find the Right Router"): set the dropdowns and click "Find My Router" — recommendations render into `#routerOut`.
- ISP Encyclopedia: click an ISP row to expand/collapse its plan cards.
- Plan Comparison, Security Audit, and Glossary sections.
