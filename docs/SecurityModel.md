# Security Model

## Overview

The Online Training Management Platform (OTMP) uses Salesforce security features to ensure users can access only the data required for their role.


## Organization-Wide Defaults (OWD)

| Object | Default Access |
|--------|----------------|
| Student | Private |
| Trainer | Public Read Only |
| Course | Public Read Only |
| Batch | Public Read Only |
| Enrollment | Private |
| Payment | Private |


## Role Hierarchy

The following roles are configured:

- System Administrator
- Student Support
- Trainer
- Finance Team


## Profiles

The following profiles are used:

- System Administrator
- Standard User


## Permission Sets

Permission Set:

- Online Training Management Platform Application

Purpose:

- Provides access to OTMP custom objects.
- Grants permissions to use OTMP features.


## Sharing Rules

Examples:

- Share Course records with Trainers.
- Share Enrollment records with Student Support users.



## Field-Level Security

Sensitive fields are protected.

Examples:

- Payment Amount
- Transaction ID
- Student Personal Information

These fields are visible only to authorized users.

---

## Summary

The OTMP security model uses Organization-Wide Defaults, Role Hierarchy, Profiles, Permission Sets, Sharing Rules, and Field-Level Security to provide secure access to Salesforce data.
