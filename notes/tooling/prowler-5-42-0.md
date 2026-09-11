# Prowler 5.42.0

**Source:** tag:github.com,2008:Repository/66474729/5.42.0
**Date:** 2026-09-11
**Tags:** tooling, compliance, prowler

Prowler 5.42.0 adds native support for scanning AWS ISO partitions (`aws-iso`, `aws-iso-b`, `aws-iso-e`, `aws-iso-f`) from bundled botocore endpoint metadata, needing no network access or hand-edited region files, and lowers the default Boto3 connect timeout from 60s to 10s (configurable) to stop restricted-egress/GovCloud scans from stalling for hours. It also lets the Image provider reuse a persistent Trivy vulnerability database via `TRIVY_CACHE_DIR`, enabling offline/air-gapped image scanning, and fixes a broad set of duplicate/stale compliance-check references across 42 frameworks. These are workflow-changing fixes for anyone running Prowler against GovCloud, air-gapped, or ISO-partition AWS environments, not cosmetic version bumps.
