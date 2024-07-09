---
title: "Product Plan's Features Tab"
description: "A detailed guide on configuring and managing features for different product plans in RoSaaS."
lead: "Learn how to effectively add and manage features for various product plans in RoSaaS to provide tailored services to your tenants."
date: 2023-07-25T09:14:16+03:00
lastmod: 2023-07-25T09:14:16+03:00
draft: false
images: []
menu:
  docs:
    parent: "products"
weight: 41
toc: true
---

# Product Plan's Features Tab

## Overview

The Product Plan's Features tab allows you to assign specific features to different product plans. This ensures that each plan has a distinct set of functionalities tailored to meet the needs of different tenant types.

## Adding a Plan's Feature

1. **Plan**: Select the plan you want to add the feature to from the dropdown menu. This is essential for ensuring that the feature is associated with the correct subscription tier.
2. **Feature**: Choose the feature you wish to add. Features can be predefined and should be relevant to the plan. This step involves selecting from a list of existing features, each designed to enhance the plan's value.
3. **Description**: Provide a brief description of the feature to explain its purpose and benefits. This helps tenants understand what they are getting with each plan.
4. **Reset**: Define how often the feature limit resets. Options include Non-Resettable, Weekly, Monthly, and Annual. This setting is crucial for features that are limited in quantity, ensuring they are replenished according to the specified interval.
5. **Limit**: Set a limit for the feature. This could be a quantity or capacity, depending on the feature type. For example, if the feature is storage space, the limit might be set in gigabytes.
6. **Unit**: Specify the unit of measurement for the limit. This could be units like GB, MB, emails, etc., depending on the feature.
7. **Unit Display Name**: Enter the name of the unit that will be displayed to the tenants. This is the label that tenants will see, ensuring they understand the scope of their subscription.

## Example of Adding a Feature

### Number Type Feature

For a feature like "Storage Space":

- **Plan**: Select the relevant plan, e.g., "Standard Plan".
- **Feature**: Choose "Storage Space (Number)".
- **Description**: "Provides additional storage space for your data."
- **Reset**: Set to "Monthly".
- **Limit**: Define the limit, e.g., "50".
- **Unit**: Specify the unit, e.g., "GB".
- **Unit Display Name**: Enter "Gigabytes".

### Boolean Type Feature

For a feature like "Basic Analytics":

- **Plan**: Select the relevant plan, e.g., "Basic Plan".
- **Feature**: Choose "Basic Analytics (Boolean)".
- **Description**: "Provides access to basic analytics features."

## Managing Plan's Features

Once features are added to a plan, they can be managed through the Plan's Features tab. You can:

- **Edit**: Modify the details of the feature assigned to the plan. This allows for updates or corrections to feature settings.
- **Delete**: Remove a feature from the plan. This is useful for deprecating features that are no longer needed or are being replaced.
- **View Details**: See detailed information about each feature and its configuration for the plan. This helps in understanding how each feature is utilized within the plan.

## Publishing Plans

To control the visibility of each plan to tenants, use the toggle button located on the right side of each plan. This button allows you to quickly publish or unpublish plans as needed.

- **Publish**: When a plan is ready for tenants, toggle the button to publish it. This makes the plan available for new and existing tenants.
- **Unpublish**: If you need to hide a plan from tenants, toggle the button to unpublish it. This is useful for plans that are under maintenance or are being phased out.

## Best Practices

- Ensure that features are relevant and valuable to the target tenants of each plan.
- Regularly review and update features to align with changing tenant needs and product capabilities.
- Clearly describe each feature to help tenants understand the benefits and usage limits.
- Use the publish toggle button to manage plan availability efficiently.

## Additional Details for Plan Features

### Reset Options

- **Non-Resettable**: The feature limit does not reset; once it's used, it's depleted.
- **Weekly**: The feature limit resets every week, providing tenants with a fresh allocation of the feature.
- **Monthly**: The feature limit resets every month, aligning with typical billing cycles.
- **Annual**: The feature limit resets once a year, suitable for features with long-term usage patterns.

### Unit and Unit Display Name

The unit and unit display name fields are critical for ensuring tenants understand the limits of their subscription. For example, if the feature is related to API calls, the unit might be "calls" and the unit display name could be "API Calls".

By effectively managing features across different plans, you can provide a flexible and scalable SaaS product that meets diverse tenant requirements.
