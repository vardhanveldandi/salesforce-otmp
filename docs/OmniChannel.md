OTMP — Omni-Channel Case Routing
1. Overview
The Online Training Management Platform (OTMP) uses Salesforce Case Management and Omni-Channel to support automated student issue routing.
Target Flow
Student
  ↓
Create Case
  ↓
Case Assignment Rule
  ↓
Support Queue
  ↓
Service Channel
  ↓
Routing Configuration
  ↓
Omni-Channel
  ↓
AgentWork
  ↓
Support Agent
  ↓
Case Resolved
Implementation note: The configuration was implemented through Omni-Channel, but AgentWork → Support Agent was not successfully validated in the current Salesforce Developer Edition environment. Public Service Routing was also not fully validated.

2. Business Objective
OTMP supports:
Enrollment issues
Payment issues
Course issues
Trainer issues
Certificate issues
Technical issues
The objective is to place Cases into the correct support queue and, in a fully supported environment, automatically deliver available work to the appropriate support agent.

3. Salesforce Components
Component
Purpose
Status
Case
Stores student support requests
Configured
Case Record Types
Classifies support issues
Configured
Case Assignment Rule
Assigns Cases to queues
Configured
Support Queues
Organizes support work
Configured
Service Channel
Makes Cases routable
Configured
Routing Configuration
Controls routing behavior
Configured
Presence Status
Defines agent availability
Configured
Presence Configuration
Defines agent capacity
Configured
Omni-Channel Utility
Displays routing/work status
Configured
AgentWork
Represents routed work
Not generated as expected
Public Service Routing
Additional routing capability
Not fully validated


4. Case Record Types
Configured Case Record Types:
Enrollment Issue
Payment Issue
Course Issue
Trainer Issue
Certificate Issue
These classifications can be used to determine the appropriate support queue.

5. Support Queues
Queue
Responsibility
Enrollment Support
Enrollment-related Cases
Payment Support
Payment-related Cases
Trainer Support
Trainer-related Cases
Technical Support
Technical issues
OTMP Support Queue
General OTMP support


6. Case Assignment Rule
The Assignment Rule determines the initial Case owner/queue.
Example configuration
Rule: OTMP Case Assignment Rule
Criteria: Case Status = New
Assignment: OTMP Support Queue
Important distinction
Assignment Rule
      ↓
Determines Case Owner / Queue
      ↓
Omni-Channel
      ↓
Routes eligible work to an available agent
Assignment Rules and Omni-Channel perform different responsibilities.

7. Service Channel
Service Channel: Case Support
Purpose: identifies Cases as work items that can be routed through Omni-Channel.
Case
  ↓
Case Support Service Channel

8. Routing Configuration
Routing Configuration: OTMP Case Routing
Setting
Value
Priority
1
Routing Model
Most Available
Capacity
10

The configuration controls how eligible work is distributed to available agents.

9. Presence Configuration
Presence Configuration: OTMP Support Configuration
Setting
Value
Capacity
10
Profile
System Administrator
User
OTMP Support Agent

The capacity controls how much Omni-Channel work the agent can receive.

10. Presence Status
Configured statuses:
Available — Online and available for Case Support
Busy — Online but not available for additional work
Offline — Offline
Expected behavior:
Agent = Available
       ↓
Eligible for Omni-Channel work

11. Omni-Channel Utility
The Omni-Channel utility was added to the Service Console.
It is intended to allow agents to:
View availability
Set status to Available
Receive routed work
Accept work
Work on Cases
Change availability
Expected agent flow:
Login
  ↓
Service Console
  ↓
Omni-Channel Utility
  ↓
Status = Available
  ↓
Receive Routed Work

12. End-to-End Process
Step 1 — Create Case
Example:
Subject: Payment Issue
Status: New
Type: Payment Issue
Step 2 — Assignment Rule
Case Status = New
       ↓
OTMP Support Queue
Step 3 — Queue
The Case is placed in the configured support queue.
Step 4 — Omni-Channel
The Case becomes eligible for routing through the configured Service Channel and Routing Configuration.
Step 5 — Agent Availability
The support agent sets the Omni-Channel status to Available.
Step 6 — Expected AgentWork
Case
  ↓
