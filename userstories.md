As a visitor, I want to see what gifts the profile owner wants.

---

As a visitor, I want to see what gifts the profile owner wants for a user-specified event.

Acceptance:
- users can create events

Dev Notes:
Event:
  - date: Date
  - name: String
  - [description]: String

---

As a visitor, I want to see what gifts the profile owner wants for their birthday.

Acceptance:
- system somehow got ahold of the birthday
- created the birthday event automatically

---

As a visitor, I want to see what gifts the profile owner wants for Christmas.

Acceptance:
- created the Christmas event automatically

---

As a profile owner, I want to CRUD events.

Acceptance:
- after the date of an event (+7 leave some leeway for ppl) has passed the
profile owner can check who claimed what gifts

---

As a profile owner, I want to allocate gifts to events.

Acceptance:
- gifts don't need to have an event associated with them

---

As a profile owner, I want to be notified that I should update my gift list for
an upcoming event.

Acceptance:
- notifications can be toggled for different events individually
- or for all at once

---

As a visitor, I will see that other users have marked a number of gifts as
something they will be getting for the profile owner.

Acceptance:
- the profile owner shall not even see the anonymous info

---

As a user, I will see the users who have marked what gifts as something they
will be getting for the profile owner.

Acceptance:
- user is not profile owner

---

As a user, I want to mark gift as something I'm getting, as to communicate to
other profile visitors that the given gift is "taken".

Acceptance:
- warning if gift already taken by other user

---

As a profile owner, I can report spam/abuse "takings" to flag people you don't
know (and from whom you did not get the marked gift.)

Acceptance:
- account suspension after two reports, open to manual appeal (mailto: admins)

---

As a profile owner, I want to add gifts to my profile.

Dev Notes:
Gift:
  - [name]: String
  - [image]: binary | link_to_image
  - [link]: String (http link - validate)
  - [description]: String
  - [priority]: ? Freitext oder Nummer ?

Links in the description should be clickable

---

As a profile onwer, I want to import gifts from my Amazon wishlist.

Acceptance:
- wishlists need to be public/have read-access link

Dev Notes:
- scrape page, taking name, image, ama-link, ?description? (prob not very useful)

---

As the site owner, I want to insert my affiliate marketing link into the
outgoing urls.

Dev Notes:
- scrub links
- write them to db

- read link from db
- insert affiliate marketing id into link
- answer frontend request

---

As the site owner, I want to have an XMR wallet for donations in the footer.

---

As a visitor, I want to click the icons for popular market-places to look up the
gift there.

Acceptance:
- gift has a name
- gift does not have a link of its own
- user goes to their regional variant (amazon.de, amazon.co.uk)
- link has affiliate marketing id

Dev Notes:
- Put product name into query: https://smile.amazon.de/s?k=%s
- the icons are the favicon of the websites
  - domain/favicon.ico
  - https://stackoverflow.com/questions/10282939/how-to-get-favicons-url-from-a-generic-webpage-in-javascript
  - https://stackoverflow.com/questions/1990475/how-can-i-retrieve-the-favicon-of-a-website-with-xslt-or-jsp (dont use the google link)

---

As a visitor, I can find a users profile by putting in their phone number.

Acceptance:
- phone number is not accesible anywhere on the profile

Dev Notes:
- function in the backend: getProfileIdFromPhoneNumber(phone_number) = profile_id

---

TODO: convert into user stories:
Signup:
1. (preferred and should be emphasized as such): requires:
- phone number
- email (2fa, notifications)
optional:
- username (generated otherwise, but changable)
- password (you could just not have this to make it easier onyourself)
2. requires:
- username
- email (2fa, notifications)
optional:
- phone number (another prompt for it)
