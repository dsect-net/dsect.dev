# dsect.net

The public website of **DSECT** (Developmental Systems, Engineering & Computing Technologies),
served at **https://dsect.net**.

This repository was named `dsect.dev` when it was created; DSECT does not own that domain. The
site's canonical home is `dsect.net`.

## Layout

| path | what |
|---|---|
| `site/` | everything that is published: `index.html`, `404.html`, `assets/` |
| `site/assets/site.css` | styles; colour and type tokens mirror [`design-system`](https://github.com/dsect-net/design-system) `tokens.css` |
| `.github/workflows/deploy.yml` | deploys `site/` to GitHub Pages on every push to `main` |

Plain static HTML and CSS: no build step, no JavaScript, no tracking.

## Working on it

Follow the org [contributing guide](https://github.com/dsect-net/.github/blob/main/CONTRIBUTING.md):
branch from `main`, keep a pull request to one concern, and merge only after a self-check.

Preview locally:

```sh
python3 -m http.server 8000 -d site
```

Before merging, check:

- the page at 393px and 1440px widths
- keyboard navigation and visible focus
- nothing internal in `site/`: `grep -rE "100\.[0-9]+\.|ts\.net|agentmail|tailnet" site/` must print nothing

## Rules

- **Public by definition.** Nothing internal goes here: no private hostnames, internal addresses,
  agent inboxes or secrets. Internal DSECT services are never reachable through this site.
- Copy comes from the DSECT Charter. Changes to mission or positioning need Scotty's approval.

## License

Code: [Apache-2.0](LICENSE). The Inter font is under the SIL Open Font License
(`site/assets/fonts/LICENSE-Inter-OFL.txt`).
