---
title: "Subscription Auto-Renewal Disabled"
description: ""
lead: "The `Subscription.AutoRenewal.AutoRenewalDisabled` event indicates that auto-renewal for a subscription is disabled."
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 74
toc: true
---

> 💡 **Note:** Subscriptions will not automatically renew at the end of each billing cycle when this feature is disabled.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### Event (string)

The type of event. For this event, the value is `Subscription.AutoRenewal.Disabled`.

### EventCode (integer)

Unique code representing the event type. For `Subscription.AutoRenewal.Disabled`, the event code is `15`.

### MetaData (object)

Additional dynamic metadata related to the event.

#### MetaData Attributes

- **CurrentSubscriptionPlan (string):** The system name of the current subscription plan.
- **CancellationTime (timestamp):** The UTC timestamp indicating when auto-renewal was disabled.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `Subscription.AutoRenewal.Disabled` event:

```json
{
  "TenantSystemName": "example_tenant",
  "Event": "Subscription.AutoRenewal.Disabled",
  "MetaData": {
    "CurrentSubscriptionPlan": "example_plan",
    "CancellationTime": "2024-06-04T10:00:00Z"
  },
  "EventCode": 15,
  "Created": "2024-06-04T10:00:00Z"
}
```
