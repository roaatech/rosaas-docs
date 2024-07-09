---
title: "Tenant Registered In RoSaas Db"
description: ""
lead: "The `Tenant.RegisteredInRoSaasDb` event indicates that a tenant has been successfully registered in the RoSaaS (Registration of SaaS) database. This event signifies the completion of the tenant registration process and provides detailed information about the tenant and their subscription."
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Event-Type-Objects"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 51
toc: true
---

> 💡 **Note:** This event occurs when a new tenant is added to the RoSaaS database, signifying the registration process completion.

## Event Attributes

### TenantSystemName (string)

The name of the tenant system within the RoSaaS database.

### EventCode (integer)

Unique code representing the event type. For `Tenant.RegisteredInRoSaasDb`, the event code is typically `1`.

### Event (string)

The type of event. For this event, the value is `Tenant.RegisteredInRoSaasDb`.

### MetaData (object)

Additional dynamic metadata related to the event. This can include details such as creation date, system name, and plan details.

#### MetaData Attributes

- **creationDate (timestamp):** The date and time when the tenant was created.
- **systemName (string):** The system name of the tenant.
- **endDate (timestamp):** The end date of the tenant's subscription or trial period.
- **Plan (string):** The system name of the tenant's subscription plan.
- **planPrice (decimal):** The price of the tenant's subscription plan.
- **Date (timestamp):** The date and time when the event metadata was generated.

### Created (timestamp)

The UTC timestamp indicating when the event was created.

## Example

Here is an example JSON representation of the `Tenant.RegisteredInRoSaasDb` event:

```json
{
  "EventCode": 1,
  "Event": "Tenant.RegisteredInRoSaasDb",
  "TenantSystemName": "example_tenant",
  "MetaData": {
    "creationDate": "2024-05-01T08:30:00Z",
    "systemName": "example_tenant_system",
    "endDate": "2025-05-01T08:30:00Z",
    "Plan": "Standard-Plan",
    "planPrice": 49.99,
    "Date": "2024-05-28T12:34:56Z"
  },
  "Created": "2024-05-28T12:34:56Z"
}
```
