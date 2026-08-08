# Omni-Channel Documentation

## Overview

The Online Training Management Platform (OTMP) uses Salesforce Omni-Channel to automatically route student support cases to the appropriate support team.

## Queues

The following support queues are configured:

- Enrollment Support Queue
- Payment Support Queue
- Trainer Support Queue
- Technical Support Queue
- Course Support Queue

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

- Configuration Name: OTMP Case Routing
- Routing Model: Most Available
- Priority: 1
- Capacity: 10

### Purpose:
Routes incoming cases to the most available support agent.

## Case Assignment Rules

- Rule Name: OTMP Case Assignment

### Logic:

- Enrollment Issue → Enrollment Queue
- Payment Issue → Payment Queue
- Trainer Issue → Trainer Queue
- Technical Issue → Technical Queue
- Course Issue → Certificate Queue

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
