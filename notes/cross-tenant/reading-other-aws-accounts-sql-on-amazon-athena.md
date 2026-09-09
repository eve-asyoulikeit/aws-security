# Reading other AWS accounts' SQL on Amazon Athena

**Source:** https://act.security/resources/reading-other-aws-accounts-sql-on-amazon-athena
**Date:** 2026-09-09
**Tags:** cross-tenant, athena, trino

Act Security found that Athena's `StartQueryExecution` API let a caller pass `Catalog=system` via the `QueryExecutionContext` parameter (rather than in the SQL text, which is blocked) to query Trino's built-in `system.runtime.queries` table directly. That table exposed full SQL text and account IDs of other, unrelated AWS accounts' recent queries (up to ~54 minutes of history), affecting 102 of 109 test landings. AWS fixed it globally within 4 days of report (Aug 6-10 2026); no CVE was assigned since no customer action was required, but it's a useful case study in shared-infra/multi-tenant isolation failures for anyone assessing or building on similar serverless query services.
