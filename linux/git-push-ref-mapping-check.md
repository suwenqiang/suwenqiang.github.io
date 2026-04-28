layout: note
title: "Git Push Ref Mapping Check"
permalink: /linux/git-push-ref-mapping-check/
---

## Symptom

`git push` succeeds, but the branch lands in an unexpected remote ref such as `refs/for/main`.

## Checkpoints

1. Inspect local repo config:
   - `git config --get-regexp '^(remote\\.|push\\.|branch\\.)'`
2. Inspect global config:
   - `git config --global --get-regexp '^(remote\\.|push\\.)'`
3. Verify the exact push target:
   - `git push origin HEAD:refs/heads/main`

## Root Cause Pattern

An explicit `remote.origin.push` rule overrides the normal branch push behavior.

## Fix

- remove the unexpected push rule in the affected repo
- set the upstream branch again if needed

## Verification

- `git remote -v`
- `git branch -vv`
- `git push origin HEAD:refs/heads/main`
