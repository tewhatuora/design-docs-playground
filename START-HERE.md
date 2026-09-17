# Getting Started

This document contains instructions for bootstrapping a new project from a copy of the template repository, and instructions for setting up a local development environment.

Note: a local development environment is optional, and most suited to doing a lot of contributing or when customising the theme etc. Simple changes (depending on repository configuration) could be made directly through the web UI of Gitlab or Github.

While this template supports publishing the site to Gitlab Pages or Github pages via CI pipelines, it is possible to build the site locally and publish to some other destination.

## Technologies

- [MkDocs](https://www.mkdocs.org/) : a python project for building a static site out of markdown files.
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) : a sophisticated theme for mkdocs.
- [Mermaid](https://mermaid.ai/open-source/intro/) : a plain text diagram definition format that can be rendered to SVG images.

## Bootstrapping a new project

This only needs to be done once per project, just after a new repository has been created from the template. Future contributors don't need to follow the project bootstrap steps.

### Initial config edits

Look for settings marked with `# <- EDIT` comments in the `mkdocs.yml` and `pyproject.toml` files and change to better suit the new project.

### Publishing setup for Gitlab Pages

From within your Gitlab project, select `Deploy` then `Pages` from the menu on the left hand side.

There you can find settings for domains etc.

### Publishing setup for Github Pages 

Go to `Settings` > `Pages` to enable Pages.

Under "Build and Deployment" set the Source to be "Github Actions".

You can optionally set a custom domain name. Doing so will require cooperation of the team in charge of managing that domain name. The Pages settings page will detail what needs to be set in DNS.

Note: in the public `tewhatuora` Github Organisation, only public repositories can enable Github Pages. This restriction doesn't apply in the `healthnz` Github Enterprise.


## Local Build and Preview

To edit, build and test locally on your own computer, you'll need to set up your local environment.

### Prequisites

- [uv](https://docs.astral.sh/uv/getting-started/installation/) : A package mangement tool for Python.
- [nvm](https://www.nvmnode.com/guide/introduction.html) : A tool for installing and managing NodeJS versions.

Optional: GNU Make will be very handy for simplfying the development workflow. On Windows, install via Chocolately: `choco install make`. On a Mac it is included as part of the XCode Command line tools, or installed via `brew`. On Linux, install via your distros package manager.

### Set up Python

From the project root directory, run `uv python install`. This will install the version specified in the `.python-version` file, and ensure you use the same version as other contributors and the CI pipelines.

### Set up NodeJS

From the project root directory, run `nvm install`. This will install the version specified in the `.nvmrc` file, and ensure you use the same version as other contributors and the CI pipelines.

### Install dependencies

From the project root directory run `make init` to install all the Python and Javascript packages needed for mkdocs.

This will create a new `uv.lock` file in the root directory that you should commit to git.

If you don't have `make` installed, you can run `uv sync` directly for this step.

### Make tasks

- `make` reminds you of the available tasks in case you forget.
- `make init` installs project dependencies with `uv`.
- `make serve` starts MkDocs' local live-reloading server running at `http://127.0.0.1:8000/` by default.
- `make build` builds the static site into `public/`.

Note: If you don't have `make` installed, look in `Makefile` to see the actual commands to run for those tasks.

### Committing changes

CI only runs once a merge request is merged into the default branch; it does not validate an open merge request beforehand, so check a change locally with `make serve` or `make build` before merging.
