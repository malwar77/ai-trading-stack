# Contributing Guide

Thank you for contributing to the AI Trading Stack repository! This guide details how our automated link verification works, how to investigate failures, and how to handle false positives.

---

## 1. Automated Link Check Workflow

We use a GitHub Actions workflow (`.github/workflows/link-check.yml`) powered by [Lychee](https://github.com/lycheeverse/lychee) to verify that every URL in `README.md` is alive, reachable, and not redirected.

* **Trigger**: Runs on every `push` and `pull_request` targeting `main` that modifies `README.md`, every Monday at 06:00 UTC, and via manual `workflow_dispatch`.
* **Zero Redirect Policy (`--max-redirects 0`)**: Any redirected URL (such as HTTP -> HTTPS or renamed repository path) will fail the check so links remain canonical and up to date.

---

## 2. Reviewing Workflow Failures

When a link check fails:

1. Open the [Actions tab](https://github.com/malwar77/ai-trading-stack/actions) and click on the failed **Link Check** run.
2. Check the **Job Summary** or inspect the automatic GitHub Issue opened by the workflow.
3. Common error codes:
   * `404 Not Found`: Repository moved, renamed, or deleted. Update the link to the canonical location or find an official replacement.
   * `301 / 302 / 308 Redirect`: The link was redirected. Replace the link with the exact target destination URL.
   * `429 Too Many Requests`: Rate-limiting by external providers.

---

## 3. Handling False Positives & Edge Cases

Some external sites or documentation endpoints block automated scrapers or return `403 Forbidden` / `429 Too Many Requests` despite being valid in a regular browser.

If you encounter a confirmed false positive:

1. Edit `.github/workflows/link-check.yml`.
2. Add an `--exclude` argument to the Lychee step with a regex or exact domain:
   ```yaml
   args: >-
     --verbose
     --no-progress
     --max-redirects 0
     --timeout 20
     --exclude "https://example-rate-limited-domain.com/.*"
     ./README.md
   ```
3. Open a Pull Request detailing why the URL was excluded.

---

## 4. Proposing New Repositories

When recommending a new open-source repository for the stack:

* The repository must be active and open-source with an OSI-approved license.
* It must address a distinct phase of quantitative trading (data, strategy, backtesting, risk, execution, or agent runtime).
* Include a verified GitHub REST API source link and factual description in the verification table.
