---
title: " RoSaaS API Integration"
description: ""
lead: "Welcome to the Integration Guide for connecting your External System with the RoSaaS platform. This guide will walk you through the necessary steps to integrate your product's external system with RoSaaS, enabling seamless communication and interaction between your system and RoSaaS features.
"
date: 2023-08-15T12:13:37+03:00
lastmod: 2023-08-15T12:13:37+03:00
draft: false
images: []
menu:
  docs:
    parent: "technical-specification"
    identifier: " integration-Guid-a676682e606aa6c231a4a878310c0610"
weight: 50
toc: true
---

## Introduction

> This documentation outlines the integration process for `external systems` to seamlessly interact with `RoSaaS` system. To establish integration, `external systems` are required to implement a specific set of designated endpoints. The `RoSaaS` system will invoke these endpoints in response to specific events. Additionally, `external systems` can also consume the existing endpoints provided by the `RoSaaS` system, thereby enabling them to leverage the capabilities and features `RoSaaS` system offer. Adherence to the outlined guidelines is crucial to ensuring smooth communication and achieving effective integration.

## External Systems Implementing Endpoints

### Overview

> In this section, `external systems` are required to implement designated endpoints to facilitate seamless communication between our systems. These endpoints will be invoked by `RoSaaS` system in response to specific events, enabling the exchange of information.

### Integration Guidelines

> `External systems` should implement these endpoints within the tenancy management service as custom HTTP requests (Webhooks), defined by you as the product's owner. These endpoints are triggered by events that occur on a product's tenant, such as tenant creation, activation, or deactivation. When such events occur, the `RoSaaS` system sends an HTTP request to the URI specified in the `RoSaaS` Control Panel. This mechanism ensures timely and accurate data exchange between `RoSaaS` system and `external systems`.

1. **Creation - POST Method:**  
   Upon tenant creation, the RoSaaS system automatically sends an HTTP request to the external system along with the new tenant's uninqu name. This request prompts the external system to construct and activate the required tenant resources.
2. **Activation - POST Method:**  
   When RoSaaS's admin updates the status of a tenant to "activating", the RoSaaS system automatically sends an HTTP request to the external system along with the tenant's uninqu name. The external system then proceeds to activate the tenant's resources.
3. **Deactivation - POST Method:**  
   When RoSaaS's admin updates the status of a tenant to "deactivating", the RoSaaS system automatically sends an HTTP request to the external system along with the tenant's uninqu name. The external system then proceeds to deactivate the tenant's resources.
4. **Deletion - POST Method:**  
   When RoSaaS's admin updates the status of a tenant to "deleting", the RoSaaS system automatically sends an HTTP request to the external system along with the tenant's uninqu name. The external system then proceeds to delete the tenant's resources.
5. **Unavailable (Tenant is Down) - POST Method:**  
   The RoSaaS system automatically and periodically checks the availability (health status) of tenants. When the RoSaaS system detects that a tenant is unavailable, it sends an HTTP request to the external system along with the tenant's uninqu name to inform it that the tenant is down/unavailable.
6. **Health Check - GET Method:**  
   The RoSaaS system automatically and periodically checks the availability (health status) of tenants. The RoSaaS System checks the health status of a product’s tenants by sending an HTTP request to a default Health Check URL for the product’s tenants.

### Implementation Guidelines

#### 1\. HTTP Response Consistency

All implemented endpoints must consistently return an HTTP status code of 200 upon successful request execution. This status code indicates that the request was successfully processed by our system.

#### 2\. Security and Authentication

For enhanced security, all endpoints must be protected using an API key. External systems must include this API key in the `Authorization` header of every request. Failing to provide a valid API key will result in a 401 response, indicating unauthorized access.

#### 3\. Endpoint Type and Request Format

Each POST request must include a JSON request body with the following structure:

```json
{
  "tenantName": "string"
}
```

The `tenantName` parameter represents the unique identifier of the tenant associated with the specific event.

### Example Request

```
POST /api/integration/event-endpoint HTTP/1.1
Host: your-system.com
Content-Type: application/json
api-key:{your-api-key}
{
  "tenantName": "example-tenant"
}

```

#### 4\. **Health Check**

When implementing this endpoint, please consider the following instructions:

- All the previous instructions must be adhered to when implementing this endpoint.
- The GET request must Include a parameter in the route named "`name`" with the following structure:

```markup
{Host}/api/integration/{name}/health-status

```

The `tenant-5` is unique name of the tenant that represents the `name` parameter.

### Example Request

```markdown
GET /api/integration/tenant-5/health-status HTTP/1.1
Host: {your-system.com}
api-key:{your-api-key}
```

## Consuming Existing Endpoints

### Introduction

In this section, `external systems` can cunsume `ROSAS` system's existing endpoints to benefit from its capabilities and features. These endpoints offer a user-friendly way to interact with core system functionalities and are designed with robust error handling and a consistent response structure.

### ROSAS API Overview

> `ROSAS API` offers a user-friendly approach for engaging with the core features of our system. All endpoints are meticulously crafted with robust error handling and adhere to a consistent response structure. This ensures a unified and informative experience for users, resulting in smooth interactions and clear, easily responses.

### Authentication and Access

> All endpoints are secure and require proper authentication. You'll need to include an access token in your request header. If your authentication is missing or incorrect, you'll receive a `401` response, indicating unauthorized access to the requested endpoint.

### Response Structure

