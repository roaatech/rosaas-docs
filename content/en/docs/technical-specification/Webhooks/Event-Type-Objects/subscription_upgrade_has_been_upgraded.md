---
title: "Subscription Has Been Upgraded"
description: ""
lead: "The `Subscription.Upgrade.HasBeenUpgraded` event indicates that a subscription has been successfully upgraded. This event occurs when the upgrade process from a lower-tier plan to a higher-tier plan is completed successfully."
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 30005
toc: true
---

> 💡 **Note:** This event occurs when the upgrade process from a lower-tier plan to a higher-tier plan is completed successfully.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### Event (string)

The type of event. For this event, the value is `Subscription.Upgrade.HasBeenUpgraded`.

### EventCode (integer)

Unique code representing the event type. For `Subscription.Upgrade.HasBeenUpgraded`, the event code is typically `8`.

### MetaData (object)

Additional dynamic metadata related to the event. This can include details such as the subscription expiration date and the new subscription plan.

#### MetaData Attributes

- **SubscriptionExpirationDate (timestamp):** The expiration date of the upgraded subscription.
- **SubscriptionNewPlan (string):** The display name of the new subscription plan.
- **Date (timestamp):** The UTC timestamp indicating when the metadata was generated.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `Subscription.Upgrade.HasBeenUpgraded` event:

```json
{
  "TenantSystemName": "example_tenant",
  "Event": "Subscription.Upgrade.HasBeenUpgraded",
  "MetaData": {
    "SubscriptionExpirationDate": "2025-05-01T08:30:00Z",
    "SubscriptionNewPlan": "Premium Plan",
    "Date": "2024-05-29T12:00:00Z"
  },
  "EventCode": 8,
  "Created": "2024-05-29T11:05:32.520057Z"
}
```
