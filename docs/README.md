# 🎓 Online Training Management Platform (OTMP)

## Project Overview

The **Online Training Management Platform (OTMP)** is a Salesforce-based application designed to manage online training operations. The platform centralizes student management, course management, batch scheduling, trainer management, enrollments, payments, customer support, and AI-powered student assistance.

## Problem Statement

Training organizations often manage student information, course schedules, enrollments, payments, and support requests across multiple manual processes. OTMP centralizes these operations on Salesforce to improve efficiency, data visibility, automation, and customer support.

## Business Goals

* Centralize training management operations
* Simplify student enrollment and course management
* Track batches, trainers, enrollments, and payments
* Automate repetitive business processes
* Improve customer support using Case Management and Omni-Channel
* Provide AI-powered student assistance using Agentforce
* Provide business insights through Reports and Dashboards

## Key Features

* Student Management
* Course Management
* Trainer Management
* Batch Management
* Enrollment Management
* Payment Management
* Session/Meeting Management
* Case Management
* Email Notifications
* Omni-Channel Support
* Reports & Dashboards
* Agentforce AI
* Prompt Builder

## Salesforce Architecture

The application uses Salesforce capabilities including:

* Sales Cloud
* Service Cloud
* Experience Cloud
* Salesforce Flow
* Reports & Dashboards
* Case Management
* Omni-Channel
* Agentforce
* Prompt Builder

## Custom Objects

The OTMP data model includes:

* Student
* Trainer
* Course
* Batch
* Enrollment
* Payment
* Session/Meeting

These objects are connected through relationships to support training operations and business processes.

## Security Model

The security model uses Salesforce access-control features including:

* Organization-Wide Defaults (OWD)
* Role Hierarchy
* Profiles
* Permission Sets
* Sharing Rules
* Field-Level Security
* Record-Level Access

## Automation

Business processes are automated using **Salesforce Flow**.

Examples include:

* Payment → Enrollment Automation
* Enrollment → Batch Strength Update
* Enrollment Confirmation Email
* Get Batch Details Flow
* Get Enrollment Details Flow
* Get Payment Details Flow
* Get Trainer Details Flow

## Reports & Dashboards

The project includes reports and dashboards for monitoring business operations and AI activity.

Examples include:

* OTMP Enrollment Report
* Payments Revenue Report
* Batch and Trainer Reports
* AI Interaction Reports
* AI Analytics Dashboard
* OTMP Enrollment Dashboard
* OTMP Payment Revenue Dashboard
* Executive OTMP Dashboard

## Case Management & Omni-Channel

The Service Cloud implementation includes:

* Case Management
* Case Record Types
* Queues
* Case Assignment Rules
* Service Channel
* Routing Configurations
* Presence Statuses
* Omni-Channel

These capabilities support routing customer and student support cases to appropriate support queues and users.

## Agentforce AI

The project includes an **OTMP Student Support Agent** with specialized support capabilities.

### Subagents

* Payment Support
* Enrollment Support
* Batch Schedule Support
* Trainer Support

### AI Actions

Agentforce uses Salesforce Flow-based actions to retrieve information such as:

* Enrollment Details
* Payment Details
* Batch Details
* Trainer Details

AI interactions are tracked using the **AI Interaction** custom object.

## Prompt Builder

Prompt Builder is used to create reusable AI prompt templates.

Examples include:

* Student Welcome Email
* Payment Fee Reminder
* Batch Performance Summary

Prompt templates use Salesforce record information to generate context-aware responses.

## Salesforce Metadata

Salesforce metadata and configuration documentation is maintained in this `docs` folder.

Detailed documentation includes:

* Custom Objects
* Fields
* Relationships
* Flows
* Permission Sets
* Page Layouts
* Applications
* Other Salesforce Configuration

See the individual documentation files in this folder for detailed configuration information.

## Screenshots

Salesforce configuration screenshots are available in the [`screenshots`](../screenshots/) folder.

Screenshots cover areas such as:

* Objects
* Page Layouts
* Flows
* Reports
* Dashboards
* Security
* Omni-Channel
* Agentforce

## Architecture Diagrams

Architecture and process diagrams are available in the [`diagrams`](../diagrams/) folder.

The diagrams include:

* System Architecture
* Data Model / ER Diagram
* Security Model
* Automation Flow
* AI Workflow
* Omni-Channel Routing

## Installation / Setup Overview

To explore or reproduce the project:

1. Create or use a Salesforce Developer Org.
2. Configure the required Salesforce objects and fields.
3. Configure security and permissions.
4. Configure automation and Flow.
5. Configure Reports and Dashboards.
6. Configure Case Management and Omni-Channel.
7. Configure Agentforce and Prompt Builder.
8. Test the application functionality.

## Future Enhancements

Potential future improvements include:

* Enhanced AI capabilities
* Data Cloud integration
* Additional analytics
* External collaboration integrations
* Mobile application support

## Author

**Vardhan Veldandi**

Salesforce Administrator | Agentforce AI Specialist
