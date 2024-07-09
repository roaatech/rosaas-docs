---
title: "Product Plans Tab"

description: "A comprehensive guide to the Plans tab in the Product Details section of RoSaaS, covering all essential information and configurations for efficient product management."

lead: "Understand the detailed information and configurations available in the Plans tab of each product in RoSaaS to optimize your SaaS product management."
date: 2023-07-25T09:14:16+03:00
lastmod: 2023-07-25T09:14:16+03:00
draft: false
images: []
menu:
  docs:
    parent: "products"
weight: 39
toc: true
---

# Plans Tab

The Product Plans tab is an essential section where you can manage the different subscription plans for your products. Each plan can be customized to meet the specific needs of your users. Below is an overview of the elements found in the Product Plans tab.

## Overview of Product Plans Tab

### Elements in the Product Plans Tab:

1. **Display Name**: This is the user-friendly name of the plan. It helps users easily identify and understand the purpose of the plan.
2. **System Name**: The unique identifier for the plan used within the system. This name is critical for system processes and integration, ensuring that each plan is distinct and correctly referenced in backend operations.
3. **Status**: Indicates whether the plan is published or unpublished.

   - **Published**: Means the plan is active and available for users to subscribe.
   - **Unpublished**: Indicates the plan is not active and not visible to users.

4. **Tenancy Type**: Specifies if the plan is "Planned" or otherwise. This helps in categorizing the plans based on their implementation status or lifecycle stage.
5. **System Lock Status**: Shows if the system is locked or unlocked.

   - **Locked**: The plan settings are fixed and cannot be modified by users.
   - **Unlocked**: The plan settings can be adjusted as needed.

6. **Subscribers**: The number of subscribers currently using the plan. This provides a quick view of the plan's popularity and usage.
7. **Description**: A brief overview of the plan's features and benefits. This helps users understand what the plan offers and its suitability for their needs.
8. **Display Order**: The order in which the plans are displayed. Plans with a lower display order value will appear first, helping to prioritize and organize the plans on the interface.
9. **Downgrade Plan**: Specifies the plan to which a subscription will transfer if it becomes inactive. This ensures continuity for users whose current plans are downgraded.
10. **Trial Period In Days**: Will appear if the product trial period type is set to "Each Plan Has Optional Trial Period." This defines how long the trial period will last before the user is moved to the full plan.

11. **Actions**: Options to manage the plan, including:
    - **Edit**: Opens the form to update the plan details.
    - **Published**: Toggles the plan's published status.
    - **Delete**: Removes the plan from the system.

### Adding a New Plan

To add a new plan, click on the "Add Plan" button. This will open a form where you can enter the following details:

- **Display Name**: The user-friendly name of the plan.
- **System Name**: The unique identifier for the plan within the system.
- **Description**: A brief description of the plan.
- **Display Order**: The order in which the plan will be displayed.
- **Trial Period In Days**: The trial period duration, if applicable.
- **Downgrade Plan**: The plan to which the subscription will transfer if it becomes inactive.

After filling in the details, click the "Submit" button to save the new plan.

### Editing a Plan

To edit an existing plan, locate the plan in the list and click on the "..." button under the Actions column. Select "Edit" from the dropdown menu. This will open a form where you can update the plan's details. Make the necessary changes and click "Submit" to save the updates.

### Publishing or Unpublishing a Plan

To change the published status of a plan, click on the "..." button under the Actions column for the respective plan and select "Published." This will toggle the plan between published and unpublished statuses, making it available or unavailable to users.

### Deleting a Plan

To delete a plan, click on the "..." button under the Actions column for the respective plan and select "Delete." Confirm the deletion to remove the plan from the system.

## Notes:

- **Downgrade Plan**: This field allows you to specify a fallback plan for subscribers if their current subscription becomes inactive.
- **Trial Period In Days**: This field is relevant if the product's trial period type is set to "Each Plan Has Optional Trial Period."

By effectively managing your product plans, you can ensure that your offerings are tailored to meet the diverse needs of your users and maximize customer satisfaction.
