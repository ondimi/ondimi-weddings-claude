---
name: getting-started
description: First steps with onDimi. Use when the couple has just connected onDimi, asks what onDimi can do, says they are new, or when their wedding has no guests or details yet.
---

# Getting started with onDimi

onDimi runs an AI guest concierge for one wedding. It texts, emails, calls and
chats with each guest party to collect RSVPs, mailing addresses and other
details, answers guest questions from the wedding's information, and sends the
updates the couple approves. You help the couple steer it.

## First conversation

1. Call `wedding_profile` (no arguments). It returns the `business_id` every
   other tool needs, the wedding name, date and days to go. Use that id for
   the rest of the conversation; never guess one.
2. Call `wedding_status_digest` to see where things stand: guest count, RSVP
   tally, missing addresses, plans running, recent updates.
3. Greet the couple by the wedding name and summarize in two or three
   sentences. Then offer the most useful next step:
   - **No guests yet:** offer to import their guest list (the
     `import-guest-list` skill). A pasted spreadsheet or website export works.
   - **Guests but no RSVP campaign:** offer to start collecting RSVPs (the
     `rsvp-campaign` skill).
   - **No wedding date or milestones:** offer to set their timeline
     (`wedding_details`, then `concierge_guide` topic `wedding-milestones`).
   - **No venue or logistics in the knowledge:** offer to add them (the
     `guest-questions` skill) so the concierge can answer guests.

## What to tell a couple who asks "what can you do?"

Keep it short and concrete:
- Import and tidy the guest list.
- Collect RSVPs and mailing addresses by text, email, phone and chat, with
  automatic follow-ups.
- Answer guests' questions about the wedding.
- Send one update to many guests (a time change, shuttle details), after the
  couple approves the wording and the audience.
- Report exact numbers any time: who's coming, who declined, who hasn't
  answered.

## Rules that always apply

- Nothing reaches a guest without the couple's explicit approval of who gets
  it and what it says.
- Some outreach channels depend on the wedding's onDimi plan. If a tool says
  the plan doesn't include something, tell the couple plainly and share the
  link the tool returns; don't work around it.
- Use onDimi's words: "guest parties" (one invitation, possibly several
  people), "the concierge", "updates".
- For detail on any workflow, `concierge_guide` has reference pages; call it
  with no topic to list them.
