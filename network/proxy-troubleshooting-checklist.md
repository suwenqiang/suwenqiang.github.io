---
layout: page
title: "Proxy Troubleshooting Checklist"
permalink: /network/proxy-troubleshooting-checklist/
---

## Symptom

Downloads, API requests, or Git operations fail only in specific environments, often with timeout, TLS, or DNS errors.

## Quick Checks

1. Check environment variables:
   - `env | rg 'proxy|PROXY'`
2. Confirm direct connectivity without proxy if possible.
3. Verify whether the tool uses HTTP proxy, HTTPS proxy, or SOCKS proxy.
4. Confirm certificate trust requirements in managed networks.
5. Test with `curl -I` or a minimal API request before debugging the full toolchain.

## Verification

- `curl -I https://example.com`
- `git config --get-regexp 'proxy'`
- tool-specific proxy settings
