---
title: "Subscription Forced Downgrade Enabled"
description: ""
lead: "The `Subscription.Downgrade.ForcedDowngradeEnabled` event indicates that a forced downgrade has been enabled. This event occurs when a downgrade is forcefully initiated or enabled."
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 30007
toc: true
---

> 💡 **Note:** This event occurs when a downgrade is forcefully initiated or enabled.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### Event (string)

The type of event. For this event, the value is `Subscription.Downgrade.ForcedDowngradeEnabled`.

### EventCode (integer)

Unique code representing the event type. For `Subscription.Downgrade.ForcedDowngradeEnabled`, the event code is typically `11`.

### MetaData (object)

Additional dynamic metadata related to the event.

#### MetaData Attributes

- **downgradeEnabled (boolean):** Indicates if the downgrade is enabled.
- **forcedDowngradedPlanPrice (decimal):** The price of the new, downgraded plan.
- **forcedDowngradedPlanCycle (string):** The billing cycle of the new, downgraded plan.
- **forcedDowngradedPlanSystemName (string):** The system name of the new, downgraded plan.
- **downgradeForced (boolean):** Indicates if the downgrade was forced.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `Subscription.Downgrade.ForcedDowngradeEnabled` event:

```json
{
  "TenantSystemName": "example_tenant",
  "Event": "Subscription.Downgrade.ForcedDowngradeEnabled",
  "MetaData": {
    "downgradeEnabled": true,
    "forcedDowngradedPlanPrice": 19.99,
    "forcedDowngradedPlanCycle": "monthly",
    "forcedDowngradedPlanSystemName": "basic-plan",
    "downgradeForced": true
  },
  "EventCode": 11,
  "Created": "2024-05-29T11:05:32.520057Z"
}
```
