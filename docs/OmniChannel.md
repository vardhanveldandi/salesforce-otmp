# Omni-Channel Documentation

## Overview

The Online Training Management Platform (OTMP) uses Salesforce Omni-Channel to automatically route student support cases to the appropriate support team.

## Service Channel

- Name: Case Support
- Object: Case
- Capacity Model: Status-Based
- Routing Configuration: OTMP Case Routing

### Purpose: 
Identifies Cases as work items that can be routed through Omni-Channel.

## Queues

The following support queues are configured:

- OTMP Enrollment Support Queue
- OTMP Course Support Queue
- OTMP Payment Support Queue
- OTMP Trainer Support Queue
- OTMP Technical Support Queue

### Purpose:
Automatically group cases based on the issue type.

## Presence Status

Configured Presence Statuses:

- Available
- Busy
- Offline

### Purpose:

Allows agents to control their availability for receiving work.

## Routing Configuration

### RC-1
- Configuration Name: OTMP Case Routing
- Routing Model: Most Available
- Priority: 1
- Capacity: 10

### RC-2 
- Configuration Name: Course Routing
- Routing Model: Most Available
- Priority: 1
- Capacity: 10

### RC-3
- Configuration Name: Enrollment Routing
- Routing Model: Most Available
- Priority: 1
- Capacity: 10

### RC-4
- Configuration Name: Payment Routing
- Routing Model: Most Available
- Priority: 1
- Capacity: 10

### RC-5
- Configuration Name: Trainer Routing
- Routing Model: Most Available
- Priority: 1
- Capacity: 10

### RC-6
- Configuration Name: Technical Routing
- Routing Model: Most Available
- Priority: 1
- Capacity: 10

### Purpose of RC :
Routes incoming cases to the most available support agent.

### Presence Configuration

Capacity:
10

Assigned User:
System Administrator

## Case Assignment Rules

- Rule Name: OTMP Case Routing

   - Active Assignment Rule details

   - All 5 Rule Entries :
   
     ### Logic:
     - Course Issue → OTMP Course Support Queue
     - Enrollment Issue → OTMP Enrollment Support Queue
     - Payment Issue → OTMP Payment Support Queue
     - Trainer Issue → OTMP Trainer Support Queue
     - Technical Issue → OTMP Technical Support Queue

## Actual OTMP Testing Result

The following Salesforce Omni-Channel components were successfully
configured:

- Case
- Case Record Types
- Case Assignment Rules
- Support Queues
- Service Channel
- Routing Configurations
- Presence Configuration
- Presence Statuses
- Omni-Channel Utility

### Successfully Validated

The following Case-routing portion was successfully tested:

Case Created
     ↓
Case Assignment Rule
     ↓
Support Queue
     ↓
Case Ownership

## During end-to-end testing:
Case Created
    ↓
Queue Assignment
    ↓
Omni-Channel Configuration
    ↓
Expected AgentWork
    ↓
Not Generated as Expected

Therefore, the complete AgentWork → Support Agent stage could not be validated.
Public Service Routing could not be fully completed/validated in the current environment.
So finally, it completes end-to-end flow remains partially validated.

## Routing Flow

Student submits a support request

↓

Case is created

↓

Case Assignment Rule evaluates the case

↓

Case is assigned to the appropriate Queue

↓

Omni-Channel routes the case

↓

Support Agent accepts the work

↓

Case is resolved

↓

Case status is updated to Closed

## Case Lifecycle

New

↓

Assigned

↓

In Progress

↓

On Hold (Optional)

↓

Resolved

↓

Closed

## Business Benefits

- Automatically routes support requests.
- Reduces manual case assignment.
- Improves response times.
- Balances workload among support agents.
- Improves customer satisfaction.
