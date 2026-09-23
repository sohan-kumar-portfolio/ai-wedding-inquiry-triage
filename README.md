# AI Inquiry Triage System

## Problem
Manual lead triage is slow and inconsistent — wedding vendor inquiries
sit unanswered for hours, and urgent requests get the same treatment
as casual ones.

## Solution
An automated pipeline that reads every inquiry, classifies urgency
and category, logs it to a CRM, and sends a personalized reply —
all within seconds of submission.

## Architecture
[Google Form] → [Google Sheets] → [Make.com]
                                      ├─ Gemini AI (extract urgency/category/reply)
                                      ├─ HubSpot (create contact + deal)
                                      └─ Gmail (auto-reply + urgent alert)

## Tools
Google Forms, Google Sheets, Make.com, Google Gemini API, HubSpot CRM, Gmail

## What it does
1. Client submits an inquiry via form
2. Gemini analyzes the message: urgency (high/med/low), category, drafts a reply
3. Contact + deal auto-created in HubSpot, tagged with AI classifications
4. Personalized reply sent instantly; urgent cases trigger an internal alert

## Impact
Cuts response time from hours to under a minute. No lead is
untracked — every inquiry becomes a CRM record automatically.

## Next steps
- Branch alerting so only high-urgency cases ping the team (currently all do)
- Deal-to-contact association (blocked by free-tier HubSpot scope limits)
