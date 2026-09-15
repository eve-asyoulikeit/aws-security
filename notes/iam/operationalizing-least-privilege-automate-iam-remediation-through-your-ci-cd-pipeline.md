# Operationalizing least privilege: Automate IAM remediation through your CI/CD pipeline

**Source:** 655dce2552e057a970b7bf591d74f47f0fc54ff5
**Date:** 2026-09-15
**Tags:** iam, automation, ci-cd

Describes an automated remediation workflow that turns AWS IAM Access Analyzer's unused-permission findings into action instead of a growing backlog: it classifies each flagged role by how it was created and produces a ready-to-review artifact per case — a pull request with generated CDK code for IaC-managed roles, an issue with the recommended policy plus migration guidance for console-created roles, or a soft-disable issue with a monitored decommission plan for unused principals. Actionable because it closes the gap between detection (which Access Analyzer already does well) and durable remediation (which manual right-sizing loses on the next IaC deployment), directly reducing standing excess-permission attack surface at scale.
