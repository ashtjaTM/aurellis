---
title: "Sign In"
parent: "Application"
summary: "Provides the Aurellis sign-in screen with email and password fields and a sign-in action."
tags: ["authentication", "account"]
related:
  - file: "Sign Up"
    type: related_to
sources: ["exploration"]
version: 17
confidence: high
has_open_conflicts: false
updated_at: "2026-11-18T08:31:37.423Z"
---

## Sub-features
- Email and password sign-in

## Business Rules
- The /auth/sign-in screen presents a sign-in form with fields labelled “EMAIL” and “PASSWORD” and a “SIGN IN” button.
- The sign-in form requires the EMAIL field, which is an email input.
- The sign-in form requires the PASSWORD field, which is a password input.
- On the Sign In page, submitting with both fields empty leaves the page and its visible text unchanged; no application validation message appears in the inspected page text.
- The Email and Password fields are required on the sign-in form. If Password is blank when Sign in is submitted, browser required-field validation blocks submission and displays “Please fill in this field.”
- On /auth/sign-in, submitting the form with Email and Password empty is blocked by required-field validation; the browser reports “Please fill in this field.”
- On /auth/sign-up, the Create account form requires the Name field, which is a text input.
- On /auth/sign-up, the Create account form requires the Email field, which is an email input.
- On /auth/sign-up, the Create account form requires the Password field, which is a password input with a minimum length of 8 characters.
- On /auth/forgot-password, the form submitted by "Send reset link" has one field labeled "Email"; it is a required email input. No minlength, maxlength, or pattern constraint was observed.

## Terminology
- EMAIL
- PASSWORD
- SIGN IN

## Unexplored / Unknown
- form "Sign in" on /auth/sign-in: rejection (type) - no evidence of validation after 2 attempts - last error: The page could not be inspected: getByText('SIGN IN') matches 2 elements on the page: add #1 to #2 to the step's target for one of them (#1 is the first), or narrow it with "in <target>".
- form "Send reset link" on /auth/forgot-password: rejection (empty) - needs a sandbox or a person: it would change data in a protected environment
- form "Send reset link" on /auth/forgot-password: rejection (required) - needs a sandbox or a person: it would change data in a protected environment
- form "Send reset link" on /auth/forgot-password: rejection (type) - needs a sandbox or a person: it would change data in a protected environment
- Unknown: Exact validation text shown after submitting an email value of the wrong format is not recorded; the sign-in page's baseline snapshot did not expose a rejection message.
- Unknown: The forgot-password screen at /auth/forgot-password is present, but its visible controls and recovery behavior are not yet documented.

## Changelog
- v17 (2026-11-18): Regenerated from typed knowledge items (10 observed, 2 unknown). [sources: exploration]
- v16 (2026-11-18): Regenerated from typed knowledge items (10 observed, 2 unknown). [sources: exploration]
- v15 (2026-11-18): Regenerated from typed knowledge items (9 observed, 2 unknown). [sources: exploration]
- v14 (2026-11-18): Regenerated from typed knowledge items (6 observed, 2 unknown). [sources: exploration]
- v13 (2026-11-18): Regenerated from typed knowledge items (6 observed, 2 unknown). [sources: exploration]
- v12 (2026-11-18): Regenerated from typed knowledge items (6 observed, 1 unknown). [sources: exploration]
- v11 (2026-11-18): Regenerated from typed knowledge items (6 observed, 1 unknown). [sources: exploration]
- v10 (2026-11-18): Regenerated from typed knowledge items (6 observed, 1 unknown). [sources: exploration]
- v9 (2026-11-18): Regenerated from typed knowledge items (5 observed, 1 unknown). [sources: exploration]
- v8 (2026-11-18): Regenerated from typed knowledge items (5 observed, 1 unknown). [sources: exploration]
- v7 (2026-11-18): Regenerated from typed knowledge items (5 observed). [sources: exploration]
- v6 (2026-11-18): Regenerated from typed knowledge items (4 observed). [sources: exploration]
- v5 (2026-11-18): Regenerated from typed knowledge items (3 observed). [sources: exploration]
- v4 (2026-11-18): Regenerated from typed knowledge items (3 observed). [sources: exploration]
- v3 (2026-11-18): Regenerated from typed knowledge items (3 observed). [sources: exploration]
- v2 (2026-11-18): Regenerated from typed knowledge items (1 observed). [sources: exploration]
- v1 (2026-11-18): Regenerated from typed knowledge items (1 observed). [sources: exploration]
