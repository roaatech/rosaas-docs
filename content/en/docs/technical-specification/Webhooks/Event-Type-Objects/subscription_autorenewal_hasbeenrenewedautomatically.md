---
title: "Subscription Has Been Renewed Automatically"
description: ""
lead: "The `Subscription.AutoRenewal.HasBeenRenewedAutomatically` event indicates that a subscription has been automatically renewed. This event occurs when a subscription is renewed automatically at the end of each billing cycle"
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 69
toc: true
---

> 💡 **Note:** This event signifies the automatic renewal of a subscription.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### Event (string)

The type of event. For this event, the value is `Subscription.AutoRenewal.HasBeenRenewedAutomatically`.

### EventCode (integer)

Unique code representing the event type. For `Subscription.AutoRenewal.HasBeenRenewedAutomatically`, the event code is `7`.

### MetaData (object)

Additional dynamic metadata related to the event.

#### MetaData Attributes

- **SubscriptionExpirationDate (timestamp):** The expiration date of the renewed subscription.
- **SubscriptionNewPlan (string):** The display name of the new subscription plan.
- **Date (timestamp):** The UTC timestamp indicating when the metadata was generated.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `Subscription.AutoRenewal.HasBeenRenewedAutomatically` event:

```json
{
  "TenantSystemName": "example_tenant",
  "Event": "Subscription.AutoRenewal.HasBeenRenewedAutomatically",
  "MetaData": {
    "SubscriptionExpirationDate": "2025-06-01T08:30:00Z",
    "SubscriptionNewPlan": "Premium Plan",
    "Date": "2024-06-02T12:00:00Z"
  },
  "EventCode": 7,
  "Created": "2024-06-02T12:00:00Z"
}
```
