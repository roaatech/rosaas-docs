---
title: "Product Details Exploration"
description: "Welcome to the Product Details Exploration section! Here, you will gain a comprehensive understanding of your digital products within the RoSaaS platform. Uncover valuable insights about each product, its configurations, and capabilities as a Software as a Service (SaaS) solution. This documentation empowers you to make informed decisions for efficient product management, SaaSification, and subscription handling."
lead: "Welcome to the Product Details Exploration section! Here, you will gain a comprehensive understanding of your digital products within the RoSaaS platform. Uncover valuable insights about each product, its configurations, and capabilities as a Software as a Service (SaaS) solution. This documentation empowers you to make informed decisions for efficient product management, SaaSification, and subscription handling."
date: 2023-07-25T13:36:17+03:00
lastmod: 2023-07-25T13:36:17+03:00
draft: false
images: []
menu:
  docs:
    parent: "Products"
    identifier: "Managing-Products-61a9c835936a92429a5d672d9a0481d2"
weight: 22
toc: true
---

## Access the "Product" Page

To get started, log in to your RoSaaS account using your credentials. After successful login, you will land on the main dashboard.

From the left-hand navigation menu, locate and click on "Products." This will take you to the Products page, where you can find the list of your digital products.

## Product List

The Product List provides a centralized and organized view of all your digital products and their associated details. From this list, you can perform various management actions to effectively handle your SaaS offerings.

## View Details

Click the "View Details" button (represented by "..." in the "Actions" column) for a specific product to access comprehensive insights into the product's attributes. This view is divided into two tabs:

### Details Tab

In the Details tab, you can access essential information about the product, including:

- **Name:** This is the name of the digital product you have created in RoSaaS. It serves as an identifier for the product within the platform.

- **Client:** The client refers to the owner of the product. In RoSaaS, a client has a dedicated workspace and is responsible for managing their specific product offerings.

- **Created Date:** The date when the product was initially created in RoSaaS. It provides information about the product's inception on the platform.

- **Last Updated Date:** This indicates the most recent date when the product's details were modified or updated. It helps track changes and version history for the product.

- **Default Health Check URL:** Provide the default health check URL for the product’s Tenants.

- **Health Status Change URL:** to inform external system that the specific tenant is unavailable.

- **Creation URL:** Specify the API endpoint responsible for creating the product’s Tenants.

- **Activation URL:** Specify the API endpoint for activating the product’s Tenants.

- **Deactivation URL:** Provide the API endpoint for deactivating the product’s Tenants.

- **Deletion URL:** The API endpoint to delete the product's tenant .

Understanding this information allows you to have insights into the product's configuration and its capabilities as a Software as a Service (SaaS) solution. You can use these details to make informed decisions about managing and optimizing your SaaS offerings.

### Subscriptions Tab

In the Subscriptions tab, you can access a list of all subscriptions associated with the selected product. This section provides detailed information about each subscription, allowing you to manage them effectively. Here are the additional details for the subscription data you provided:

- **Title:** The title represents the identifier for each subscription associated with the product. It helps differentiate between different subscription instances.

- **Unique Name:** The unique name corresponds to the unique identifier for each subscription. It is useful for backend systems and databases to distinguish between various subscriptions.

- **Health Check URL is Overridden:** This field indicates whether the health check URL for the subscription is overridden or not. When the health check URL is overridden, it means that a custom health check URL is being used for this specific subscription.

- **Status:** The status of each subscription provides information about its current state. The possible statuses and their meanings are as follows:

  - **Create request is sent:** The subscription is in the process of being created, and a request for creation has been sent.

  - **Creating:** The subscription is currently being created.

  - **Created As Active:** The subscription was successfully created and is now active and in use.

  - **Deactivate request is sent:** A deactivation request has been initiated for this subscription.

  - **Deactivating:** The subscription is currently being deactivated.

  - **Deactivate:** The subscription has been successfully deactivated.

- **Created Date:** This field indicates the date and time when each subscription was created. It helps track the subscription's inception and understand the timeline of subscription management.

By effectively utilizing these actions and exploring the product details, you can efficiently manage your digital products within RoSaaS, access comprehensive insights, and handle subscriptions seamlessly. This level of control empowers you to optimize the performance and subscription offerings of your SaaS products.

Congratulations! You now have a clear understanding of how to explore and manage your product details and subscriptions within RoSaaS.
