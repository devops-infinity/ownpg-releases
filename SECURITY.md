# Security policy

## Supported versions

`ownpg` is in development. No version has been released yet. Once one ships, the most recent release receives security fixes.

## Reporting a vulnerability

Report a vulnerability privately through GitHub's private vulnerability reporting on this repository: https://github.com/devops-infinity/ownpg-releases/security/advisories/new. Do not open a public issue for a security problem. If private vulnerability reporting is unavailable to you, email sazzad@devops.bd instead.

Include the affected version, the steps to reproduce it, and the impact.

Expect an acknowledgement within seven days and an assessment within fourteen. A critical issue is fixed within seven days of the report, a high one within thirty, and the rest in the next minor release. A fix ships as a patch release on every install path on the same day, with an advisory here and, for the `ownpg-core` crate, a RustSec advisory.

## Scope

A report is in scope when it affects `ownpg` itself: the binary, the published crates, or an artifact distributed from this repository's releases, including a compromised release artifact or a checksum or signature that does not match.

A report about the PostgreSQL server, role, or network you configured `ownpg` to connect to is out of scope. Securing that connection is yours to do.
