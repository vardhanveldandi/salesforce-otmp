# Salesforce Flow Documentation

## Overview

This document describes the Salesforce Flows used in the Online Training Management Platform (OTMP).

The flows automate business processes, reduce manual work, and improve data accuracy.


# Payment - Enrollment Automation Flow 

## Purpose

Automatically updates the enrollment after a payment is successfully recorded. 
## Type

Record-Triggered Flow

## Trigger

Runs when a Payment record is created or updated. 

## Process

1. Check the payment status.
2. Verify the payment amount.
3. Update the related Enrollment record.
4. Mark the enrollment as enrolled


## Outcome

- Enrollment becomes Enrolled



# Enrollment Confirmation Email Automation Flow *

## Purpose

 Automatically sends a confirmation email to the student after a successful enrollment.

## Type

Record-Triggered Flow

## Trigger

Executes when an Enrollment record is created or updated and the Enrollment Status changes to Confirmed (or Active, depending on your implementation).

## Process

1. Identify the email template.
2. Populate student information about enrolled course and batch details 
3. Send the email.

## Outcome

Students receive automated email notifications.



# Enrollment Update Batch Strength Automation Flow *

## Purpose

Automatically updates the number of enrolled students (Batch Strength) whenever an enrollment is created, updated, or cancelled.

## Type

Record-Triggered Flow

## Trigger

Executes when an Enrollment record is created, updated, or deleted (depending on your implementation).

## Process

1. Count enrolled students.
2. Update Batch capacity.
3. Check availability.
4. Update Batch status if full.

## Outcome

Batch information stays up to date.


# Get Trainer Details flow

## Purpose

Retrieves trainer information from the Trainer object and returns the details to Agentforce or another automation so students can quickly access trainer information without manual searching.

## Type

Autolaunched Flow

## Trigger

Triggered when an Agentforce action or another Salesforce Flow invokes the Get Trainer Details flow and passes the required input variables (such as Trainer Name or Student ID).

## Process

1. Receive the input variables (Agent Name, Student ID, Trainer Name).
2. Create an AI Interaction record for logging the request.
3. Search the Trainer object using Get Records.
4. Retrieve the trainer details (Phone Number, Expertise, Experience, etc.).
5. Store the retrieved values in output variables using the Assignment element.
6. Return the output variables to Agentforce or the calling flow.


## Outcome

The flow successfully returns the trainer's information (Phone Number, Expertise, Experience, etc.) to Agentforce or another automation, enabling the AI assistant to answer trainer-related queries while maintaining an AI interaction log.


# Get payment status Flow 

## Purpose

Retrieves the payment details of a student from the Payment object and returns the information to Agentforce or another Salesforce automation without requiring users to manually search for payment records.

## Type

Autolaunched Flow

## Trigger

Triggered when an Agentforce Action or another Flow calls the Get Payment Status Flow and passes the required input variable (Student ID).

## Process

1. Receive the input variables (Agent Name and Student ID).
2. Create an AI Interaction record to log the user's request.
3. Search the Payment object using Get Records based on the Student ID.
4. Retrieve the payment details (Payment Status, Payment Amount, Pending Amount, Due Date).
5. Store the retrieved values in output variables using the Assignment element.
6. Return the output variables to Agentforce or the calling Flow.

## Outcome

The flow returns the student's payment information (Payment Status, Payment Amount, Pending Amount, and Due Date) so Agentforce or another automation can display accurate payment details to the user.


# Get Enrollment Details Flow 

## Purpose

Retrieves a student's enrollment details from the Enrollment object and returns the information to Agentforce or another Salesforce automation without requiring users to manually search for enrollment records.

## Type

Autolaunched Flow

## Trigger

Triggered when an Agentforce Action or another Salesforce Flow calls the Get Enrollment Details Flow and passes the required input variable (Student ID or Enrollment ID).

## Process

1. Receive the input variables (Agent Name and Student ID/Enrollment ID).
2. Create an AI Interaction record to log the request.
3. Search the Enrollment object using Get Records.
4. Retrieve the enrollment details (Course Name, Batch, Enrollment Status, Payment Status, Enrollment Date, etc.).
5. Store the retrieved values in output variables using the Assignment element.
6. Return the output variables to Agentforce or the calling Flow.

## Outcome

The flow returns the student's enrollment information (Course Name, Batch, Enrollment Status, Payment Status, Enrollment Date, etc.) so Agentforce or another automation can provide accurate enrollment details to the user.


# Get Batch Details Flow 

## Purpose
Retrieves batch information from the Batch object and returns the details to Agentforce or another Salesforce automation, enabling users to view batch schedules and related information without manually searching Salesforce records.

## Type

Autolaunched Flow

## Trigger

Triggered when an Agentforce Action or another Salesforce Flow calls the Get Batch Details Flow and passes the required input variable (Batch ID, Batch Name, or Student ID).

## Process

1. Receive the input variables (Agent Name and Batch ID/Student ID).
2. Create an AI Interaction record to log the user's request.
3. Search the Batch object using Get Records.
4. Retrieve the batch details (Batch Name, Course, Trainer, Start Date, End Date, Schedule/Time Slot, Capacity, Available Seats, etc.).
5. Store the retrieved values in output variables using the Assignment element.
6. Return the output variables to Agentforce or the calling Flow.

## Outcome

The flow returns the batch information (Batch Name, Course, Trainer, Start Date, End Date, Schedule, Capacity, etc.) so Agentforce or another automation can provide accurate batch details to the user.




