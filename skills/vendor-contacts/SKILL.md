---
name: vendor-contacts
description: Keep the wedding's vendor contacts in onDimi and use them. Use when the couple mentions their caterer, venue, DJ, MC, florist, photographer, transportation or another vendor; asks who a vendor is or how to reach them; wants to add, change or remove a vendor; or wants to send a vendor something from the guest list, such as the dietary needs for the caterer.
---

# Vendor contacts

onDimi keeps one contact card per vendor: category, business name, contact
person, email, phone, website and notes. It holds contact details only, with
no prices or contracts, and it never messages vendors itself.

## Finding a vendor

Use `vendor_list` with `business_id`:
- `category` for one type: `caterer`, `venue`, `photographer`,
  `videographer`, `florist`, `dj`, `band`, `mc`, `officiant`, `cake`,
  `hair_makeup`, `attire`, `rentals`, `transportation`, `lodging`, `planner`,
  `stationery` or `other`.
- `q` to search the name, contact person, email or notes.
- `vendor_id` for one vendor.

Answer from the result. Never guess or invent a vendor's email or phone; if a
field is empty, say so.

## Adding, changing or removing a vendor

Use `vendor_manage`, and read the change back to the couple and get a yes
first.
- `action: add` needs `category`, `name` and a 10-digit US `phone`. Add the
  contact person, email, website and notes when the couple gives them.
- `action: edit` needs `vendor_id` (from `vendor_list`) and only the fields
  that change. Name, category and phone can't be cleared.
- `action: remove` needs `vendor_id`. Name the vendor you're removing and
  confirm first.

If two vendors could match ("the photographer" when there are two), ask which
one.

## Sending a vendor guest information

The common request is "send our caterer the dietary list". The same steps work
for seating notes for the venue, accessibility needs for transportation, or
song requests for the DJ.

1. Gather the guest details. `wedding_status_digest` shows how many parties
   have dietary or other needs. Use `guest_list` (all pages) and `guest_get`
   for the names and each party's notes. Separate allergies from preferences,
   and note people who asked a question (e.g. "can kosher be accommodated?").
2. Find the vendor with `vendor_list` (`category: caterer`). If there's no
   caterer, or no email, say so and offer to add it with `vendor_manage`.
3. Draft the email: To (the vendor's email and contact person), Subject, and a
   short body with the wedding name and date, the current attending count,
   the grouped list, and what you need back from them. Show it to the couple.
4. onDimi does not send vendor email. If the couple has an email connector
   such as Gmail, send it from there only after they approve the final text.
   Otherwise give them the text to copy.

Flag anything odd before it goes out, such as a guest marked as a test, or a
note that looks like a question rather than a need.
