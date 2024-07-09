---
title: "Integrating with RoSaaS Webhooks"
description: ""
lead: "RoSaaS provides a powerful and flexible webhook system that allows external systems to receive real-time notifications about various events. This guide will walk you through the steps necessary to integrate your system with RoSaaS webhooks, ensuring seamless communication and event handling."
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "Webhooks"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0611"
weight: 51
toc: true
---

## Receive RoSaaS Events in Your Webhook Endpoint

Listen to events in your RoSaaS account on your webhook endpoint so your integration can automatically trigger reactions.

### Why Use Webhooks

When building RoSaaS integrations, you might want your applications to receive events as they occur in your RoSaaS accounts, so that your backend systems can execute actions accordingly.

To enable webhook events, you need to register webhook endpoints. After you register them, RoSaaS can push real-time event data to your application’s webhook endpoint when events happen in your RoSaaS account. RoSaaS uses HTTPS to send webhook events to your app as a JSON payload that includes an Event object.

Receiving webhook events is particularly useful for listening to asynchronous events such as when a tenant’s status changes, a subscription is upgraded, or a payment fails.

### Event Overview

RoSaaS uses events to notify you of important changes and activities in your account. When a significant event occurs, such as a tenant's status changing from active to passive, RoSaaS creates a new Event object. This object contains details about the event and its context.

Events are triggered by changes in the state of various resources within RoSaaS. For example, a `Tenant.StatusChanged` event occurs when a tenant's status changes. The data field of the event contains the state of the resource at the time of the change. In the case of a `Tenant.StatusChanged` event, it might include information about the previous status (e.g., active) and the new status (e.g., passive) of the tenant.

You can retrieve individual events or lists of events from RoSaaS using API endpoints. Additionally, RoSaaS provides a webhooks system that allows you to receive Event objects directly to an endpoint on your server. This enables your integration to automatically react to events, such as updating your internal systems when a `Tenant.StatusChanged` event occurs.

### Event Type Overview

ChatGPT
markdown
Copy code

- [Tenant.RegisteredInRoSaasDb](../event-type-objects/tenant_registered_in_rosaas_db)

  > Indicates that a tenant has been registered in the RoSaaS database.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Tenant.RegisteredInRoSaasDb event, please refer to the documentation by clicking on the event title." />}}

- [Tenant.StatusChanged](../event-type-objects/tenant_status_changed)

  > Indicates a change in the status of a tenant.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Tenant.StatusChanged event, please refer to the documentation by clicking on the event title." />}}

- [Subscription.Trial.UpgradedToStandard](../event-type-objects/subscription_trial_upgraded_to_standard)

  > Indicates that a trial subscription has been upgraded to a standard subscription.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Subscription.Trial.UpgradedToStandard event, please refer to the documentation by clicking on the event title." />}}

- [Subscription.Upgrade.Enabled](../event-type-objects/subscription_upgrade_enabled)

  > Indicates that users have requested an upgrade to an advanced plan.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Subscription.Upgrade.Enabled event, please refer to the documentation by clicking on the event title." />}}

- [Subscription.Upgrade.UpgradingDisabled](../event-type-objects/subscription_upgrade_upgrading_disabled)

  > Indicates that the request for an upgrade has been canceled or disabled.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Subscription.Upgrade.UpgradingDisabled event, please refer to the documentation by clicking on the event title." />}}

- [Subscription.Upgrade.HasBeenUpgraded](../event-type-objects/subscription_upgrade_has_been_upgraded)

  > Indicates that a subscription has been successfully upgraded.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Subscription.Upgrade.HasBeenUpgraded event, please refer to the documentation by clicking on the event title." />}}

- [Subscription.Downgrade.DowngradeEnabled](../event-type-objects/subscription_downgrade_downgrade_enabled)

  > Indicates that users have requested a downgrade to a lower-tier plan.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Subscription.Downgrade.DowngradeEnabled event, please refer to the documentation by clicking on the event title." />}}

