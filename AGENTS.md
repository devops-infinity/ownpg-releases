# OwnPG releases agent instructions

Instructions for an AI agent working in this repository. `CLAUDE.md` and `AGENTS.md` carry identical text under two names, so every tool finds the rules under the name it looks for. Change one and copy it to the other in the same run.

## What this repository is

This repository holds no source code. It is the public install, release, and issue-reporting hub for OwnPG, whose source lives in the `devops-infinity/ownpg` repository. Its only tracked content is `README.md`, `SECURITY.md`, two license files, and three GitHub issue-form templates under `.github/ISSUE_TEMPLATE/`.

See `README.md` for the install paths and `SECURITY.md` for the vulnerability-reporting process; this file does not restate either.

## How a release actually gets here

A GitHub Release on this repository, its binaries, `sha256.sum`, `sha256.sum.minisig`, and its SBOM, is written by the `ownpg` repository's own release script, run by hand from that repository, never from here. This repository has no `.github/workflows/` directory and runs no CI of its own. The Homebrew formula for OwnPG does not live here either; it goes to the separate `devops-infinity/homebrew-tap` repository.

## Do

- Edit `README.md`, `SECURITY.md`, an issue template, or a license file by hand when asked to change this repository's own documentation.
- Address every sentence to a public, external reader. This repository once carried an internal maintainer title in its README; keep that mistake from coming back.

## Don't

- Don't hand-create or hand-edit a GitHub Release, a release binary, a checksum file, or a signature here. The `ownpg` repository's release process writes them, and a hand edit gets overwritten or falls out of sync with what that process expects.
- Don't add a `.github/workflows/` directory on the assumption one is missing by oversight. This repository runs no CI by design.
- Don't add a `Formula/` directory here. The Homebrew tap is `devops-infinity/homebrew-tap`.
- Don't reconfigure GitHub's private vulnerability reporting on this repository. It is already enabled, matching what `SECURITY.md` documents as live.
