# onDimi Weddings for Claude

Manage your wedding guest list by talking to Claude, and keep your guests
informed. You sign in to your own onDimi wedding; Claude sees that wedding and
nothing else.

## Who onDimi contacts, and how

- **Only your guests.** onDimi contacts only the guests you added to your
  wedding's guest list. No tool takes a phone number or an email address to
  contact, so nobody outside your guest list can be reached.
- **Only with consent.** Each guest is reached only on the channels that
  guest consented to: text, email or phone call. A guest can opt out at any
  time (reply STOP) and onDimi stops.
- **Only what you approve.** You choose the guests and approve the wording
  before anything goes out.
- **Why guests hear from onDimi:** to give their RSVP, to give their mailing
  address, to get an answer to a question about the wedding, or to receive an
  update from you (a new ceremony time, the shuttle schedule).
- **Reminders, one guest at a time.** When you ask a guest for an RSVP or an
  address, onDimi follows your wedding's reminder plan for that guest: a few
  reminders at set times by text, email or, if the guest consented to calls,
  a phone call. The reminders stop as soon as that guest answers.
- **Calls say who is calling.** Every call opens with "it's onDimi, the AI
  guest concierge of <the couple>".
- **US guests only.**

## What you can ask

- "Here's our guest list" (paste a spreadsheet or an export) — Claude imports
  it, shows you what was added, and offers to start collecting RSVPs.
- "How are RSVPs looking?" or "Who declined?" — exact counts and names.
- "Who still needs to send their address?" — and, once you agree, a
  reminder to those guests.
- "Tell everyone attending the ceremony moved to 4:30" — Claude drafts the
  update, shows you a sample, and sends it only after you approve.
- "Add the shuttle schedule so guests can ask about it" — the concierge
  answers guests from that information from then on.
- "List the dietary needs and draft an email to our caterer" — Claude pulls
  the needs from your guest list and the caterer's contact from your saved
  vendors, and drafts the email for you to send.

## Getting started

1. Add the plugin, then connect **onDimi** from the plugin's Connectors tab.
2. Sign in with your onDimi wedding account, or create one in the same window.
   Creating an account doesn't contact any guests.
3. Ask Claude "Let's set up our wedding." Claude fills in your wedding and
   account details and the information guests will ask about (venue, times,
   hotels, FAQ). These are needed before onDimi contacts any guest; you can
   also fill them in on your onDimi dashboard.

## What's included

- **Connector:** `https://api.ondimi.com/couples/mcp`, the onDimi wedding
  tools (guest list, RSVPs, reminder plans, updates, wedding details,
  knowledge and vendors).
- **Skills:** getting started (wedding setup first), importing a guest list,
  RSVP and address follow-up, sending a guest update, the daily status check, keeping the concierge's
  knowledge current, looking up guests with exact counts, and vendor contacts.
- **Commands:** `/ondimi-weddings:setup`, `/ondimi-weddings:status`, `/ondimi-weddings:rsvps`,
  `/ondimi-weddings:send-update`.

## Data and privacy

The plugin itself stores nothing and runs no code on your computer; it is
instructions plus a connector entry. When you use the connector, Claude sends
your requests to onDimi at `api.ondimi.com` over HTTPS, signed in as you, and
onDimi returns your own wedding's data: guest names, contact details,
addresses, RSVP answers, guest notes and message history. A connection can
see only your wedding. Messages reach only your own guests, and only after
you approve them.

Disconnect any time from Claude's connector settings; changing your onDimi
password also disconnects every assistant. onDimi's
[Privacy Policy](https://weddings.ondimi.com/privacy-policy) and
[Terms](https://weddings.ondimi.com/terms-and-conditions) apply.

## Support

Email [support@ondimi.com](mailto:support@ondimi.com) or visit
[weddings.ondimi.com/contact](https://weddings.ondimi.com/contact).