- [Subscription.AutoRenewal.Enabled](../event-type-objects/subscription_autorenewal_enabled)

  > Indicates that auto-renewal for a subscription is enabled.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Subscription.AutoRenewal.Enabled event, please refer to the documentation by clicking on the event title." />}}

- [Subscription.Downgrade.DowngradingDisabled](../event-type-objects/subscription_downgrade_downgradingdisabled)

  > Indicates that the request for a downgrade has been canceled or disabled.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Subscription.Downgrade.DowngradingDisabled event, please refer to the documentation by clicking on the event title." />}}

- [Subscription.Downgrade.ForcedDowngradeEnabled](../event-type-objects/subscription_downgrade_forceddowngradeenabled)

  > Indicates that a forced downgrade has been enabled.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Subscription.Downgrade.ForcedDowngradeEnabled event, please refer to the documentation by clicking on the event title." />}}

- [Subscription.AutoRenewal.Disabled](../event-type-objects/subscription_autorenewal_disabled)

  > Indicates that auto-renewal for a subscription is disabled.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Subscription.AutoRenewal.Disabled event, please refer to the documentation by clicking on the event title." />}}

- [Subscription.AutoRenewal.HasBeenRenewedAutomatically](../event-type-objects/subscription_autorenewal_hasbeenrenewedautomatically)

  > Indicates that a subscription has been automatically renewed.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Subscription.AutoRenewal.HasBeenRenewedAutomatically event, please refer to the documentation by clicking on the event title." />}}

- [Subscription.Downgrade.HasBeenDowngraded](../event-type-objects/subscription_downgrade_hasbeendowngraded)

  > Indicates that a subscription has been successfully downgraded.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Subscription.Downgrade.HasBeenDowngraded event, please refer to the documentation by clicking on the event title." />}}

- [ExternalSystem.CreatedTenantResources](../event-type-objects/externalsystem_createdtenantresources)

  > Indicates that tenant resources have been created in an external system.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the ExternalSystem.CreatedTenantResources event, please refer to the documentation by clicking on the event title." />}}

- [Tenant.Availability.ChangedToUnhealthy](../event-type-objects/tenant_availability_changedtounhealthy)

  > Indicates a change in the availability status of a tenant to unhealthy.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Tenant.Availability.ChangedToUnhealthy event, please refer to the documentation by clicking on the event title." />}}

- [Subscription.SuspendedDueToUnpaid](../event-type-objects/subscription_suspendeddueunpaid)

  > Indicates that a subscription has been suspended due to unpaid charges.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Subscription.SuspendedDueToUnpaid event, please refer to the documentation by clicking on the event title." />}}

- [Subscription.AutoRenewal.AutoRenewalDisabled](../event-type-objects/subscription_autorenewal_autorenewaldisabled)

  > Indicates that auto-renewal for a subscription is disabled.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Subscription.AutoRenewal.AutoRenewalDisabled event, please refer to the documentation by clicking on the event title." />}}

- [Tenant.Availability.ChangedToHealthy](../event-type-objects/tenant_availability_changedtohealthy)

  > Indicates a change in the availability status of a tenant to healthy.
  >
  > {{< alert icon="💡" text="For further attribute details and an example data object of the Tenant.Availability.ChangedToHealthy event, please refer to the documentation by clicking on the event title." />}}

### Event Object

The Event object we send to your webhook endpoint provides a snapshot of the object that changed. They might include a `previous_attributes` property that indicates the change, when applicable.

See the full list of event types that we send to your webhook.

#### Example Event Payload

The following event shows a subscription update at the end of a trial.

```json
{
  "TenantSystemName": "example_tenant", // Tenant system name
  "EventCode": 1, // Unique event code
  "Event": "TrialSubscriptionUpgradedToStandard", // Event type
  "MetaData": {
    // Event-specific data
    "subscription_id": "sub_123456789", // Subscription ID
    "status": "upgraded" // New status
  },
  "Created": "2024-05-28T12:34:56Z" // UTC timestamp
}
```

