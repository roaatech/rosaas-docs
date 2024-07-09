---
title: "Product Details Tab"

description: "A comprehensive guide to the Details tab in the Product Details section of RoSaaS, covering all essential information and configurations for efficient product management."

lead: "Understand the detailed information and configurations available in the Details tab of each product in RoSaaS to optimize your SaaS product management."
date: 2023-07-25T09:14:16+03:00
lastmod: 2023-07-25T09:14:16+03:00
draft: false
images: []
menu:
  docs:
    parent: "products"
weight: 34
toc: true
---

## Product Details Tab

The Details tab in the Product Details section of RoSaaS provides a centralized view of all essential information and configurations for each product. This tab is crucial for understanding the product's setup, API endpoints, and other relevant details that contribute to the efficient management and optimization of your SaaS offerings. Here’s a detailed breakdown of the elements you will find in the Details tab:

### Accessing the Details Tab

1. **Log In:** Start by logging in to your RoSaaS account using your credentials.
2. **Main Dashboard:** After a successful login, you will land on the main dashboard.
3. **Navigate to “Products”:** In the left-hand navigation menu, locate and click on “Products.”
4. **Select a Product:** From the list of products, select the one you want to explore by clicking on its name.
5. **Details Tab:** By default, you will be taken to the Details tab of the selected product.

### Key Elements in the Details Tab

#### Display Name

- **Description:** The user-friendly name associated with the product.
- **Purpose:** Helps users and administrators easily identify the product.

#### System Name

- **Description:** The unique identifier for the product used in system integrations.
- **Purpose:** Used for internal references and cannot be changed once set.

#### Client

- **Description:** The client or organization associated with the product.
- **Purpose:** Indicates which client owns or manages the product.

#### Description

- **Description:** A brief overview of the product's purpose and features.
- **Purpose:** Provides context and information about the product to users and administrators.

#### API Key

- **Description:** A unique key used for secure API access.
- **Purpose:** Essential for authenticating API requests and ensuring secure communication between systems.

### API Endpoints

#### Default Health Check URL

- **Method:** GET
- **URL:** The endpoint used to monitor the product's health.
- **Purpose:** Allows external systems to check the operational status of the product.

#### Health Status Change URL

- **Method:** POST
- **URL:** The endpoint used to update the product's health status.
- **Purpose:** Enables dynamic monitoring and status updates of the product's operational state.

#### Subscription Reset URL

- **Method:** POST
- **URL:** The endpoint used to reset subscription attributes.
- **Purpose:** Facilitates adjustments to subscription settings without deactivating the product.

#### Subscription Upgrade URL

- **Method:** POST
- **URL:** The endpoint used to upgrade subscription plans.
- **Purpose:** Allows seamless transitions to higher-tier subscription plans.

#### Subscription Downgrade URL

- **Method:** POST
- **URL:** The endpoint used to downgrade subscription plans.
- **Purpose:** Facilitates adjustments to lower-tier subscription plans.

#### Creation URL

- **Method:** POST
- **URL:** The endpoint responsible for creating new instances of the product's Tenants.
- **Purpose:** Supports the integration of new tenants (users or subscribers) into the product.

#### Activation URL

- **Method:** POST
- **URL:** The endpoint used to activate the product for its Tenants.
- **Purpose:** Grants tenants access to the product's features and services.

#### Deactivation URL

- **Method:** POST
- **URL:** The endpoint used to deactivate the product for its Tenants.
- **Purpose:** Restricts tenant access and pauses the usage of the product.

#### Deletion URL

- **Method:** POST
- **URL:** The endpoint used to delete the product for its Tenants.
- **Purpose:** Initiates the removal of the product from the tenant's workspace.

### Additional Information

- **Created Date:** The date when the product was created.
- **Last Updated Date:** The date when the product details were last updated.
- **Trial Type:** Indicates if the product has an optional trial period for new users.

### Managing Product Details

#### Editing Product Details

1. **Access Product Actions:** Click on the "Edit" button to modify the product details.
2. **Modify Information:** Update the necessary fields in the "Edit Product" form.
3. **Submit Changes:** Click "Submit" to save the updated product details.

By understanding and utilizing the information and configurations available in the Details tab, you can effectively manage your digital products within RoSaaS, ensuring optimal performance and seamless integration. For more detailed instructions on each feature, refer to the respective documentation pages.
