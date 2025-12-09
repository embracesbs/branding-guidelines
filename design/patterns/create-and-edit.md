---
description: All create and edit actions happen in centered and minimizable modals
icon: circle-plus
---

# Create and edit

### The problem

Create and edit actions (forms) are scattered in different places throughout the Suite. Often, they appear in overlays in the context panel, which created a critical usability issue:

Users needed access to information that lived in the context panel to complete actions that were also in the context panel.

Example scenario:

* User starts filling out a ticket form in the context panel
* User realises they need info from a contract to complete the form
* User opens the contract overlay
* The contract overlay covers the form they were working on, all changes are lost

This showed task abandonment, workarounds with external tools (note-taking in Word) and potential errors from misremembered information. In any case, frustration.

### The decision

**All create and edit actions happen in centered and minimizable modals.**

<figure><img src="../.gitbook/assets/afbeelding (24).png" alt=""><figcaption><p>An example of a focused, centered modal.</p></figcaption></figure>

#### **Centered modal**

* Dims background
* Centered, focused

#### Background remains accessible

* Panels stay visible
* Information stays accessible

#### Minimizable

* Clicking outside the modal minimizes the modal
* Return to the form with all progress still intact



## Principles

### Keep it simple

* Clear separation, viewing
