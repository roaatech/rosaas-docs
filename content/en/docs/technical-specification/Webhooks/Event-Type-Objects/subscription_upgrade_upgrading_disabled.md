---
title: " Subscription Upgrade Disabled"
description: ""
lead: "The `Subscription.Upgrade.UpgradingDisabled` event indicates that the request for an upgrade has been canceled or disabled. This event occurs when the upgrade process is halted or canceled before completion."
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 30004
toc: true
---

> 💡 **Note:** This event occurs when the upgrade process is halted or canceled before completion.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### Event (string)

The type of event. For this event, the value is `Subscription.Upgrade.UpgradingDisabled`.

### EventCode (integer)

Unique code representing the event type. For `Subscription.Upgrade.UpgradingDisabled`, the event code is typically `16`.

### MetaData (object)

Additional dynamic metadata related to the event. This can include details such as the current subscription plan and the cancellation time.

#### MetaData Attributes

- **CurrentSubscriptionPlan (string):** The system name of the current subscription plan.
- **CancellationTime (timestamp):** The UTC timestamp indicating when the upgrade process was disabled.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `Subscription.Upgrade.UpgradingDisabled` event:

```json
{
  "EventCode": 16,
  "Event": "Subscription.Upgrade.UpgradingDisabled",
  "TenantSystemName": "example_tenant",
  "MetaData": {
    "CurrentSubscriptionPlan": "pro-plan",
    "CancellationTime": "2024-05-29T12:00:00Z"
  },
  "Created": "2024-05-29T11:05:32.520057Z"
}
```
