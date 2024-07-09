---
title: "Product Webhook Tab"

description: "Configure webhooks for your product to enable real-time communication and automation."

lead: "Webhooks in RoSaaS allow you to set up automated notifications and actions based on specific events related to your products."

date: 2023-07-25T09:14:16+03:00
lastmod: 2023-07-25T09:14:16+03:00
draft: false
images: []
menu:
  docs:
    parent: "products"
weight: 36
toc: true
---

## Webhook Tab

The Webhook tab enables you to configure webhooks for your products, allowing real-time communication and automation based on specific events. This powerful feature lets you set up automated notifications and actions, enhancing the efficiency and responsiveness of your SaaS offerings.

### Configuring Webhooks

In the Webhook tab, you can manage your webhook endpoints, specifying the URL, events to listen for, and other details:

- **URL:** The endpoint URL where the webhook will send the data.
- **Events to Listen:** The specific events that will trigger the webhook. For example, Tenant.RegisteredInRoSaasDb or Subscription.Upgrade.UpgradingDisabled.
- **Signing Secret:** A secret key used to sign the webhook payloads to ensure secure communication.
- **Activation Status:** Indicates whether the webhook is active or inactive.
- **Description:** A brief description of the webhook’s purpose.
- **Actions:** Options to edit or delete the webhook configuration.

To add a new webhook, click on the "Add Endpoint" button and provide the necessary details.

For more detailed information on how to configure and use webhooks, please refer to the [Webhooks Documentation](../../../technical-specification/webhooks/integrating-with-rosaas-webhooks/).
