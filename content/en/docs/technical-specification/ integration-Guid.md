---
title: " Integration Guid"
description: ""
lead: "Welcome to the Integration Guide for connecting your External System with the ROSAS platform. This guide will walk you through the necessary steps to integrate your product's external system with ROSAS, enabling seamless communication and interaction between your system and ROSAS features.
"
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "technical-specification"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0610"
weight: 10
toc: true
---

## Authentication

In this section, you will learn how to authenticate your External System 2 with ROSAS, ensuring secure access to privileged endpoints.

### POST: Generate Client Access Token for External System

This endpoint generates an access token required for authentication in various protected endpoints across the API.

[Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#ef205d12-d344-40d7-9a68-2f70c4d52d48:~:text=POST-,Generate%20client%20access%20token%20for%20external%20system,-Tenant)

## Tenant Management

Tenant management is crucial for providing customized experiences within the ROSAS platform. This section covers various operations related to tenant management.

### POST: Set the Tenant as Created

This endpoint is used to inform ROSAS that the tenant's resources have been successfully created and activated.

[Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#32ff1914-34ea-4ede-84f9-270dc8538d66:~:text=POST-,Set%20the%20tenant%20as%20Created,-POST)

### POST: Set the Tenant as Active

This endpoint is used to activate a tenant's resources, indicating that they are ready to be used.

[Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#32ff1914-34ea-4ede-84f9-270dc8538d66:~:text=POST-,Set%20the%20tenant%20as%20Active,-POST)

### POST: Set the Tenant as Inactive

This endpoint is used to deactivate a tenant's resources, temporarily disabling their access.

[Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#32ff1914-34ea-4ede-84f9-270dc8538d66:~:text=POST-,Set%20the%20tenant%20as%20Inactive,-POST)

### POST: Set the Tenant as Deleted

This endpoint is used to inform ROSAS that the tenant's resources have been permanently deleted.

[Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#32ff1914-34ea-4ede-84f9-270dc8538d66:~:text=Set%20the%20tenant%20as%20Deleted)

### POST: Upsert Tenant's Metadata

This endpoint allows the external system to store custom metadata associated with the product's tenant. Metadata is stored using a flexible JSON object structure, granting the external system the capacity to save assorted metadata related to the tenant.

[Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#ef205d12-d344-40d7-9a68-2f70c4d52d48:~:text=Upsert%20Tenant%27s%20Metadata)

### GET: Get Tenant's Status

This endpoint retrieves the status of a tenant.

[Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#ef205d12-d344-40d7-9a68-2f70c4d52d48:~:text=GET-,Get%20Tenant%27s%20Status,-GET)

### GET: Get Tenant's Metadata

This endpoint retrieves the metadata associated with a tenant.

[Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#ef205d12-d344-40d7-9a68-2f70c4d52d48:~:text=Get%20Tenant%27s%20Metadata)

## Ending

Congratulations! You've reached the end of the Integration Guide for connecting your External System 2 with ROSAS. By following the steps outlined in this guide, you've successfully integrated your product's external system with ROSAS, unlocking a range of powerful features and capabilities.

**Next Steps:**

- Test your integration thoroughly to ensure seamless communication between your external system and ROSAS.
- Explore ROSAS documentation and resources to discover additional features and optimizations.
- Should you have any questions or need further assistance, don't hesitate to contact our dedicated support team.
