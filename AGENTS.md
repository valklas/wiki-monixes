# AGENTS.md

## Project overview

Monixes is a lightweight Nix flake that provides reusable configuration
wrappers for NixOS and Home Manager. The flake exports:

- `nixosModules.default`
- `homeManagerModules.default`

This repository contains the user documentation for those modules. Keep
configuration options under the established namespaces:

- `monixes.system.*` for NixOS/system configuration
- `monixes.home.*` for Home Manager/user configuration

Keep the repository README focused on project identity and documentation
architecture. Put detailed feature documentation in the wiki pages.

## Required workflow

Before changing files:

1. Inspect the relevant source modules, README architecture, Git status, and
   recent history.
2. Explain the proposed approach, affected files, and any assumptions.
3. Ask the user for approval before implementing the change when working on an
   unrequested change.

During implementation:

- Prefer the smallest change that satisfies the request.
- Keep option names, defaults, examples, and links consistent with the source
  modules.
- Mirror the source module tree in the wiki: preserve directory names and
  module basenames, convert `.nix` module files to `.md`, and represent
  `default.nix` entry points with `README.md` pages. For example,
  `modules/nixos/desktop/DM/greetd-tuigreet.nix` maps to
  `system-modules/desktop/DM/greetd-tuigreet.md`.
- Keep one documentation page per independently configurable source module;
  use directory `README.md` files for indexes and composition entry points.
- Whenever a page or directory is added or removed, update the README's
  documentation architecture and file count in the same change.
- Do not document options that are not implemented in the Monixes source.
- Keep detailed feature documentation here rather than in the source README.

## Validation

After changes:

- Run `git diff --check`.
- Check all Markdown links and code examples affected by the change.
- Report any validation that could not run and why.

## Git and commits

- Make atomic commits: one feature, fix, refactor, or documentation change per
  commit.
- Do not commit or push unless the user requests it.
- Never rewrite history, reset, or discard user changes without explicit
  approval.

## Design direction

Monixes currently uses Catppuccin as its theme backend, exposed through the
unified `monixes.system.theme` and `monixes.home.theme` interfaces. Keep that
backend replaceable in documentation so a future theme backend can be adopted
without forcing users to change their Monixes option names.