### Create an Endpoint in Your System

- To integrate your external system with RoSaaS webhooks, follow these steps:

1. **Create an Endpoint in Your System:**

- Implement an endpoint in your system similar to the "Notify me" endpoint provided by RoSaaS. This endpoint should:

  - Accept incoming webhook notifications.
  - Include a Signing Secret in the header for secure verification.
  - Always return the following data:
    - `TenantSystemName` (string): The name of the tenant associated with your product within the RoSaaS system.
    - `Event` (string): The type of event being notified.
    - `EventCode` (int): A unique code representing the event type.
    - `MetaData` (dynamic): Additional dynamic metadata related to the event.
    - `Created` (DateTime): The timestamp indicating when the event notification was received.

2. **Access RoSaaS Panel:**

   - Log in to the RoSaaS panel using your credentials.

3. **Navigate to Products Page:**

   - Once logged in, navigate to the "Products" page either from the products list or using the sidebar navigation.

4. **Select Product and Navigate to Webhook Tab:**

   - Choose the desired product from the products list or sidebar.
   - In the product details page, locate and select the "Webhook" tab.

5. **Add Endpoint:**

   - In the top section of the "Webhook" tab, you will find an "Add Endpoint" button. Click on it to proceed.

6. **Fill Endpoint Form:**

   - A dialog form will appear for adding a new endpoint. Fill out the following details:
     - **Endpoint URL:** Provide the URL of the endpoint you created in your system.
     - **Signing Secret:** Either press the "Generate" button to generate a random secret or provide a specific value. This signing secret will be used in the header of the webhook notification requests for secure verification.
     - **Select Events to Listen To:** Choose one or more events from the list or select "Select All" to listen to all events.
     - **Description:** Optionally, provide a description for the webhook endpoint.

7. **Submit Form:**

   - After filling out the form, submit it to add the webhook endpoint to your RoSaaS product.

8. **Receive Webhook Notifications:**

   - Expose an HTTP endpoint in your system to receive webhook notifications. In the example above, the endpoint is `/api/WebhookListener/notifyme`.
   - The endpoint should accept POST requests containing the webhook payload data in the request body.

   ```csharp
   using Microsoft.AspNetCore.Mvc;
   using System.Collections.Generic;
   using System.Threading.Tasks;
   using Microsoft.Extensions.Configuration;
   using Microsoft.AspNetCore.Http;
   namespace YourNamespace.Controllers
   {
   [Route("api/[controller]")]
   [ApiController]
   public class WebhookListenerController : ControllerBase
   {
   private readonly IConfiguration \_configuration;

         public WebhookListenerController(IConfiguration configuration)
         {
               _configuration = configuration;
         }

         // POST: api/<WebhookListenerController>/notifyme
         [HttpPost("notifyme")]
         public async Task<IActionResult> NotifymeAsync(GlobalPayloadRequest model, [FromHeader(Name = "X-Signing-Secret")] string signingSecret)
         {
               // Retrieve the expected signing secret from configuration
               var expectedSecret = _configuration["RoSaaS:SigningSecret"];

               // Validate the signing secret
               if (signingSecret != expectedSecret)
               {
                  return Unauthorized("Invalid signing secret.");
               }

               // Store the received webhook payload data in your system
               // Example: Store.DB.Add(model);
               // Your implementation here

               return Ok();
         }
      }
   }
   ```

### Secure Your Webhook Endpoint

Ensure that your webhook endpoint is secure by validating the signature of incoming requests.
{{< alert icon="💡" text="The Signing Secret should be included in the header of the webhook notification requests for secure verification." />}}

By following these steps, your external system will be successfully integrated with RoSaaS webhooks, allowing seamless communication and event notifications between systems.
