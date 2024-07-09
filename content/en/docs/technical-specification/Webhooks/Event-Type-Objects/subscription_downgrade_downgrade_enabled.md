---
title: "Subscription Downgrade Enabled"
description: ""
lead: "The `Subscription.Downgrade.DowngradeEnabled` event indicates that users have requested a downgrade to a lower-tier plan. This event signifies the initiation of a downgrade process from a higher-tier plan to a lower-tier plan."
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 66
toc: true
---

> 💡 **Note:** This event signifies the initiation of a downgrade process from a higher-tier plan to a lower-tier plan.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### Event (string)

The type of event. For this event, the value is `Subscription.Downgrade.DowngradeEnabled`.

### EventCode (integer)

Unique code representing the event type. For `Subscription.Downgrade.DowngradeEnabled`, the event code is typically `10`.

### MetaData (object)

Additional dynamic metadata related to the event. This can include details such as the downgraded plan information and whether the downgrade was forced.

#### MetaData Attributes

- **downgradeEnabled (boolean):** Indicates if the downgrade is enabled.
- **downgradedPlanId (string):** The ID of the new, downgraded plan.
- **downgradedPlanPrice (decimal):** The price of the new, downgraded plan.
- **downgradedPlanCycle (string):** The billing cycle of the new, downgraded plan.
- **downgradedPlanSystemName (string):** The system name of the new, downgraded plan.
- **downgradeForced (boolean):** Indicates if the downgrade was forced.
- **Date (timestamp):** The UTC timestamp indicating when the metadata was generated.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `Subscription.Downgrade.DowngradeEnabled` event:

```json
{
  "TenantSystemName": "example_tenant",
  "Event": "Subscription.Downgrade.DowngradeEnabled",
  "MetaData": {
    "downgradeEnabled": true,
    "downgradedPlanId": "plan_12345",
    "downgradedPlanPrice": 19.99,
    "downgradedPlanCycle": "monthly",
    "downgradedPlanSystemName": "basic-plan",
    "downgradeForced": true,
    "Date": "2024-05-29T12:00:00Z"
  },
  "EventCode": 10,
  "Created": "2024-05-29T11:05:32.520057Z"
}
```
