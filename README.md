This repository contains a strategy to release winget packages every time the RSS feed gets updated.

It is composed of an n8n instance and a GitHub Action.
- The n8n workflow defined in [Release WinGet packages.json](./Release%20WinGet%20packages.json) can be imported into an n8n instance, defined by the [docker-compose.yml](./docker-compose.yml).
- The [GitHub action](.github/workflows/release-winget-pkg.yml) can attempt a release of any existing package by manually triggering it or by calling it via the GitHub API. See the `inputs` for reference.