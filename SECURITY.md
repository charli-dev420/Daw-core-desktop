# Security Policy

DAWWW-CORE takes reports affecting the public Desktop application, project handling, authentication, billing/account surfaces, deployment, or public infrastructure seriously.

This repository is a **public product showcase**. The production source code is private, so security reports should focus on observable behavior, affected public surfaces and reproducible impact rather than requesting internal source access.

## Report a vulnerability privately

**Do not open a public GitHub Issue for a suspected vulnerability.**

Send the report to:

**contact@unicorsoundengine.com**

Use a subject such as:

`[SECURITY] DAWWW-CORE - short description`

## What to include

Provide enough information to reproduce and assess the issue safely:

- affected URL or product surface;
- date/time observed;
- browser, operating system and device when relevant;
- whether the issue affects Desktop Web, PWA, account/authentication, `.dw` import/export, local storage or another public surface;
- clear reproduction steps;
- expected behavior and actual behavior;
- security impact you believe is possible;
- screenshots, console excerpts or a minimal proof of concept when useful;
- whether you accessed or modified any data that was not your own.

Please remove passwords, access tokens, API keys, private `.dw` projects and unrelated personal information from the report.

## Responsible testing

When investigating a suspected vulnerability:

- use your own accounts and data;
- avoid service disruption, denial of service or destructive testing;
- do not attempt to access data belonging to other users;
- do not persist, publish or redistribute credentials or private data;
- stop testing if continuing would increase impact beyond what is needed to demonstrate the issue.

## Public disclosure

Please allow time for the issue to be reproduced, assessed and addressed before publishing technical details. A disclosure timeline can be discussed once the report has been acknowledged and scoped.

## Supported public surface

Reports are useful when they concern the currently deployed DAWWW-CORE public product or infrastructure. Historical builds, third-party forks, browser extensions, unrelated services and unsupported modifications may fall outside the actionable scope.

## Non-security product problems

Crashes, incorrect audio behavior, UX issues, performance problems and feature requests without a security impact should use the normal GitHub Issue forms described in [SUPPORT.md](SUPPORT.md).