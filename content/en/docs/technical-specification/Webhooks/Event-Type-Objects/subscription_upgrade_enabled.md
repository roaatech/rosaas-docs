---
title: "Subscription Upgrade Enabled"
description: ""
lead: "The `Subscription.Upgrade.Enabled` event indicates that users have requested an upgrade to an advanced plan. This event signifies the initiation of an upgrade process from a lower-tier plan to a higher-tier plan."
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

> 💡 **Note:** This event signifies the initiation of an upgrade process from a lower-tier plan to a higher-tier plan.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### Event (string)

The type of event. For this event, the value is `Subscription.Upgrade.Enabled`.

### EventCode (integer)

Unique code representing the event type. For `Subscription.Upgrade.Enabled`, the event code is typically `9`.

### MetaData (object)

Additional dynamic metadata related to the event. This can include details such as whether the upgrade is enabled, the system name of the upgraded plan, the ID of the upgraded plan price, and the previous plan.

#### MetaData Attributes

- **upgradeEnabled (boolean):** Indicates whether the upgrade is enabled.
- **upgradedPlanSystemName (string):** The system name of the upgraded plan.
- **upgradedPlanPriceId (string):** The ID of the upgraded plan price.
- **previousPlan (string):** The system name of the previous plan.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `Subscription.Upgrade.Enabled` event:

```json
{
  "EventCode": 9,
  "Event": "Subscription.Upgrade.Enabled",
  "TenantSystemName": "apptomator-tenant-1716377056300",
  "MetaData": {
    "upgradeEnabled": true,
    "upgradedPlanSystemName": "enterprise-plan",
    "upgradedPlanPriceId": "0f3243d6-89ff-4934-9660-b7aa6d3d628c",
    "previousPlan": "pro-plan"
  },
  "Created": "2024-05-29T11:05:32.520057Z"
}
```
