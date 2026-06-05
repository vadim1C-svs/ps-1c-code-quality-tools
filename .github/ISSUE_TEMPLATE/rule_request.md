# Rule Request

## Problem

Describe the 1C code quality problem.

## Example of bad code

```bsl
Expected recommendation

Describe how the code should be improved.

Severity
 Low
 Medium
 High
 Critical
Configuration context
 1C:Accounting for Kazakhstan
 1C:Trade Management
 1C:Retail
 1C:UNF
 Other

---

# 7. `SECURITY.md`

Так как в форме OpenAI есть интерес к Codex Security, добавь файл:

```text
SECURITY.md

Содержимое:

# Security Policy

## Supported versions

This repository contains documentation, examples, prompts, and code quality rules for 1C:Enterprise projects.

## Reporting a vulnerability

If you find a security issue in examples, prompts, or checklists, please create a GitHub issue or contact the maintainer.

## Security focus areas

This project pays attention to:

- Hardcoded tokens and passwords
- Sensitive data in logs
- Incorrect access rights checks
- Unsafe external integrations
- Unvalidated external input
- Confidential client data in source code
- Unsafe file operations
- Unsafe exchange mechanisms

## Confidential data

Do not submit real client data, real tokens, real passwords, production database fragments, or proprietary configuration code.