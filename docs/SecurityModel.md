# Security Model

## Overview

The Online Training Management Platform (OTMP) uses Salesforce security features to ensure users can access only the data required for their role.


## Organization-Wide Defaults (OWD)

| Object | Default Access |
|--------|----------------|
| Student | Public, Read/Write |
| Trainer | Public Read Only |
| Course | Private |
| Batch | Controlled by Parent |
| Enrollment | Controlled by Parent  |
| Payment |  Controlled by Parent |


## Role Hierarchy

The following roles are configured:

 Wipro
│
├── Admin
│   ├── Student 
│   ├── Trainer
│          ├── Support
│
├── CEO





### Purpose

- **Wipro** – Top-level organizational role.
- **Admin** – Manages Salesforce configuration, users, security, and application setup.
- **CEO** – Executive-level role with access to organizational data.


## Profiles

The following profiles are used:

- System Administrator
- Trainer Profile
- Support Profile


## Permission Sets

Permission Set:

- Online Training Management Platform Application

Purpose:

- Provides access to OTMP custom objects.
- Grants permissions to use OTMP features.


## Sharing Rules

Examples:

- Share Course records with Trainers.



## Field-Level Security

Sensitive fields are protected.

Examples:

- Payment Amount
- Student Personal Information

These fields are visible only to authorized users.


## Summary

The OTMP security model uses Organization-Wide Defaults, Role Hierarchy, Profiles, Permission Sets, Sharing Rules, and Field-Level Security to provide secure access to Salesforce data.
