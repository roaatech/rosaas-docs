---
title: "Subscription Downgrade  Disabled"
description: ""
lead: "The `Subscription.Downgrade.DowngradingDisabled` event indicates that the request for a downgrade has been canceled or disabled. This event occurs when the downgrade process is halted or canceled before completion.
"
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 30006
toc: true
---

> 💡 **Note:** This event occurs when the downgrade process is halted or canceled before completion.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### Event (string)

The type of event. For this event, the value is `Subscription.Downgrade.DowngradingDisabled`.

### EventCode (integer)

Unique code representing the event type. For `Subscription.Downgrade.DowngradingDisabled`, the event code is typically `17`.

### MetaData (object)

Additional dynamic metadata related to the event.

#### MetaData Attributes

- **CurrentSubscriptionPlan (string):** The current subscription plan of the tenant.
- **Date (timestamp):** The UTC timestamp indicating when the metadata was generated.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `Subscription.Downgrade.DowngradingDisabled` event:

```json
{
  "TenantSystemName": "example_tenant",
  "Event": "Subscription.Downgrade.DowngradingDisabled",
  "MetaData": {
    "CurrentSubscriptionPlan": "pro-plan",
    "Date": "2024-05-29T12:00:00Z"
  },
  "EventCode": 17,
  "Created": "2024-05-29T11:05:32.520057Z"
}
```
