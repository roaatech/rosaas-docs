---
title: "Product Client Credentials Tab"

description: "This document describes the functionalities and details available in the 'Client Credentials' tab for products within RoSaaS."

lead: "Learn how to manage client credentials and access tokens in the 'Client Credentials' tab of RoSaaS."

date: 2024-06-24T09:14:16+03:00
lastmod: 2024-06-24T09:14:16+03:00
draft: false
images: []
menu:
  docs:
    parent: "products"
weight: 37
toc: true
---

## Client Credentials Tab

The Client Credentials tab in RoSaaS allows you to manage the client credentials and access tokens for your products. This tab provides an overview of all clients, their statuses, and relevant actions that can be performed.

### Overview

- **Client Name:** The name of the client associated with the product.
- **Client ID:** The unique identifier for the client.
- **Status:** The current status of the client (Active/Inactive).
- **Client Type:** The type of client (e.g., External System).
- **Access Token Lifetime:** The duration for which the access token is valid.
- **Description:** A brief description of the client.

### Actions

You can perform the following actions within the Client Credentials tab:

#### Create New Client

To add a new client, follow these steps:

1. **Click on 'New Client':** This button is located at the top right corner of the Client Credentials tab.
2. **Fill in the Client Details:** In the "Create New Client" form, provide the following information:
   - **Display Name:** The name of the client.
   - **Client ID:** A unique identifier for the client.
   - **Description:** A brief description of the client.
   - **Access Token Lifetime:** The validity period of the access token in hours.
3. **Submit:** Click the "Submit" button to create the new client.

#### Edit Client

To edit an existing client, follow these steps:

1. **Locate the Client:** Find the client you want to edit in the list.
2. **Click on the 'Actions' Menu:** Click the "..." button in the Actions column.
3. **Select 'Edit':** Choose the "Edit" option to open the "Edit Client" form.
4. **Update the Details:** Modify the client details as needed.
5. **Submit:** Click the "Submit" button to save the changes.

#### Revoke Client

To revoke a client, follow these steps:

1. **Locate the Client:** Find the client you want to revoke in the list.
2. **Click on the 'Actions' Menu:** Click the "..." button in the Actions column.
3. **Select 'Revoke':** Choose the "Revoke" option to deactivate the client.

#### Manage Secrets

Each client can have multiple secrets associated with it. To manage these secrets:

1. **Click on the Keys Button:** Click the keys button next to the client name to expand the client details and view associated secrets.
2. **Create New Secret:** Click on "New Secret" and fill in the details such as Display Name and Expiration Date.
3. **Edit Secret:** Click on the "..." button next to a secret and choose "Edit" to modify it.
4. **Revoke Secret:** Click on the "..." button next to a secret and choose "Revoke" to deactivate it.

### Client Details

For each client, you can view comprehensive details, including:

- **Client Name**
- **Client ID**
- **Status**
- **Client Type**
- **Access Token Lifetime**
- **Description**

This tab provides a centralized location for managing all client-related configurations, ensuring secure and efficient access to your product's APIs.

For more detailed instructions on managing client credentials, refer to the respective documentation sections: [Creating Clients](../creating-clients), [Editing Clients](../editing-clients), and [Revoking Clients](../revoking-clients).
