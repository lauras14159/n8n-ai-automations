# AI Customer Support Agent

## Problem
Customers ask the same questions repeatedly, and slow replies lose sales.

## What it does
- Chat trigger receives customer messages
- AI agent answers only from a Google Sheet FAQ (looked up as a tool)
- Remembers the conversation (window memory)
- Escalates to a human via Discord when unsure, upset, or asked for a person
- Logs every conversation to Google Sheets

## Safeguards
- Answers only from the FAQ, never invents prices or policies
- Asks for contact details before escalating
- Doesn't claim it escalated if the tool failed

## Tools
n8n, Gemini, Google Sheets, Discord
