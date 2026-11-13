# AEGIS GitHub IP SHIELD

This repository-level workflow records a provenance snapshot on pushes, pull requests, manual runs and a weekly schedule.

## Recorded data
- Commit and tree IDs, branch/ref and workflow run identifiers.
- Tracked file paths, Git blob IDs and SHA-256 fingerprints (up to 25,000 files).
- Up to 500 commit metadata entries; author email is represented by SHA-256, not published in clear text.
- JSON report and checksum uploaded as a GitHub Actions artifact (90-day retention).
- Non-PR runs also preserve a versioned report on the `ip-shield-ledger` branch.

## Enablement
Merge this workflow into the default branch. GitHub Actions must be enabled and the workflow token must be permitted to write repository contents. If organization policy or branch rules block writes, artifact upload may still succeed while ledger preservation fails.

## Limits
Git commit author and timestamp fields are declared metadata, not verified identity or independently trusted time. Hashes prove byte identity, not authorship, originality, ownership or infringement. The runner clock is not a trusted timestamp authority. The ledger branch is version-controlled evidence, not immutable storage. This does not register copyright or patents, prevent copying, or revoke third-party rights. Contributions and licenses must be assessed separately.

This workflow covers only this repository and the refs that trigger it. It does not silently install itself in other repositories or monitor repositories outside the configured scope.
