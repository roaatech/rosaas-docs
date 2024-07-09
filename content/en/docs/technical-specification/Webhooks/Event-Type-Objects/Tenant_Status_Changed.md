---
title: "Tenant Status Changed"
description: ""
lead: "The `Tenant.StatusChanged` event indicates a change in the status of a tenant within the RoSaaS system. This event signifies any modification or update to the status of a tenant, providing detailed information about the new status and other relevant attributes."
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 62
toc: true
---

> 💡 **Note:** This event signifies any modification or update to the status of a tenant within the RoSaaS system.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### EventCode (integer)

Unique code representing the event type. For `Tenant.StatusChanged`, the event code is typically `2`.

### Event (string)

The type of event. For this event, the value is `Tenant.StatusChanged`.

### MetaData (object)

Additional dynamic metadata related to the event. This can include details such as the new tenant status, date, and plan details.

#### MetaData Attributes

- **NewTenantStatus (string):** The new status of the tenant.
- **Date (timestamp):** The date and time when the event metadata was generated.
- **Plan (string):** The system name of the tenant's subscription plan.
- **planPrice (decimal):** The price of the tenant's subscription plan.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `Tenant.StatusChanged` event:

```json
{
  "EventCode": 2,
  "Event": "Tenant.StatusChanged",
  "TenantSystemName": "example_tenant",
  "MetaData": {
    "NewTenantStatus": "active",
    "Date": "2024-05-28T12:34:56Z",
    "Plan": "Standard-Plan",
    "planPrice": 49.99
  },
  "Created": "2024-05-28T12:34:56Z"
}
```
