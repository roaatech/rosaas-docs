---
title: "External System Created Tenant Resources"
description: ""
lead: "The `ExternalSystem.CreatedTenantResources` event indicates that tenant resources have been created in an external system. This event occurs when resources associated with a tenant are successfully created within an external system."
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 71
toc: true
---

> 💡 **Note:** This event signifies the successful creation of tenant resources in an external system.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### Event (string)

The type of event. For this event, the value is `ExternalSystem.CreatedTenantResources`.

### EventCode (integer)

Unique code representing the event type. For `ExternalSystem.CreatedTenantResources`, the event code is `19`.

### MetaData (object)

Additional dynamic metadata related to the event.

#### MetaData Attributes

- **Date (timestamp):** The UTC timestamp indicating when the metadata was generated.
- **Plan (string):** The system name of the plan associated with the tenant resources.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `ExternalSystem.CreatedTenantResources` event:

```json
{
  "TenantSystemName": "example_tenant",
  "Event": "ExternalSystem.CreatedTenantResources",
  "MetaData": {
    "Date": "2024-06-02T12:00:00Z",
    "Plan": "enterprise-plan"
  },
  "EventCode": 19,
  "Created": "2024-06-02T12:00:00Z"
}
```
