---
title: "Subscription AutoRenewal Enabled"
description: ""
lead: "The `Subscription.AutoRenewal.Enabled` event indicates that auto-renewal for a subscription is enabled. Subscriptions will automatically renew at the end of each billing cycle when this feature is enabled.
"
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 65
toc: true
---

> 💡 **Note:** Subscriptions will automatically renew at the end of each billing cycle when this feature is enabled.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### Event (string)

The type of event. For this event, the value is `Subscription.AutoRenewal.Enabled`.

### EventCode (integer)

Unique code representing the event type. For `Subscription.AutoRenewal.Enabled`, the event code is typically `14`.

### MetaData (object)

Additional dynamic metadata related to the event. This can include details such as the number of renewals and the renewal cycle.

#### MetaData Attributes

- **autoRenewalEnabled (boolean):** Indicates if auto-renewal is enabled.
- **renewalsCount (integer):** The number of times the subscription has been renewed.
- **isContinuousRenewal (boolean):** Indicates if the subscription renews continuously.
- **renewalCycle (string):** The billing cycle for the renewal.
- **Date (timestamp):** The UTC timestamp indicating when the metadata was generated.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `Subscription.AutoRenewal.Enabled` event:

```json
{
  "TenantSystemName": "example_tenant",
  "Event": "Subscription.AutoRenewal.Enabled",
  "MetaData": {
    "autoRenewalEnabled": true,
    "renewalsCount": 3,
    "isContinuousRenewal": true,
    "renewalCycle": "monthly",
    "Date": "2024-05-29T12:00:00Z"
  },
  "EventCode": 14,
  "Created": "2024-05-29T11:05:32.520057Z"
}
```
