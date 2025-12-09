---
description: >-
  The panels that can be opened in a contextual situation (right-side) we call
  'overlays'.
icon: browser
---

# Overlays

In the Suite, several entities are available (see [Entities](../data/entities.md)). Per each entity, a specific set of information is available to display. The display of this data is often contextual information, shown in the right side (see [Panels](panels.md)). The right-side panels that can be closed, we call 'overlays'.

## The problem

Our previous overlay system allowed stacking overlays on top of each other, without allowing the user to track back their steps. This created serious issues:

* User confusion (users lost track of what was open)
* Navigation failure (difficult to figure out how to track back)
* Lost progress (opening another overlay while working on a ticket, would lose all progress)
* Task abandonment (high complexity led to users giving up)

## The decision

**Simplify radically.** A simple layout, simple interaction and simple navigation.

**Primary content stays undisturbed.** Users should maintain focus on their main content, while aiding themselves to secondary information.

<figure><img src="../.gitbook/assets/afbeelding (22).png" alt=""><figcaption><p>The main three-pane structure of the Suite. An overlay is highlighted in blue.</p></figcaption></figure>

### Single overlay at a time

* Opening a new overlay replaces the current one
* No stacking WITHOUT changing the URL
* Can't get lost in nested layers

### Browser navigation

* Back button returns to previous state
* Forward button reopens overlay (after going back)
* Familiar interaction
* Enables tracking back through the users path

#### URL reflects overlay state

The URL always reflects the overlay state, as shown in the table below:

| URL                          | Context pane                    |
| ---------------------------- | ------------------------------- |
| /chat/123123/                | Initial overlay (relation card) |
| /chat/123123/contract/456456 | Unit overlay                    |
| /chat/123133/ticket/789789   | Ticket overlay                  |

## Structure

### Header

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

#### Visual

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Each overlay refers to an entity. Each entity has its own visual identity which makes it easy for users to recognize the entity type. More about this in [Entities](../data/entities.md).

#### Title and CTA

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

The title of the entity is displayed. If available, the main CTA of the entity is displayed in the header.&#x20;

**Interactions**

* By clicking on the title of the overlay, the user can navigate to the entity in a standalone view.

#### Close

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

On the top-right side (common pattern), the overlay can be closed.

**Interactions**

* Close the overlay

#### Tabs

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

The tab group is the main navigation for the content of the overlay.&#x20;

Default active tab is 'Details', unless a conversation is available (Chat, E-mail).

## Principles

### Intuitive for beginners

* Browser navigation is universally understood
* Can't get lost
* Back button does as is expected

### Powerful for experts

* Fast overlay switching
* Shortcuts (Escape, back/forward)
* URL is bookmarkable
