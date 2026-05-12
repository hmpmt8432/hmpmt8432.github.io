# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository purpose

Personal portfolio site for Jeremiah Cornelius, focused on project/program management and cybersecurity homelab work. Published via GitHub Pages at `hmpmt8432.github.io`.

## Stack

- **Jekyll** site built and served by GitHub Pages (no custom Gemfile, no build script committed).
- **Theme**: `jekyll-theme-hacker` (configured in `_config.yml`).
- All content lives at the repo root as front-matter Markdown pages — there is no `_layouts/`, `_includes/`, `_posts/`, or `assets/` directory yet.

## Build / preview

There is no local build tooling configured. GitHub Pages builds and deploys automatically when changes land on the default branch (`main`). To preview locally, a contributor would need to run Jekyll with the `github-pages` gem themselves; nothing in the repo automates that.

## Page conventions

- Every page begins with YAML front matter containing at least `title:` (see `index.md`, `about.md`, etc.).
- `_config.yml` sets the site `title`, `description`, and `theme`. `google_analytics` is intentionally left blank.
- Pages link to each other with root-relative URLs (`/about`, `/homelab`, `/resume`, `/certifications`, `/project-management`).

## Known structural gap

`index.md` and `homelab.md` link to project detail pages under `/projects/...` (e.g. `/projects/homelab-architecture`, `/projects/pfsense-network-segmentation`, `/projects/active-directory-lab`, `/projects/domain-joined-workstation`, `/projects/centralized-logging-siem`). **No `projects/` directory or files exist yet** — those links currently 404. When adding a referenced project, create it as `projects/<slug>.md` (or `projects/<slug>/index.md`) with matching front matter so the existing links resolve.

## Content style

Existing pages follow a consistent voice and structure (purpose, scope, focus areas, roadmap, lessons learned). When adding new project pages, match the documentation pattern called out in `homelab.md`: purpose and scope, architecture/design, implementation steps, security value, challenges, outcomes, lessons learned, supporting artifacts.

## Placeholders to be aware of

Several pages contain literal placeholder text the author has not yet filled in — do not treat these as bugs unless asked to replace them:
- `resume.md`: "Add downloadable PDF link here", "Add LinkedIn profile link here".
- `certifications.md`: "Add your degree information here in the format you prefer."
- `index.md`: LinkedIn line reads `add-your-link-here`.
