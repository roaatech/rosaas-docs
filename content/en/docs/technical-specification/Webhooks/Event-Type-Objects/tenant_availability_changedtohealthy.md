---
title: "Tenant Availability Changed to Healthy"
description: ""
lead: "The `Tenant.Availability.ChangedToHealthy` event indicates a change in the availability status of a tenant to healthy within the RoSaaS system."
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 30014
toc: true
---

> 💡 **Note:** This event occurs when the availability status of a tenant changes to healthy within the RoSaaS system.

## Event Attributes

### MetaData (object)

Additional dynamic metadata related to the event.

#### MetaData Attributes

- **ChangingDate (timestamp):** The UTC timestamp indicating when the availability status changed to healthy.

## Example

Here is an example JSON representation of the `Tenant.Availability.ChangedToHealthy` event:

```json
{
  "MetaData": {
    "ChangingDate": "2024-06-04T10:00:00Z"
  }
}
```
