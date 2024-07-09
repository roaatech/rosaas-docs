---
title: "Subscription Suspended Due To Unpaid"
description: ""
lead: "The `Subscription.SuspendedDueToUnpaid` event indicates that a subscription has been suspended due to unpaid charges."
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 73
toc: true
---

> 💡 **Note:** This event occurs when a subscription is suspended because payment for charges associated with the subscription has not been received.

## Event Attributes

### MetaData (object)

Additional dynamic metadata related to the event.

#### MetaData Attributes

- **Date (timestamp):** The UTC timestamp indicating when the subscription was suspended.
- **Plan (string):** The system name of the subscription plan.
- **PlanPrice (decimal):** The price of the subscription plan.
- **PlanCycle (string):** The billing cycle of the subscription plan.

## Example

Here is an example JSON representation of the `Subscription.SuspendedDueToUnpaid` event:

```json
{
  "MetaData": {
    "Date": "2024-06-04T10:00:00Z",
    "Plan": "example_plan",
    "PlanPrice": 49.99,
    "PlanCycle": "monthly"
  }
}
```
