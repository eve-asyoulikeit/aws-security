# Prowler 5.44.0

**Source:** https://github.com/prowler-cloud/prowler/releases/tag/5.44.0
**Date:** 2026-09-29
**Tags:** #tooling #compliance #prowler

Prowler 5.44.0 adds a partial-scan "re-check" that re-runs only the checks for one just-remediated resource instead of waiting on a full scan, a one-step AWS account-connect wizard (role assumed and tested in a single submit), and S3-compatible/air-gapped self-hosted storage support (MinIO via a dedicated endpoint variable, SigV4-signed downloads for SSE-KMS-encrypted buckets). Changes how remediation verification and self-hosted deployments work, not just a version bump.

## See also
- [Prowler 5.43.0](tooling/prowler-5-43-0.md)
- [Prowler 5.42.0](tooling/prowler-5-42-0.md)
