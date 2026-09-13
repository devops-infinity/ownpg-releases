# OwnPG releases

Release artifacts, installers, and bug reports for OwnPG, the PostgreSQL DBA tool for AI clients over the Model Context Protocol. The source repository is private; this repository is where every install path resolves and where problems are reported.

## Status

OwnPG is in development. No version has been released yet. The first release appears on the Releases page of this repository when the maintainer declares the tool stable.

## Prerequisites

- A reachable PostgreSQL server, version 14 through 18.
- Rust 1.89 or newer, only if you install with `cargo install` or `cargo binstall`.

## Installing

Every path below resolves against the releases here.

- From crates.io, building locally: `cargo install ownpg --locked`
- A prebuilt binary through cargo: `cargo binstall ownpg`
- The shell installer (macOS and Linux) and the PowerShell installer (Windows) are attached to every release.
- Homebrew: `brew install devops-infinity/tap/ownpg`
- npm: `npm install -g @devops-infinity/ownpg`

Eight prebuilt targets ship with every release: macOS on Apple Silicon and Intel, Linux with glibc and fully static with musl on x86_64 and aarch64, and Windows on x86_64 and ARM64.

## Usage

Serve one database over stdio, read-only, with the default schema `public`:

```
ownpg serve -d app
```

Run `ownpg doctor` to check the connection before serving it live, and `ownpg man` for the full command reference.

## Verifying a download

Every release carries `sha256.sum` with the checksum of every archive, and `sha256.sum.minisig`, a `minisign` signature over that file. The public key is published in this README at the first release. Verify with `minisign -Vm sha256.sum -P <public key>`, then `sha256sum -c sha256.sum` (or `shasum -a 256 -c` on macOS). Every archive also carries a CycloneDX SBOM and `THIRD-PARTY.txt` with the license of every dependency, and the binary embeds its dependency list for `cargo audit bin`.

## Reporting a problem

Open an issue here with the template that fits: a bug, or a connection problem. Include the `ownpg --version` line and the `ownpg doctor` output with any password removed.

Security problems go through private vulnerability reporting on this repository, never through a public issue. See `SECURITY.md`.

## Maintenance

OwnPG has one maintainer and one publisher. Outside code contributions are not accepted; bug reports are welcome. A successor will be named before the project is relied on by others.

## License

The artifacts are licensed under either of the MIT license ([LICENSE-MIT](LICENSE-MIT)) or the Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE)), at your option.