> Each endpoint, regardless of the request's outcome, adheres to a well-defined response structure that promotes clarity and predictability. This structure consists of two primary components: the '`data`' object and the '`metadata`' object.

- **data (When Applicable)**: When an endpoint returns response data, it is enclosed within the 'data' object, which is presented as a JSON object.
- **metadata**: Contains descriptive information about the response, providing a general overview of the response.

### Response Scenarios

1. **Success with response data:**

```json
{
  "data": {
    "property": "value",
    "property-2": true,
    "property-3": 123
  },
  "metadata": {
    "errors": [],
    "success": true
  }
}
```

1. **Success without response data:**

```json
{
  "metadata": {
    "errors": [],
    "success": true
  }
}
```

1. **Error Response (400 Bad Request):**

```json
{
  "metadata": {
    "errors": [
      {
        "message": "This Resource does not exist or may be deleted or You don't                         have access",
        "sysCode": "1005",
        "parameter": ""
      }
    ],
    "success": false
  }
}
```

### Authentication

In this section, you will learn how to authenticate your External System with ROSAS, ensuring secure access to privileged endpoints.

#### `POST` Generate Client Access Token for External System

> This endpoint is used by `External System` to generate an access token required for authentication in various protected endpoints across the API. The access token serves as a secure authorization mechanism for accessing privileged resources.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#ef205d12-d344-40d7-9a68-2f70c4d52d48:~:text=POST-,Generate%20client%20access%20token%20for%20external%20system,-Tenant)

### Tenant Management

Tenant management is crucial for providing customized experiences within the ROSAS platform. This section covers various operations related to tenant management.

#### `POST` Create Tenant

> This endpoint is used to create a new tenant.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#7cb49b06-b3ec-4082-b68a-483c86ed521a)

#### `POST` Create Super Admin

> This endpoint is used to create a new super admin for the ROSAS System.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#12dadcec-6eda-4757-adc3-2a30102b08bc)

#### `POST` Send Creation Request

> This endpoint is used by External System to inform the ROSAS System that the tenant's resources have been successfully created and activated.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#fc1d9b59-47ce-40f2-b6e3-1f21a71d0b05)

#### `POST` Send Activation Request

> This endpoint is used by External System to inform the ROSAS System that the tenant's resources have been successfully created and activated.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#2d70c3c3-2931-495b-8a3e-cf43efb64075)

#### `POST` Send Deactivation Request

> This endpoint is used by External System to inform the ROSAS System that the tenant's resources have been successfully created and activated.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#92d4894f-78a1-4446-8de1-58b5336f9f19)

#### `GET` Get All Tenants

> This endpoint empowers the external system to inquire about the status of all tenants.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#bb5bd4c9-025f-4c44-afca-f126d4335b03)

#### `GET` Get Tenant

> This endpoint empowers the external system to inquire about the status of a specified tenant by utilizing the tenant's name as a parameter.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#7722ebca-f4ec-4924-9973-43bc990dab10)

#### `POST` Set the tenant as Created

> This endpoint is used by External System to inform the ROSAS System that the tenant's resources have been successfully created and activated.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#32ff1914-34ea-4ede-84f9-270dc8538d66)

#### `POST` Set the tenant as Active

> This endpoint is used by External System to inform the ROSAS System that the tenant's resources have been successfully activated.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#22cd5b5a-d25f-46bc-aebf-e269c508cf90)

#### `POST` Set the tenant as Inactive

> This endpoint is used by External System to inform the ROSAS System that the tenant's resources have been successfully deactivated.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#9889166a-44f3-4e71-b1fd-3ddf1a046dc4)

#### `POST` Set the tenant as Failure

> This endpoint is used by External System to inform the ROSAS System that the tenant's resources have been successfully deactivated.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#7e35aef0-b96d-4f9e-9b0f-b21d94a5a9e8)

#### `POST` Set the tenant as Deleted

> This endpoint is used by External System to inform the ROSAS System that the tenant's resources have been successfully deleted.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#3eb0b8b1-4039-4f2f-85ac-4bca496e27a4)

#### `POST` Upsert Tenant's Metadata

> This endpoint allows the external system to store custom metadata associated with the product's tenant.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#4270e972-f885-4e2c-88e2-4dd163b1a986)

#### `GET` Get Tenant's Status

> This endpoint empowers the external system to inquire about the status of a specified tenant by utilizing the tenant's name as a parameter.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#c8e9ebe6-4c0c-4268-bd59-ccb596c95da6)

#### `GET` Get Tenant's Metadata

> Via this endpoint, the external system obtains the capability to access descriptive data (metadata) linked to a designated tenant.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#0745158a-893a-411c-9556-9c045d7ad2e9)

#### `POST` Set Subscription As Upgrade Applied Done

> This endpoint is used by External System to inform the ROSAS System that the tenant's resources have been successfully deactivated.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#edf0022d-4ff4-4a51-a19f-166ed409174d)

### Plans

#### `GET` Get Plans List

> This endpoint empowers the external system to inquire about the status of a specified tenant by utilizing the tenant's name as a parameter.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#54a8d011-0ee0-4e52-8bec-e751589187da)

### Specifications

#### `GET` Get Specifications List

> This endpoint empowers the external system to inquire about the status of a specified tenant by utilizing the tenant's name as a parameter.
> [Details and Example](https://documenter.getpostman.com/view/24180102/2s9Xy5MAYE#b106ddf0-d42e-48b6-9c5b-571140566c6b)
