As a interested visitor, I want to sign up, to access services only available to
users.

Dev Notes:
- data to be provided at signup:
  - required:
    - email
    - phone nr
    - birthday
  - optional:
    - username (generated otherwise, compare: github repo name generator)
    - password (MVP: required)
- verify phone number via sms (what are the costs?)
- ? verify email? -> is there potential for abuse?

---

As a registered user, I want to sign in.

---

As a registered user, I want to sign in using my password.

Acceptance:
- user has set a password
  - at sign up
  - or added later on

---

As a registered user, I want to sign in by receiving an OTP via email.

Description:
This is not MVP

Acceptance:
- user has not set a password
  - at sign up
  - or deleted it afterward

---

