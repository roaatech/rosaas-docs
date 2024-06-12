---
title: "Tenant Availability Changed To Unhealthy"
description: ""
lead: "The `Tenant.Availability.ChangedToUnhealthy` event indicates a change in the availability status of a tenant to unhealthy within the RoSaaS system."
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 30012
toc: true
---

> 💡 **Note:** This event occurs when the availability status of a tenant changes to unhealthy.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### Event (string)

The type of event. For this event, the value is `Tenant.Availability.ChangedToUnhealthy`.

### EventCode (integer)

Unique code representing the event type. For `Tenant.Availability.ChangedToUnhealthy`, the event code is `4`.

### MetaData (object)

Additional dynamic metadata related to the event.

#### MetaData Attributes

- **ChangingDate (timestamp):** The UTC timestamp indicating when the availability status changed to unhealthy.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `Tenant.Availability.ChangedToUnhealthy` event:

```json
{
  "TenantSystemName": "example_tenant",
  "Event": "Tenant.Availability.ChangedToUnhealthy",
  "MetaData": {
    "ChangingDate": "2024-06-02T12:00:00Z"
  },
  "EventCode": 4,
  "Created": "2024-06-02T12:00:00Z"
}
```
