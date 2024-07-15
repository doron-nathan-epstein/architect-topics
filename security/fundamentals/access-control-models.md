# Learning Guide: Access Control Models (RBAC, ABAC)

- [Learning Guide: Access Control Models (RBAC, ABAC)](#learning-guide-access-control-models-rbac-abac)
  - [Introduction](#introduction)
  - [Key Concepts](#key-concepts)
  - [Access Control Models](#access-control-models)
    - [Role-Based Access Control (RBAC)](#role-based-access-control-rbac)
    - [Attribute-Based Access Control (ABAC)](#attribute-based-access-control-abac)
  - [Comparison](#comparison)
  - [Examples](#examples)
    - [RBAC Example](#rbac-example)
    - [ABAC Example](#abac-example)
  - [Summary](#summary)

## Introduction

Access control models define how permissions are granted to users or entities within a system. Effective access control ensures that sensitive resources are protected from unauthorized access.

## Key Concepts

- **Access Control**: The process of limiting access to resources based on policies.
- **Permissions**: Rights assigned to users or roles that define what actions can be performed.
- **User Roles**: Categories assigned to users that determine their access level.

## Access Control Models

### Role-Based Access Control (RBAC)

RBAC is a model that assigns permissions based on roles within an organization. Users are assigned roles, and each role has specific permissions associated with it.

### Attribute-Based Access Control (ABAC)

ABAC uses attributes (user attributes, resource attributes, and environment conditions) to determine access permissions. This model provides more fine-grained control compared to RBAC.

## Comparison

| **Aspect**             | **RBAC**                                          | **ABAC**                                        |
|------------------------|--------------------------------------------------|-------------------------------------------------|
| **Flexibility**        | Less flexible; relies on predefined roles        | More flexible; uses attributes for access decisions |
| **Complexity**         | Simpler to implement and manage                   | More complex due to attribute evaluation         |
| **Scalability**        | Scales well with a limited number of roles       | Scales well with a larger number of attributes   |
| **Use Cases**          | Common in enterprise applications                 | Suitable for dynamic environments with diverse conditions |

## Examples

### RBAC Example

In an e-commerce application, roles might include "Admin," "Customer," and "Guest." Each role has different permissions:

- **Admin**: Can manage products, view sales reports.
- **Customer**: Can view and purchase products.
- **Guest**: Can browse products but not make purchases.

```csharp
public class User
{
    public string Username { get; set; }
    public string Role { get; set; }
}

public bool CanManageProducts(User user)
{
    return user.Role == "Admin";
}
```

### ABAC Example

In a healthcare application, access might be granted based on user attributes (e.g., role, department) and resource attributes (e.g., document type, sensitivity level).

```csharp
public bool CanAccessDocument(User user, Document document)
{
    return user.Role == "Doctor" && document.SensitivityLevel == "Confidential";
}
```

## Summary

Access control models like RBAC and ABAC play a vital role in securing applications by ensuring that users can only access resources they are authorized to. RBAC is suitable for simpler applications with defined roles, while ABAC provides a more dynamic and flexible approach for complex environments. Understanding these models helps in implementing robust security measures in software applications.
