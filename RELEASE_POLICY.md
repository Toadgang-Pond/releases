# Public release policy

## Purpose

This repository indexes **only releases explicitly approved for public distribution**. It is not a mirror of internal development work.

## Release gates

1. Confirm the intended source repository, exact immutable source commit, release scope, release owner, and license.
2. Confirm clean working tree and that the published source corresponds to the approved commit. Never force-push or rewrite approved history.
3. Pass the project's relevant required CI and security checks **on the exact release commit**.
4. Review dependencies, third-party notices, licenses, security-sensitive files, embedded credentials, and generated artifacts for public-distribution suitability.
5. Obtain explicit human release approval and publish a version tag that resolves to the approved commit.
6. Generate release binaries from the reviewed source using a documented build process; publish SHA-256 checksums and, when supported, signed attestations.
7. Publish release notes describing changes, platform support, known limitations, and rollback instructions.
8. Verify public download URLs and hashes after publication. Add only those verified links to the release index.

## Authority and safety

- Publishing is **manual and human-approved**, not triggered by routine merges.
- Private data, secrets, real user records, private keys, and incident evidence are never packaged.
- No release is described as secure, audited, or production-ready without evidence supporting that claim.
- Rollback or withdrawal must preserve an audit trail and clearly identify impacted versions.
- Project licensing decisions are made for each release; this index does not grant rights to unlicensed code.

## Provenance record

For every release, retain:

- Project name and public distribution repository
- Source repository and exact commit SHA
- Version and tag
- CI run IDs and conclusions for that commit
- Approver and approval date
- Artifact filenames, sizes, and SHA-256 hashes
- Build environment and instructions
- Release and rollback URLs
