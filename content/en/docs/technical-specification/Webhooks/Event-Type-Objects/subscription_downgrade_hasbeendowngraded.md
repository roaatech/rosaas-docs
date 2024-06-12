---
title: "Subscription Has Been Downgraded"
description: ""
lead: "The `Subscription.Downgrade.HasBeenDowngraded` event indicates that a subscription has been successfully downgraded. This event occurs when the downgrade process from a higher-tier plan to a lower-tier plan is completed successfully.
"
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 30010
toc: true
---

> 💡 **Note:** This event signifies the successful completion of a downgrade process.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### Event (string)

The type of event. For this event, the value is `Subscription.Downgrade.HasBeenDowngraded`.

### EventCode (integer)

Unique code representing the event type. For `Subscription.Downgrade.HasBeenDowngraded`, the event code is `12`.

### MetaData (object)

Additional dynamic metadata related to the event.

#### MetaData Attributes

- **SubscriptionExpirationDate (timestamp):** The expiration date of the downgraded subscription.
- **SubscriptionNewPlan (string):** The display name of the new, downgraded subscription plan.
- **Date (timestamp):** The UTC timestamp indicating when the metadata was generated.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `Subscription.Downgrade.HasBeenDowngraded` event:

```json
{
  "TenantSystemName": "example_tenant",
  "Event": "Subscription.Downgrade.HasBeenDowngraded",
  "MetaData": {
    "SubscriptionExpirationDate": "2025-06-01T08:30:00Z",
    "SubscriptionNewPlan": "Basic Plan",
    "Date": "2024-06-02T12:00:00Z"
  },
  "EventCode": 12,
  "Created": "2024-06-02T12:00:00Z"
}
```
