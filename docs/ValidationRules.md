# Validation Rules

## Overview

This document describes the Validation Rules implemented in the Online Training Management Platform (OTMP) to maintain data quality and prevent invalid records


# 1. Payment Amount Validation

## Purpose

Ensures that the payment amount is greater than zero. Ensures that the Payment Amount entered by the user is greater than zero, preventing invalid or negative payment values from being saved.

## Rule

  ## Rule Name:

  Payment_Amount_Validation

  ## Validation Formula:

  Payment_Amount__c <= 0 

  ## Error Message:

  Payment Amount must be greater than zero.

  ## Error Location:

  Payment Amount Field

## Business Benefit

- Prevents invalid payment records.

# 2. DOB_Past_Date_Validation

## Purpose

Ensures that the Date of Birth (DOB) entered for a student is a valid date in the past, preventing users from entering today's date or a future date.

## Rule

   ## Rule Name:
 
   DOB_Past_Date_Validation

   ## Validation Formula:

   Date_of_Birth__c >= TODAY() 

   ## Error Message:

   Date of Birth must be a past date.

   ## Error Location:

   Date of Birth Field
   
## Business Benefits

- Prevents invalid future birth dates.
- Ensures accurate student demographic information.
- Improves the reliability of student records.
- Reduces data entry errors during student registration.
- Maintains high-quality and consistent student data across the OTMP application.

# 3. Phone_Number_10_Digits_Validation

## Purpose

Ensures that every student phone number contains exactly 10 digits, preventing users from saving incomplete or invalid contact numbers.

## Rule

   ## Rule Name:

   Phone_Number_10_Digits_Validation

   ## Validation Formula:
 
   NOT( REGEX( Phone_Number__c , "^[0-9]{10}$") )

  Note: If your Phone field allows special characters such as spaces, hyphens, or brackets, you may need a more advanced formula. The above formula works well    when users enter only numeric digits.

   ## Error Message:

   Phone Number must contain exactly 10 digits.

   ## Error Location:

   Phone Number Field

   
## Business Benefits

- Ensures valid and standardized student contact numbers.
- Improves communication with students through calls and SMS.
- Reduces errors caused by incomplete or incorrect phone numbers.
- Improves the accuracy of student contact information.
- Maintains consistent data quality across the OTMP application.

# 4.Start_Date_Less_Than_End_Date Validation

## Purpose

Ensures that the Batch End Date is always later than the Batch Start Date, preventing users from creating batches with invalid date ranges.

## Rule

  ## Rule Name:
 
  Start_Date_Less_Than_End_Date

  ## Validation Formula:

  Start_Date__c >= End_Date__c

  ## Error Message:

  End Date must be later than the Start Date.

  ## Error Location:

  End Date Field

## Business Benefits

- Prevents users from creating invalid batch schedules.
- Ensures accurate training duration and planning.
- Improves the reliability of enrollment and batch management processes.
- Reduces manual errors in scheduling.
- Maintains high-quality and consistent data across the OTMP application.

# 5. Course_Duration_Positive Validation

## Purpose

Ensures that the Course Duration is greater than zero, preventing users from creating courses with invalid or zero durations.

## Rule

  ## Rule Name:

  Course_Duration_Positive

  ## Validation Formula:

  OR(
   ISPICKVAL( Course_Duration__c , "0 months"),
   ISPICKVAL( Course_Duration__c , "None")
  )
  
  ## Error Message:

  Course Duration must be greater than zero.

  ## Error Location:
 
  Course Duration Field

##  Business Benefits

- Prevents invalid course duration values.
- Ensures every course has a meaningful training period.
- Improves the accuracy of course scheduling and planning.
- Reduces data entry mistakes.
- Maintains consistent and reliable course information.
  
# 6. Course_Fee_Limit_Check Validation

## Purpose

Ensures that the Course Fee falls within the organization's allowed fee range, preventing users from entering unrealistic or invalid course fees.

## Rule

  ## Rule Name:

  Course_Fee_Limit_Check

  ## Validation Formula
  
  Course_Fee__c > 100000

  ## Error Message:

  Course Fee must be greater than 0 and less than or equal to ₹100,000.

  ## Error Location:

  Course Fee Field

## Business Benefits

- Prevents invalid or unrealistic course fees.
- Ensures pricing follows organizational policies.
- Improves the accuracy of financial and revenue reports.
- Reduces manual pricing errors.
- Maintains consistent course pricing across the OTMP application.




