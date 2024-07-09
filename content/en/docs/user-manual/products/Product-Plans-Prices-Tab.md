---
title: "Product Plan's Prices Tab"
description: "A comprehensive guide to the Plan's Prices tab in the Product Details section of RoSaaS, covering all essential information and configurations for efficient product pricing management."
lead: "Understand the detailed information and configurations available in the Plan's Prices tab of each product in RoSaaS to optimize your SaaS product pricing."
date: 2023-07-25T09:14:16+03:00
lastmod: 2023-07-25T09:14:16+03:00
draft: false
images: []
menu:
  docs:
    parent: "products"
weight: 42
toc: true
---

## Overview

The Plan's Prices tab is a critical section in the Product Details of RoSaaS, allowing administrators to manage and configure the pricing for each plan within a product. This tab provides a detailed overview of all pricing options available for each plan, including various billing cycles such as weekly, monthly, yearly, and custom cycles.

## Features

### Add Plan Price

The **Add Plan Price** button allows you to add a new price for a specific plan. Clicking this button opens a form where you can specify the details of the new pricing configuration.

### View Details

The **View Details** option in the actions menu provides a comprehensive view of the pricing configuration for a plan. This includes all relevant details such as the system name, cycle, price, publication status, and more.

### Edit

The **Edit** option in the actions menu allows you to modify the existing pricing details for a plan. This ensures that you can keep your pricing information up to date and accurate.

### Published Toggle

The published toggle button in the right of each plan allows you to control the publication status of the pricing. This determines whether the pricing is visible to the tenants.

### Delete

The **Delete** option in the actions menu allows you to remove a pricing configuration. This is useful for discontinuing old or obsolete pricing options.

## Adding a New Plan Price

To add a new plan price:

1. Click the **Add Plan Price** button.
2. Fill in the required fields:

   - **System Name**: A unique identifier for the pricing configuration.
   - **Plan**: Select the plan for which you want to add the price from the dropdown menu.
   - **Cycle**: Choose the billing cycle from the available options (Week, Month, Year, One Day, Three Day, Custom, Unlimited).
   - **Price**: Enter the price amount.
   - **Description**: Provide a description for the pricing (optional).

3. Click **Submit** to save the new pricing configuration.

### Example

For example, if you want to add a monthly price for the "Basic Plan," you would select "Basic Plan" as the plan, choose "Month" as the cycle, and enter the price amount (e.g., $10). Optionally, you can add a description to provide more context about this pricing option.

## Viewing and Editing Plan Prices

### Viewing Details

To view the details of a plan price:

1. Click on the **View Details** option from the actions menu.
2. This will display the following information:
   - **System Name**: The unique identifier for the pricing configuration.
   - **System Lock Status**: Indicates if the system is locked.
   - **Plan**: The name of the plan associated with this price.
   - **Cycle**: The billing cycle (e.g., Week, Month, Year).
   - **Published Status**: Indicates if the pricing is published and visible to tenants.
   - **Subscribed Status**: Indicates if there are active subscriptions under this pricing.
   - **Description**: A brief description of the pricing.
   - **Created Date**: The date when the pricing was created.
   - **Edited Date**: The last date when the pricing was edited.

### Editing Details

To edit a plan price:

1. Click on the **Edit** option from the actions menu.
2. Update the necessary fields in the form that appears.
3. Click **Submit** to save the changes.

### Example

If the price for the "Basic Plan" changes from $10 to $12 per month, you would edit the monthly pricing configuration for the "Basic Plan" and update the price field to $12.

## Publishing and Deleting Plan Prices

### Publishing

- **Toggle Button**: Use the toggle button on the right of each plan to control the publication status. This feature allows you to make the pricing visible or invisible to the tenants based on your business needs.

### Deleting

- **Delete Option**: To delete a plan price, select the **Delete** option from the actions menu. Confirm the deletion to permanently remove the pricing configuration.

### Example

If a pricing option for a "Seasonal Plan" is no longer needed, you can delete it to ensure that it does not appear as an available option for new or existing tenants.

## Conclusion

By understanding and utilizing the Plan's Prices tab, you can effectively manage the pricing strategies for your SaaS products. This tab provides flexibility in setting and adjusting prices, ensuring that you can meet the diverse needs of your customers and adapt to market changes.

For more detailed information on each action and field, refer to the specific sections in the RoSaaS documentation.
