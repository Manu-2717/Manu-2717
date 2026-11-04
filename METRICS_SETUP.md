# Profile Metrics setup

The profile repository is [`Manu-2717/Manu-2717`](https://github.com/Manu-2717/Manu-2717). Its workflow generates four SVGs in `assets/metrics/` and commits them to `main` daily at 02:17 UTC. The workflow can also be run manually.

## 1. Create the read token

GitHub Metrics needs a personal access token to query profile wide data. Create a classic personal access token at **GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)**. For public GitHub data, start with no additional scopes. If you want private repository metrics, grant the `repo` scope and review the access this grants carefully. Give the token an expiration date and rotate it before it expires. The token value must never be placed in the README or workflow file.

In this repository, go to **Settings → Secrets and variables → Actions → New repository secret**. Name it exactly `METRICS_TOKEN` and paste the token. The workflow uses the built in `GITHUB_TOKEN` for commits through the Metrics action; it does not need a second write token.

## 2. Enable workflow writes

In **Settings → Actions → General**, enable GitHub Actions and set **Workflow permissions** to **Read and write permissions** if the repository policy requires this for automated commits. The workflow also declares `contents: write`. If branch protection blocks automated commits to `main`, allow the workflow bot to write or adapt the output branch strategy.

## 3. Run it

Open **Actions → GitHub Metrics → Run workflow**, select `main`, and run. Wait for all four steps to succeed. Confirm that `assets/metrics/contributions.svg`, `overview.svg`, `activity.svg`, and `achievements.svg` exist on `main`, then reload the profile. The README image references will render after this first successful run.

If the action reports missing data, check token expiration and access. Public metrics may omit private activity. GitHub Metrics does not provide a verified current and longest streak pair, so those values are deliberately absent. GitHub Markdown follows the viewer's theme; the dark banner and badge palette are fixed, but the page background itself cannot be forced dark.

## Customize

Edit the four `with:` blocks in `.github/workflows/metrics.yml` to change plugin sections, then manually rerun the workflow. GitHub Metrics plugin options are documented in the [official project](https://github.com/lowlighter/metrics). The README uses relative SVG paths so the generated assets remain tied to this repository.
