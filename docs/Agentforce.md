# Agentforce AI Documentation

## Overview

The Online Training Management Platform (OTMP) uses Salesforce Agentforce AI to automatically assist students by answering questions, retrieving Salesforce data, and providing personalized responses.

## Agent Name

## OTMP Student Support Agent

### Purpose

The OTMP Student Support Agent is an AI-powered virtual assistant that helps students by answering enrollment, batch, payment, and trainer-related queries. It automatically identifies the student's intent and executes the appropriate action to retrieve accurate information from Salesforce.

### Features

- Handles student support requests automatically
- Identifies user intent
- Invokes Salesforce Flows
- Uses Prompt Templates for natural responses
- Supports multiple specialized subagents
- Logs AI interactions for analytics and reporting

## Subagents

## 1. Enrollment Support

### Purpose

Handles student enrollment-related queries.

### Prompt Template

Enrollment Support Template

### Flow Action

Get Enrollment Details Flow

### Capabilities

- Retrieves course details
- Retrieves batch information
- Displays batch schedule
- Retrieves assigned trainer details
- Displays trainer experience and expertise
- Retrieves enrollment status
- Retrieves payment amount and pending balance
- Displays payment status
- Shows student satisfaction score
- Displays payment due date

## 2. Payment Type Support Subagent

### Purpose

Handles student payment-related queries.

### Prompt Template

Payment Support Template

### Flow Action

Get Payment Status Flow

### Capabilities

- Retrieves payment amount
- Displays pending payment amount
- Retrieves payment status
- Displays payment due date
- Confirms completed or pending payments

## 3. Trainer Support Subagent

### Purpose

Provides students with trainer-related information.

### Prompt Template

Trainer Support Template

### Flow Action

Get Trainer Details Flow

### Capabilities

- Retrieves trainer name
- Displays trainer experience
- Shows trainer expertise
- Retrieves trainer contact information
- Provides trainer details for the assigned batch

## 4. Batch Schedule Support Subagent

### Purpose

Provides students with batch schedule and timing information.

### Prompt Template

Batch Support Template

### Flow Action

Get Batch Details Flow

### Capabilities

- Retrieves batch name
- Displays batch time slot
- Shows assigned trainer
- Retrieves batch status
- Provides batch schedule details

## AI Flow

Student asks a question 
        │
        ▼
OTMP Student Support Agent receives the request
        │
        ▼
Agent identifies the user's intent
        │
        ▼
Routes the request to the appropriate subagent
        │
        ▼
Subagent executes the required Salesforce Flow
        │
        ▼
Flow retrieves data from Salesforce Objects
        │
        ▼
Prompt Template formats the response
        │
        ▼
Agent returns a natural language response
        │
        ▼
AI Interaction record is created for analytics

## AI Components

  Component	                                                                         Description
  ---------------------------------------------------------------------------------------------------------------------------
  AI Agent	                                                                  OTMP Student Support Agent
  Subagents                                                                 	Enrollment, Batch Schedule, Payment, Trainer
  Prompt Templates	                                                            4
  Salesforce Flows	                                                            4
  AI Interaction Object	                                                      Stores AI conversations
  
## Business Benefits

- Provides instant AI-powered student support.
- Reduces manual work for administrators.
- Retrieves real-time Salesforce data.
- Automates enrollment, payment, batch, and trainer queries.
- Improves response accuracy and consistency.
- Enhances student self-service experience.
- Reduces support ticket volume.
- Tracks AI interactions for reporting and analytics.
- Supports scalable student support using Agentforce AI.
