---
description: The 'why' behind the key UX decisions
icon: square-check
---

# Design Decisions

This page documents the strategic "why" behind key UX decisions made for the Embrace Suite from 2020 onwards. Each decision explains the problem we were solving, the approach we chose, and the rationale connecting back to our Core Principles.

For implementation details and specifications, see the individual [Pattern](/broken/pages/1AI40BtbdKhOpmKy0EFh) pages. For the principles guiding these decisions, see [Core Principles](principles.md).

## Architecture

In our Suite, we've got a extremely varied set of modules for a varied set of users. We want to serve all of our users to the best of our abilities, while providing a consistent user experience.

#### Navigation split

The division between Suite-specific UI and App-specific UI (modules) is made very clear. The topbar is reserved for Suite information or actions, while the [side bar](../navigation/side-bar.md) is reserved for app-specific actions.

<figure><img src="../.gitbook/assets/afbeelding (20).png" alt=""><figcaption><p>The top bar shows Suite specific information or actions, while the side bar is reserved for the module specific information.</p></figcaption></figure>

## Multitasking

CRM operators work in inherently interruptive environments, where phone calls can arrive mid-ticket. Traditional 'complete or discard' workflows would force operators to lose their work.&#x20;

The system should adapt to human work patterns.

#### Saving incomplete work

Decision: Allow users to save incomplete work (in cache). Keeping Draft emails or Tickets open to come back to later. \
\
Also see: [Create and edit](../patterns/create-and-edit.md)

<figure><img src="../.gitbook/assets/afbeelding (13).png" alt=""><figcaption><p>Keeping the draft modal open, even after a reload, can save important unfinished work.</p></figcaption></figure>

#### After work states

Decision: Leave time for users to 'finish up'. This is done via the 'after work' states.

## Data accessibility

Frequently accessed data varies a lot per client.

Minimize clicks to access frequent data: for CRM this is contract and household information.

<figure><img src="../.gitbook/assets/afbeelding (11).png" alt=""><figcaption><p>Quick 'copy to clipboard' actions allow for fast access to relevant data.</p></figcaption></figure>

#### Pin to top

Allow for pinning of fields, to be configured by the operator. These pinned fields allow for quick access to any data type.

<figure><img src="../.gitbook/assets/afbeelding (17).png" alt=""><figcaption><p>An example interaction of 'pinning data', making sure that the important data is quickly available.</p></figcaption></figure>

## AI-strategy

Aid, but let the human make the call

#### Prefill, do not act

Prefill data where possible, and let the user make the call whether to use the prefilled data.

#### Give option to re-do AI tasks

Always allow the user to re-do any AI automations or tasks that the system supports.

## Overlays

Some key decisions have been made regarding the usage of overlays in the context panel.&#x20;

Also see: [Overlays](../patterns/overlays.md)

<figure><img src="../.gitbook/assets/afbeelding (22).png" alt=""><figcaption><p>The main three-pane structure of the Suite. An overlay is highlighted in blue.</p></figcaption></figure>

#### Single overlay at a time

When closing an overlay, all overlays are closed, unless a 'default overlay' was specified. Previously, a stacking framework was used throughout the system. The new approach is to avoid stacking, and make use of browser navigation (explained below).

<figure><img src="../.gitbook/assets/afbeelding (15).png" alt=""><figcaption><p>Avoid stacking. Stick to a simple structure.</p></figcaption></figure>

#### Browser navigation

Instead of the previously implemented stacking behavior, we try to stick to using the browser navigation as much as possible, changing the URL path whenever a new item (overlay) is opened.

This way we stay true to the browser navigation patterns that our users are used to.

<figure><img src="../.gitbook/assets/afbeelding (8).png" alt=""><figcaption><p>A base card, open by default, can show relevant contextual information.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/afbeelding (9).png" alt=""><figcaption><p>When navigating to a different context (opening an overlay), the URL path changes accordingly.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/afbeelding (10).png" alt=""><figcaption><p>When navigating to a different context (opening an overlay), the URL path changes accordingly.</p></figcaption></figure>
