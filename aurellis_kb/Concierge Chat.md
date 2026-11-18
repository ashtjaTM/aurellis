---
title: "Concierge Chat"
parent: "Application"
summary: "The home-page chat widget lets visitors interact with the Aurellis Concierge and can be opened or closed from chat controls."
tags: ["chat", "concierge", "support"]
related:
  - file: "Home & Featured Collections"
    type: related_to
sources: ["exploration"]
version: 2
confidence: high
has_open_conflicts: false
updated_at: "2026-11-18T07:28:13.244Z"
---

## Sub-features
- Chat panel

## Business Rules
- On the home page, selecting the "Open chat" button opens the chat panel, which shows the title "Aurellis Concierge", the subtitle "Answers about products, orders & more", the introductory message "Hi — I'm the Aurellis Concierge. Ask me anything about products, orders, shipping, or your account, or pick a topic below.", a textbox labeled "Ask a question…", and buttons labeled "Start new chat" and "Send message"; both buttons are disabled in this observed state.
- Selecting the chat panel's "Close chat" button closes the chat panel and returns the home page to the state with the "Open chat" button.

## Terminology
- Aurellis Concierge

## Unexplored / Unknown
- Seen only in code, not checked in the running application: Opening the chat panel issues GET /api/chat/topics, which returned HTTP 200 with an empty $.topics array in the observed session.

## Changelog
- v2 (2026-11-18): Regenerated from typed knowledge items (3 observed). [sources: exploration]
- v1 (2026-11-18): Regenerated from typed knowledge items.
