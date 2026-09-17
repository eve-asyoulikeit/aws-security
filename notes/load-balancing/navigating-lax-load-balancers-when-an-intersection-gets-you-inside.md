# Navigating Lax Load Balancers: When an Intersection Gets You Inside

**Source:** https://blog.doyensec.com/2026/05/25/cloudsectidbits-elbaph-alb
**Date:** 2026-09-17
**Tags:** load-balancing, misconfiguration, waf-bypass

Standard AWS ELB/ALB reviews check resource-level hygiene (TLS policy, security groups, WAF attachment) but rarely trace the actual reachable routing graph. Doyensec catalog the recurring gaps this misses: an Internet-facing origin ALB behind CloudFront that's still directly reachable (bypassing every WAF rule), listener rule shadowing where a broad low-priority rule matches before a restrictive `authenticate-oidc` rule, and target groups reachable through a second listener or path that lacks the source-IP or auth gate applied to the "intended" one.