Omni-Channel
  ↓
AgentWork
  ↓
Support Agent
Step 7 — Case Resolution
New
 ↓
Working
 ↓
Resolved

13. Actual OTMP Testing Result
The following were successfully configured:
Case
Case Record Types
Case Assignment Rules
Support Queues
Service Channel
Routing Configuration
Presence Configuration
Presence Status
Omni-Channel Utility
Limitation
During end-to-end testing:
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

14. Validation Checklist
Test
Expected Result
OTMP Result
Create Case
Case created
Passed
Assignment Rule
Case assigned to queue
Configured
Queue
Case available in queue
Configured
Service Channel
Case routable
Configured
Routing Configuration
Routing available
Configured
Presence Status
Agent can become available
Configured
Omni Utility
Utility available
Passed
AgentWork
Work item generated
Not generated as expected
Agent receives Case
Case delivered to agent
Not fully validated
Case Resolution
Case can be resolved
Manual lifecycle available


15. Troubleshooting Performed
The following areas were reviewed:
Omni-Channel
Omni-Channel enabled
Service Channel configured
Routing Configuration configured
Presence Status configured
Presence Configuration configured
Omni-Channel utility available
Queue
Support queues created
Required users associated with queues
Queues configured for Case routing
Case Assignment
Assignment Rule created
Criteria configured
Queue selected as assignment target
Agent Availability
Available Presence Status configured for Case Support
Presence Configuration assigned
Omni-Channel utility available in the console
AgentWork
Expected:
Case
 ↓
Queue
 ↓
Omni-Channel
 ↓
AgentWork
 ↓
Agent
Observed: AgentWork was not generated as expected.

16. OTMP Example — Payment Issue
Student
  ↓
Payment Issue Case
  ↓
Status = New
  ↓
Case Assignment Rule
  ↓
Payment Support Queue
  ↓
Case Support Service Channel
  ↓
Payment Routing Configuration
  ↓
Omni-Channel
  ↓
AgentWork          ← Not fully validated
  ↓
Payment Support Agent
  ↓
Case Resolved
The queue/routing foundation was configured; the final AgentWork-to-agent stage remains environment-limited.

17. Business Benefits
Automatic Work Distribution — Reduces manual Case assignment.
Reduced Response Time — Makes eligible work available to agents.
Queue-Based Support — Separates support by issue type.
Capacity Management — Controls agent workload.
Centralized Service Console — Provides a single workspace for support.
Scalable Architecture — Supports future routing enhancements.

18. Production-Ready Target
In a Salesforce environment supporting the required routing capabilities, the target flow is:
Create Case
  ↓
Assignment Rule
  ↓
Support Queue
  ↓
Service Channel
  ↓
Routing Configuration
  ↓
Omni-Channel
  ↓
AgentWork Created
  ↓
Agent Receives Work
  ↓
Agent Accepts Work
  ↓
Case Worked
  ↓
Case Resolved
Future enhancements may include:
Skills-Based Routing
Priority-based routing
Multiple specialized queues
Agent capacity management
Automated Case escalation
Supervisor monitoring
Omni-Channel reporting
SLA-based routing
Advanced routing flows

19. Project Status
Overall Status: Partially Implemented / Environment-Limited
Implemented
Case
 ↓
Assignment Rule
 ↓
Support Queue
 ↓
Service Channel
 ↓
Routing Configuration
 ↓
Presence Configuration
 ↓
Presence Status
 ↓
Omni-Channel Utility
Not Fully Validated
Omni-Channel
 ↓
AgentWork
 ↓
Support Agent
The limitation is documented intentionally so the GitHub project accurately represents what was implemented and what could not be validated in the current Developer Edition environment.

20. Summary
OTMP establishes the Salesforce Omni-Channel foundation for automated student Case routing.
The implemented solution demonstrates:
Case management
Queue-based assignment
Service Channel configuration
Routing Configuration
Agent presence management
Omni-Channel console integration
The AgentWork → Support Agent stage was not claimed as completed because the expected AgentWork records were not generated during testing in the current environment.
