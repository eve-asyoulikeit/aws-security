# Transforming Bedrock Guardrails events into OCSF with CloudWatch

**Source:** a0a2ba82eb2fee43eebb7373c4985ea8fdd6fd7e
**Date:** 2026-09-21
**Tags:** detection-engineering, bedrock, ocsf

Walks through normalizing AWS Bedrock Guardrails intervention events (prompt injection blocks, PII redaction, harmful-content blocks) into OCSF Detection Finding records and landing them in the CloudWatch unified data store, so they can be correlated with CloudTrail and VPC Flow Logs via Athena or CloudWatch Logs Insights. This complements GuardDuty AI Protection's managed findings by exposing the raw guardrail telemetry for custom cross-source correlation and trend analysis, directly useful for building AI-aware SOC detections on AWS.
