---
title: "Product Actions"
description: "The Product Actions section in RoSaaS allows you to manage and perform various actions for your digital products, including creating new products, updating existing ones, and deleting products when necessary."
lead: "The Product Actions section in RoSaaS allows you to manage and perform various actions for your digital products, including creating new products, updating existing ones, and deleting products when necessary."
date: 2023-07-25T11:58:42+03:00
lastmod: 2023-07-25T11:58:42+03:00
draft: false
images: []
menu:
  docs:
    parent: "Products"
    identifier: "product-actions-a7585159740f7a874562fcca68272e27"
weight: 21
toc: true
---

## Access the "Product" Page

To get started, log in to your RoSaaS account using your credentials. After successful login, you will land on the main dashboard.

From the left-hand navigation menu, locate and click on "Products." This will take you to the Products page, where you can find the list of your digital products.

**Note:** The "Products" section in the sidebar has an accordion to display the list of all products. You can easily navigate from the sidebar to access the details of each product.

## Product Actions

The Product Actions section provides a centralized platform to efficiently manage your digital products, enabling smooth SaaSification and streamlined subscription management. Explore the following sub-sections for detailed documentation on different product-related actions:

### Create Product

To add a new digital product to RoSaaS and initiate its transformation into a fully functional Software as a Service (SaaS) solution, follow these steps:

- **Navigate to the "Create Product" Page:** From the main dashboard, log in to your RoSaaS account. Then, click on the plus button and selecting “Add Product” from the dropdown menu.

- **Fill in Product Details:** In the "Create Product" form, provide the following details for your new product:

  - **System Name:** (Automatically Generated) This unique identifier is automatically generated based on the Display Name. It serves as a distinct name for referencing and distinguishing components within the integration process. You can modify the System Name if needed before submitting. Once submitted, the System Name becomes permanent and cannot be changed.

  - **Display Name:** Enter the name of your new product. This is the user-friendly and customizable name associated with the product. You can modify and update the Display Name without affecting the underlying system integration.

  - **Description:** Provide a brief description of your product. This description helps convey the purpose and features of the product to users and administrators.

  - **API Key:** Use the box icon to auto-generate an API key or manually input any value. The API key is essential for secure authentication and authorization processes.

  - **Default Health Check Url:** Provide the default health check URL that external systems will use to monitor the health and availability of the product.

  - **Creation Url:** This API endpoint is responsible for creating instances of the product's Tenants when new tenants (users or subscribers) are added, providing seamless integration for external systems in the creation process.

  - **Activation Url:** Specify the API endpoint that external systems will use to activate the product for its Tenants, granting them access to the product's features and services.

  - **Deactivation Url:** Provide the API endpoint that external systems will use to deactivate the product for its Tenants, restricting their access and pausing the usage of the product.

  - **Deletion Url:** Specify the API endpoint that external systems will use to delete the product for its Tenants, initiating the removal of the product from the tenant's workspace.
  - **Health Status Change URL:** This URL triggers changes in the health status of a subscription from an external system, allowing dynamic monitoring of operational states.
  - **Subscription Reset URL:** This URL initiates a reset or reconfiguration of subscription attributes from an external system, facilitating adjustments without deactivation.
  - **Subscription Upgrade URL:** This URL requests an upgrade in the subscription plan from an external system, enabling seamless transitions to higher-tier plans.

  - **Subscription Downgrade URL:** Similar to the upgrade URL, this initiates a downgrade in the subscription plan from an external system, facilitating adjustments to lower-tier plans.

  - **Submit the Product Details:** Once you have filled in all the necessary details, click the "Submit" button to create the new product. Upon successful submission, you will receive a confirmation message, and the newly added product will be listed among the existing products on the Products page.

Congratulations! You have successfully created a new digital product in RoSaaS, and it is now ready to be SaaSified and managed within the platform.

### Edit Product

To update an existing product's details, follow these steps:

- **Locate the Product:** From the Products page, locate the product you want to edit in the list of existing products.

- **Access Product Actions:** In the "Actions" column for the selected product, click on the "..." button to reveal a dropdown menu.

- **Select "Edit":** From the dropdown menu, choose "Edit" to access the "Edit Product" form.

- **Modify Product Details:** In the "Edit Product" form, you can modify the following details:

  - **Name:** Change the name of the product.
  - **Default Health Check Url:** Update the default health check URL.
  - **Creation Url:** Modify the API endpoint responsible for creating the product.
  - **Activation Url:** Change the API endpoint for activating the product.
  - **Deactivation Url:** Update the API endpoint for deactivating the product.
  - **Deletion Url:** Change the API endpoint for deleting the product.

5. **Submit the Changes:** Once you have made the necessary changes, click the "Submit" button to save the updated product details.

Congratulations! You have successfully edited the product in RoSaaS, and the changes are now applied to the product's configuration and SaaS capabilities.

### Delete Product

To remove a product from RoSaaS, follow these steps:

1. **Locate the Product:** From the Products page, locate the product you want to delete in the list of existing products.

2. **Access Product Actions:** In the "Actions" column for the selected product, click on the "..." button to reveal a dropdown menu.

3. **Select "Delete":** From the dropdown menu, choose "Delete" to initiate the deletion process.

4. **Confirmation Prompt:** A confirmation prompt will appear, asking you to confirm the deletion.

5. **Choose "Yes" or "No":** You will be presented with two options - "Yes" or "No." Click "Yes" to proceed with the deletion or "No" to cancel the operation.

Please note that deleting a product is an irreversible action, and all associated data and subscriptions will be permanently removed from RoSaaS. Exercise caution before proceeding with the deletion.

By effectively utilizing these actions, you can efficiently manage your digital products within RoSaaS, access detailed information about each product, and handle subscriptions seamlessly. This level of control empowers you to optimize the performance and subscription offerings of your SaaS products.

Congratulations! You now have a clear understanding of how to manage your products effectively through the action buttons provided in RoSaaS.
