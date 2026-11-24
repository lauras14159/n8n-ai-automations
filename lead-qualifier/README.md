# AI Lead Qualification Workflow

## The problem
Small sales teams lose time on weak leads and reply too late to strong ones.

## The solution
A form submission triggers a workflow that scores the lead, saves it to a Google Sheet CRM, alerts the team about Hot leads, and prepares a follow-up draft.

## How it works
Form → AI scoring → spam filter → follow-up draft → save to sheet → Discord alert (Hot only) + Gmail draft

1. **Form trigger** collects name, email, company, need, budget, and timeline.
2. **AI scoring** returns a score (Hot, Warm, Cold), a reason, a summary, and a spam flag in a fixed format.
3. **Spam filter** stops spam before anything else runs.
4. **Follow-up draft** is written by a second AI step, tailored to the score.
5. **Google Sheet** stores every lead as the CRM.
6. **Discord alert** fires only for Hot leads.
7. **Gmail draft** is created for every real lead, for human review.

## Key decisions
- **A chain, not an agent.** The steps are always the same, so a fixed chain is cheaper, faster, and more predictable.
- **AI judges, normal nodes act.** The AI only produces a score. A plain IF node decides who gets alerted, which is more reliable.
- **Spam gate at the start.** Spam never reaches the second AI call, the sheet, or the inbox.
- **Drafts, not auto-send.** A person reviews every reply.
- **Two separate AI steps.** Scoring needs consistency (low temperature), writing needs a natural tone.

## Tools
n8n, Google Gemini, Google Sheets, Gmail, Discord
