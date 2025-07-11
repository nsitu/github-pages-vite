# github-pages-vite
Template for using Vite with GitHub Pages

## GitHub Action
This template includes a GitHub Action workflow at `.github/workflows/main.yml`. The Action builds the Vite app to `/dest`. It then deploys the contents of `/dest` to production at `https://user.github.io/repository` 

## Vite Config
When deploying a repo to GitHub Pages, the repository name becomes part of the URL path. Vite has been configured in `vite.config.js` in order to dynamically understand this path based on a falg in the GitHub Actions build environment. During local development, Vite will assume a root of `/` but when building for produciton, it will instead use `/repository-name/` as the root.
