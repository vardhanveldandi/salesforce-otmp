# Salesforce Flow Documentation

## Overview

This document describes the Salesforce Flows used in the Online Training Management Platform (OTMP).

The flows automate business processes, reduce manual work, and improve data accuracy.


# Payment Automation Flow --*

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
4. Mark the enrollment as Active.
5. Send a payment confirmation email.

## Outcome

- Enrollment becomes Active.
- Student receives a confirmation email.



# Enrollment Flow

## Purpose

Automates the student enrollment process.

## Type

Record-Triggered Flow

## Trigger

Runs when an Enrollment record is created.

## Process

1. Validate enrollment details.
2. Link the Student to the selected Batch.
3. Update the Batch strength.
4. Notify the student.

## Outcome

- Enrollment is completed successfully.
- Batch count is updated.



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
