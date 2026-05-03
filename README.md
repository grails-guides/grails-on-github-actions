# grails-github-actions-cicd

Sample app for the apache/grails-static-website guide [grails-github-actions-cicd/v8](https://grails.apache.org/guides/grails-github-actions-cicd/8/guide/index.html).

The default branch (`grails8`) demonstrates a full CI/CD pipeline for a Grails 8 application:

- `.github/workflows/ci.yml` - validation -> unit -> integration -> functional job graph, with PostgreSQL service containers and Geb functional tests
- `.github/workflows/release.yml` - tag-triggered release that builds the OCI image via `bootBuildImage`, pushes to GHCR, and creates a GitHub Release with the bootJar attached
- `.github/dependabot.yml` - weekly Gradle and GitHub Actions updates with grouped Grails / Spring / testing PRs

`initial/` is the vanilla forge starter (`postgres`, `testcontainers`, `geb-with-webdriver-binaries` features). `complete/` is the same starter with all CI/CD wiring applied.

[![CI](https://github.com/grails-guides/grails-github-actions-cicd/actions/workflows/ci.yml/badge.svg?branch=grails8)](https://github.com/grails-guides/grails-github-actions-cicd/actions/workflows/ci.yml)

## Earlier Grails versions

The older Grails 4 sample for the [Grails on GitHub Actions](https://grails.apache.org/guides/grails-on-github-actions/4/guide/index.html) guide remains on the `master` branch.
