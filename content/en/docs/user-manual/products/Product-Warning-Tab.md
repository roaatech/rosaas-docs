---
title: "Product Warning Tab"
description: "A comprehensive guide to the Warnings tab in the Product Details section of RoSaaS, covering all essential information and configurations for efficient warning management."
lead: "Understand the detailed information and configurations available in the Warnings tab of each product in RoSaaS to optimize your SaaS product management."
date: 2023-07-25T09:14:16+03:00
lastmod: 2023-07-25T09:14:16+03:00
draft: false
images: []
menu:
  docs:
    parent: "products"
weight: 44
toc: true
---

# Product Warning Tab

## Overview

The Product Warning tab in RoSaaS allows you to manage and configure various warning messages that are critical for maintaining the health and integrity of your product and tenant subscriptions. This section provides a detailed view and customization options for different warning scenarios.

## Warning Types

### Activation URL

- **Description**: The activation URL is mandatory. No tenant creation or activation can occur without it.
- **Purpose**: Ensures that the tenant activation process is correctly routed through the specified URL.

### Creation URL

- **Description**: The creation URL is mandatory. No tenant can be established without it.
- **Purpose**: Validates the tenant creation process through the provided URL.

### Deactivation URL

- **Description**: The deactivation URL is mandatory. No tenant creation or activation can occur without it.
- **Purpose**: Manages the tenant deactivation process, ensuring it's correctly routed.

### Deletion URL

- **Description**: The deletion URL is mandatory. No tenant creation or activation can occur without it.
- **Purpose**: Ensures proper routing for tenant deletion processes.

### Default Health Check URL

- **Description**: The health check URL is required for continuous validation of the availability of the tenant’s resources.
- **Purpose**: Regularly checks the health status of tenant resources to ensure availability.

### Health Status Informer URL

- **Description**: This URL is crucial for alerting the external system that one of the tenants is unavailable.
- **Purpose**: Notifies the external system about tenant unavailability.

### Subscription Reset URL

- **Description**: You won't be able to reset a tenant’s subscription without saving the Subscription Reset URL.
- **Purpose**: Manages subscription resets for tenants.

### Subscription Downgrade URL

- **Description**: Upgrading a tenant’s subscription won’t be possible without saving the Subscription Upgrade URL.
- **Purpose**: Controls the process of downgrading tenant subscriptions.

### Subscription Upgrade URL

- **Description**: Upgrading a tenant’s subscription won’t be possible without saving the Subscription Upgrade URL.
- **Purpose**: Manages the process of upgrading tenant subscriptions.

### API Key

- **Description**: External system’s API security will be compromised unless you create a private API key.
- **Purpose**: Ensures secure API communication by requiring a private API key.

## Managing Warnings

Clients can modify and customize warning messages and types through the settings section. This allows for tailored warnings that fit specific needs and scenarios within the product management environment.

## Best Practices

- Regularly review and update warning messages to keep them relevant and clear.
- Ensure all mandatory URLs are correctly configured to avoid service disruptions.
- Monitor health status and resource availability proactively to maintain tenant satisfaction.
- Use clear and concise messages to communicate issues effectively to your team and tenants.

By following these best practices, you can maintain a robust and reliable SaaS environment, minimizing downtime and ensuring a seamless experience for your tenants.
