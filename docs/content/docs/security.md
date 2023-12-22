---
prev: /advanced-topics
title: Security
weight: 3
---

## Proactive detection of vulnerabilities

At each build, a vulnerability scan is performed on the system. If a vulnerability that can be upgraded is detected, the build is stopped and the image is not pushed to the registry. Vulnerability is reported in [GitHub Security](https://docs.github.com/en/code-security/code-scanning/automatically-scanning-your-code-for-vulnerabilities-and-errors/about-code-scanning). The maintainers are alterted and have access to reports.

Automation is supported by [Snyk](https://snyk.io) and [Semgrep](https://semgrep.dev). Helm chart, configuration files, and containers, are scanned for vulnerabilities and misconfigurations.
