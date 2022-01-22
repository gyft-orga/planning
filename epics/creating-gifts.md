As a visitor, I want to see what gifts the profile owner wants.

---

As a profile owner, I want to add gifts to my profile.

Dev Notes:
Gift:
  - name: String
  - [image]: binary | link_to_image
  - [link]: String (http link - validate)
  - [description]: String
  - [priority]:
      categories: "Must Have", "Should Have", "Could Have"
      categories (human names): "Must Have", "I'd like", "Maybe", ("Fun")
  - readonly lastEdit/createDate

Links in the description should be clickable

---

