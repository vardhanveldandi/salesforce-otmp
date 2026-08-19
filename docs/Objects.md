# Salesforce Custom Objects

This document describes the custom objects used in the Online Training Management Platform (OTMP).


## Overview

The OTMP project uses custom objects to manage students, trainers, courses, enrollments, payments, and meetings



# Student Object

## Purpose

Stores information about students enrolled in training programs.

## Fields
| Field Name | Data Type | Description |
|------------|-----------|-------------|
| Student Name | Text | Name of the student |
| Date of Birth | Date | Student DOB |
|  Student Email | Email | Student email address |
| Phone Number | Phone | Student contact number |
| Status | Picklist | Active or Inactive |
| Skill Level | Picklist | Basic , competent, Skilled and mastered |
|  Highest Qualification| Picklist | Graduate , Post graduate, and Diploma |


## Relationships

- One Student can have multiple Enrollments.



# Course Object

## Purpose

Stores training course details.

# Fields
 
|             Field Name                    |           Data Type             |           Description                |
|-------------------------------------------|---------------------------------|--------------------------------------|   
|            Course Name                    |            Text                 |        Name of the course            |
|            Course Description             |         Long Text area          |        Course Description            |            
|            Course Fee                     |            Number               |        Course Fee                    |
|            Course Duration                |            Picklist             |        Course duration               |    
|            Difficulty                     |            Picklist             |   Beginner, Intermediate, Advanced   |
|            Location                       |            Text                 |        Location                      |
|            Platform                       |            Picklist             |   Platform of course like Zoom etc.. |              
|            Course URL                     |            URL                  |      Url of platform course          |



### Relationships

- One Course can have multiple Batches.

# Trainer Object

## Purpose

Stores trainer information, professional details, contact information, employment details, and payment information for trainers in the OTMP platform.

## Fields

| **Field Name**       | **Data Type**       | **Description**                                           |
| -------------------- | ------------------- | --------------------------------------------------------- |
| Trainer Name         | Text(80)            | Name of the trainer                                       |
| Trainer Email        | Email               | Email address of the trainer                              |
| Trainer Phone Number | Phone               | Contact number of the trainer                             |
| Employee ID          | Text(20)            | Unique employee identification number                     |
| Department           | Picklist            | Department associated with the trainer                    |
| Experience           | Picklist            | Trainer experience level                                  |
| Expertise            | Text(200)           | Trainer expertise or specialization                       |
| Payment Rate         | Number(18,0)        | Payment rate for the trainer                              |
| Vendor Name          | Text(50)            | Name of the associated vendor                             |


## Relationships

* Trainer can be assigned to multiple **Batches**.
* Trainer can be linked to multiple **Meetings**.
* **Batch** is linked to Trainer.
* **Meeting** is linked to Trainer.

# Batch Object

## Purpose

Stores batch information.

### Fields

| Field Name        | Data Type               | Description                                   |
|------------       |-----------              |-------------                                  |
| Batch Name        | Text                    | Batch name                                    |
| Start Date        | Date                    | Batch start date                              |
| End Date          | Date                    | Batch end date                                |
| Capacity          | Number                  | Maximum number of students                    |
| Course            | Master Detailed         | This Relationship is belongs to Batch Object. |
| Trainer           | Lookup                  | This Relationship is belongs to Batch Object. |
| Status            | Picklist                | Active or Inactive                            |
| Available seats   | Number                  | Available seats in Batch                      |
| Time Slot         | Picklist                | Time slots of Batch                           |


### Relationships

- Linked to Course
- Linked to Trainer
- Linked to Enrollment



# Enrollment Object

## Purpose

Tracks student enrollments.

### Fields

| Field Name          | Data Type | Description |
|------------         |-----------|-------------|
|Enrollment|Text|Name of the enrollment|
|Enrollment Date     | Date | Enrollment date |
| Enrollment Status | Picklist | Enrolled, Dropped, Completed |
| Payment Status | Picklist | Paid , Pending and completed |
|Student email|Formula|Email of the student.|
|Course Name|Lookup|This Relationship is belongs to Enrollment Object.|
|Student|Master-Detailed|This Relationship is belongs to Enrollment Object.|
|Meeting |Lookup|This Relationship is belongs to Enrollment Object.|

### Relationships

- Linked to Student
- Linked to Batch and Course



# Meetings Object

## Purpose

Stores training meeting/session details.

### Fields

| Field Name | Data Type | Description |
|------------|-----------|-------------|
| Meeting Name | Text | Name of the Meeting |
| Meeting Date | Date | Meeting date |
| Meeting Link | URL | Online meeting URL |
| Active | Checkbox | Checked or unchecked |
| Student mail on meeting | Email | Email of student |
| Trainer | Master-Detailed |This relationship is belongs to Meeting Object.|
| Batch | Master-Detailed |This relationship is belongs to Meeting Object.|


### Relationships

- Linked to Batch and Trainer



# Payment Object

## Purpose

Stores payment details.

### Fields

| Field Name | Data Type | Description |
|------------|-----------|-------------|
| Payment Name | Text | Name of the payment  |
| Payment Date | Date | Date of payment |
| Payment Status | Picklist | Paid, Pending and completed |
| Payment Amount | Number | Payment amount |
| Payment Method | Picklist | Upi. Net banking , Debit card and credit card |
| Transaction ID | Text | Payment transaction reference |
| Student | Master-Detailed | This relationship is belongs to Payment object |
| Course | Master-Detailed | This relationship is belongs to Payment object |
| Batch | Lookup| This relationship is belongs to Payment object |
| Enrollment | Lookup | This relationship is belongs to Payment object |
| Pending Amount | Number | Pending amount |
| Due Date | Date | Due Date of payment |
| Installment Number | Number | No.of installed numbers |

### Relationships

- Linked to Enrollment
- Linked to Student
- Linked to Course
- Linked to Batch




