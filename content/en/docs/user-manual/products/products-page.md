---
title: "Products"

description: "Products in RoSaaS are digital offerings that can be easily transformed into fully functional Software as a Service (SaaS) solutions, providing businesses with a centralized workspace for efficient management and optimization."

lead: "Products in RoSaaS are digital assets that can be seamlessly transformed into fully functional Software as a Service (SaaS) solutions, providing businesses with a centralized workspace for efficient management and optimization."
date: 2023-07-25T09:14:16+03:00
lastmod: 2024-06-12T12:00:00+03:00
draft: false
images: []
menu:
  docs:
    parent: "products"
weight: 31
toc: true
---

## Products Page

The Products page in RoSaaS serves as a centralized workspace for managing all your digital products and their SaaSification process. From this page, you can create new products, view existing ones, and access comprehensive details about each product’s features and subscription plans. Here’s a step-by-step guide on how to navigate and utilize the Products page effectively:

### Accessing the Products Page

1. **Log In:** Start by logging in to your RoSaaS account using your credentials.
2. **Main Dashboard:** After successful login, you will land on the main dashboard.
3. **Navigate to “Products”:** In the left-hand navigation menu, locate and click on “Products.” This action will take you to the Products page.

### Product List

The Product List provides an overview of all digital products. Each row in the list contains the following information:

- **Display Name:** The user-friendly name of the product.
- **System Name:** A unique identifier for the product.
- **Client:** The client associated with the product.
- **Date:** The date when the product was created or last modified.
- **Actions:** Options to view details, edit, or delete the product.

### Product Actions

#### Create Product

To add a new digital product to RoSaaS and initiate its transformation into a fully functional Software as a Service (SaaS) solution, follow these steps:

1. **Navigate to the "Create Product" Form:** From the main dashboard, log in to your RoSaaS account. Then, click on the plus button and select “Add Product” from the dropdown menu. Alternatively, you can use the button on the products list page to navigate to the form.

2. **Fill in Product Details:** In the "Create Product" form, provide the following details for your new product:
   - **System Name:** This unique identifier is automatically generated based on the Display Name. It serves as a distinct name for referencing and distinguishing components within the integration process. You can modify the System Name if needed before submitting. Once submitted, the System Name becomes permanent and cannot be changed.
   - **Display Name:** Enter the name of your new product. This is the user-friendly and customizable name associated with the product. You can modify and update the Display Name without affecting the underlying system integration.
   - **Description:** Provide a brief description of your product. This description helps convey the purpose and features of the product to users and administrators.
   - **API Key:** Use the box icon to auto-generate an API key or manually input any value. The API key is essential for secure authentication and authorization processes.
   - **Default Health Check Url:** Provide the default health check URL that external systems will use to monitor the health and availability of the product.
   - **Health Status Change URL:** This URL triggers changes in the health status of a subscription from an external system, allowing dynamic monitoring of operational states.
   - **Subscription Reset URL:** This URL initiates a reset or reconfiguration of subscription attributes from an external system, facilitating adjustments without deactivation.
   - **Subscription Upgrade URL:** This URL requests an upgrade in the subscription plan from an external system, enabling seamless transitions to higher-tier plans.
   - **Subscription Downgrade URL:** Similar to the upgrade URL, this initiates a downgrade in the subscription plan from an external system, facilitating adjustments to lower-tier plans.
   - **Creation URL:** This API endpoint is responsible for creating instances of the product's Tenants when new tenants (users or subscribers) are added, providing seamless integration for external systems in the creation process.
   - **Activation URL:** Specify the API endpoint that external systems will use to activate the product for its Tenants, granting them access to the product's features and services.
   - **Deactivation URL:** Provide the API endpoint that external systems will use to deactivate the product for its Tenants, restricting their access and pausing the usage of the product.
   - **Deletion URL:** Specify the API endpoint that external systems will use to delete the product for its Tenants, initiating the removal of the product from the tenant's workspace.
3. **Submit the Product Details:** Once you have filled in all the necessary details, click the "Submit" button to create the new product. Upon successful submission, you will receive a confirmation message, and the newly added product will be listed among the existing products on the Products page.

#### Edit Product

To update an existing product's details, follow these steps:

1. **Locate the Product:** From the Products page, locate the product you want to edit in the list of existing products.
2. **Access Product Actions:** In the "Actions" column for the selected product, click on the "..." button to reveal a dropdown menu.
3. **Select "Edit":** From the dropdown menu, choose "Edit" to access the "Edit Product" form.
4. **Modify Product Details:** In the "Edit Product" form, you can modify the following details:
   - **Display Name:** Change the name of the product.
   - **Description:** Update the description of the product.
   - **API Key:** Modify the API key.
   - **Default Health Check Url:** Update the default health check URL.
   - **Health Status Change URL:** Modify the health status change URL.
   - **Subscription Reset URL:** Update the subscription reset URL.
   - **Subscription Upgrade URL:** Change the subscription upgrade URL.
   - **Subscription Downgrade URL:** Modify the subscription downgrade URL.
   - **Creation URL:** Change the API endpoint responsible for creating the product.
   - **Activation URL:** Change the API endpoint for activating the product.
   - **Deactivation URL:** Update the API endpoint for deactivating the product.
   - **Deletion URL:** Change the API endpoint for deleting the product.
5. **Submit the Changes:** Once you have made the necessary changes, click the "Submit" button to save the updated product details.

#### Delete Product

To remove a product from RoSaaS, follow these steps:

1. **Locate the Product:** From the Products page, locate the product you want to delete in the list of existing products.
2. **Access Product Actions:** In the "Actions" column for the selected product, click on the "..." button to reveal a dropdown menu.
3. **Select "Delete":** From the dropdown menu, choose "Delete" to initiate the deletion process.
4. **Confirmation Prompt:** A confirmation prompt will appear, asking you to confirm the deletion.
5. **Choose "Yes" or "No":** You will be presented with two options - "Yes" or "No." Click "Yes" to proceed with the deletion or "No" to cancel the operation.

Please note that deleting a product is an irreversible action, and all associated data and subscriptions will be permanently removed from RoSaaS. Exercise caution before proceeding with the deletion.

By effectively utilizing these actions, you can efficiently manage your digital products within RoSaaS, access detailed information about each product, and handle subscriptions seamlessly. This level of control empowers you to optimize the performance and subscription offerings of your SaaS products.

## Product Details

For each product, you can view comprehensive details.

By accessing the product details, you can manage and optimize the configurations and capabilities of your digital products, ensuring efficient SaaSification and subscription management.

Congratulations! You now have a clear understanding of how to manage your products effectively through the RoSaaS platform.
