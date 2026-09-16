# AWS STS simplifies session token size limits and adds session token size monitoring

**Source:** 4310321b5bbaec5ed0fa81752fad3a7e52ccc318
**Date:** 2026-09-16
**Tags:** iam, sts

AWS STS replaces its separate packed-policy-size and overall-token-size limits with a single 4,096-byte session token limit, and now reports `SessionTokenSize`/`SessionTokenUtilization` in API responses, CloudTrail, and CloudWatch, plus a new `MinimumSessionTokenSize` testing parameter. Actionable for anyone building session-tag/ABAC policies against the old dual-limit behavior, and gives defenders a new signal (unusually large or near-limit session tokens) to monitor for abuse.
