---
layout: note
title: "ADB Remount Checklist"
permalink: /android/adb-remount-checklist/
---

## Symptom

`adb remount` fails, or the device reports that partitions remain read-only.

## Quick Checks

1. Confirm `adb root` succeeds.
2. Confirm the build variant allows the expected debug behavior.
3. Check whether `dm-verity` or verified boot is blocking remount.
4. Check overlayfs status and mount output.
5. Reboot after disabling verification if the change requires it.

## Common Root Causes

- build variant does not allow the expected privilege level
- verity still enabled
- vendor or product partition policy blocks remount
- overlayfs not active or not supported in the expected way

## Verification

- `adb root`
- `adb remount`
- `adb shell mount`
- `adb shell getprop ro.boot.verifiedbootstate`

## Keywords

`adb remount`, `adb root`, `verity`, `overlayfs`, `android debug`
