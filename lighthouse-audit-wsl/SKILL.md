---
name: lighthouse-audit-wsl
description: Runs Lighthouse audits for local web applications inside WSL and guides agents to configure, execute, inspect, and act on Lighthouse reports. Use when the user asks to run Lighthouse, improve Lighthouse scores, audit performance, accessibility, SEO, or best practices, or set up Lighthouse for Claude Code, Codex, or another coding agent in WSL.
---

# Lighthouse Audit on WSL

## Instructions

Use repository-local configuration whenever possible.

Prefer adding Lighthouse as a dev dependency and exposing it through npm scripts. Do not rely on a global Lighthouse installation unless the repository already documents that approach.

```bash
npm i -D lighthouse
`````

Add scripts like these, adjusting the URL and port to the project.

`````json
{
      "scripts": {
              "lh": "lighthouse http://127.0.0.1:5173 --chrome-flags='--headless=new' --output html --output-path ./lighthouse-report.html",
                  "lh:json": "lighthouse http://127.0.0.1:5173 --chrome-flags='--headless=new' --output json --output-path ./lighthouse-report.json"
                    }
                    }
                    `````

## Browser requirement

Before running Lighthouse, verify that Node.js, npm, Lighthouse, and Chrome or Chromium are available inside WSL.

`````bash
node -v
npm -v
npx lighthouse --version
google-chrome --version || chromium --version || true
`````

If Chrome or Chromium is unavailable, install Chrome for Testing.

`````bash
npx @puppeteer/browsers install chrome@stable
`````

When Chrome is installed at a non-default path, set ```CHROME_PATH`.

```bash
CHROME_PATH=/path/to/chrome npm run lh
`````

Do not add ```--no-sandbox` by default. Add it only after Chrome fails with a sandbox-related error.

## Running the audit

Run the application and Lighthouse inside the same WSL distribution.

Prefer production builds when the framework supports them.

For Vite:

```bash
npm run build
npm run preview -- --host 127.0.0.1
npm run lh:json
`````

For Next.js:

`````bash
npm run build
npm run start
npm run lh:json
`````

If the project only supports a development server, use the documented dev command and the correct local port.

Check connectivity before running Lighthouse when the server status is unclear.

`````bash
curl -I http://127.0.0.1:5173
`````

## Acting on results

Read the JSON report for machine-readable audit details.

Use the HTML report for human review.

Fix concrete Lighthouse audit failures. Do not make broad refactors only to change the score.

Prioritize:

1. Accessibility failures with clear DOM or source locations
2. Broken metadata such as title, viewport, canonical, robots, and description
3. Missing image dimensions and incorrect responsive image sizing
4. Render-blocking resources
5. Excessive page JavaScript
6. Layout shift caused by missing dimensions or late-loading UI
7. Unused CSS or JavaScript

For accessibility issues, prefer native HTML semantics over ARIA. Add ARIA only when native HTML cannot express the required semantics.

## WSL rules

Use ```127.0.0.1` instead of `localhost` when DNS, proxy, or host resolution behavior is uncertain.

Do not assume Windows Chrome is available from WSL.

Do not put Windows paths in repository npm scripts.

Use Linux paths inside WSL.

Good:

```bash
CHROME_PATH=/home/user/.cache/puppeteer/chrome/linux-*/chrome-linux64/chrome
`````

Bad:

`````bash
CHROME_PATH=C:\\Program Files\\Google\\Chrome\\Application\\chrome.exe
`````

## Completion criteria

When completing a Lighthouse task, report:

- the command used
- the audited URL
- the report path
- the main failing audit items
- the source files changed
- whether Lighthouse was re-run after the changes

Do not claim a score improvement unless Lighthouse was re-run after the relevant changes.````

