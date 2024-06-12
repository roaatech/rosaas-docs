---
title: "Subscription Trial Upgraded To Standard"
description: ""
lead: "The `Subscription.Trial.UpgradedToStandard` event indicates that a trial subscription has been upgraded to a standard subscription. This event occurs when a trial subscription transitions to a paid, standard subscription plan."
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 30003
toc: true
---

> 💡 **Note:** This event occurs when a trial subscription transitions to a paid, standard subscription plan.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### EventCode (integer)

Unique code representing the event type. For `Subscription.Trial.UpgradedToStandard`, the event code is typically `5`.

### Event (string)

The type of event. For this event, the value is `Subscription.Trial.UpgradedToStandard`.

### MetaData (object)

Additional dynamic metadata related to the event. This can include details such as the trial plan system name, standard plan system name, trial period in days, and date.

#### MetaData Attributes

- **TrialPlanSystemName (string):** The system name of the trial plan.
- **StandardPlanSystemName (string):** The system name of the standard plan.
- **TrialPeriodInDays (integer):** The number of days in the trial period.
- **Date (timestamp):** The date and time when the event metadata was generated.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `Subscription.Trial.UpgradedToStandard` event:

```json
{
  "EventCode": 5,
  "Event": "Subscription.Trial.UpgradedToStandard",
  "TenantSystemName": "example_tenant",
  "MetaData": {
    "TrialPlanSystemName": "trial_plan_example",
    "StandardPlanSystemName": "standard_plan_example",
    "TrialPeriodInDays": 14,
    "Date": "2024-05-28T12:34:56Z"
  },
  "Created": "2024-05-28T12:34:56Z"
}
```
