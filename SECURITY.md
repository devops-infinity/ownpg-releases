# Security policy

## Supported versions

OwnPG is in development. No version has been released yet. Once one ships, the most recent release receives security fixes.

## Reporting a vulnerability

Report a vulnerability privately through GitHub's private vulnerability reporting on this repository: https://github.com/devops-infinity/ownpg-releases/security/advisories/new. Do not open a public issue for a security problem. If private vulnerability reporting is unavailable to you, email sazzad@devops.bd instead.

Include the affected version, the steps to reproduce it, and the impact.

Expect acknowledgement within a few business days. Response time after that depends on severity and maintainer availability; OwnPG is pre-1.0 and does not commit to a fixed resolution deadline.

## Scope

A report is in scope when it affects OwnPG itself: the binary, the published crates, or an artifact distributed from this repository's releases, including a compromised release artifact or a checksum or signature that does not match.

A report about the PostgreSQL server, role, or network you configured OwnPG to connect to is out of scope. Securing that connection is yours to do.
