# OTMP Page Layouts

## Overview

The Online Training Management Platform (OTMP) uses customized Salesforce Page Layouts to provide different record views based on business requirements.

Page Layouts control:

- Field visibility
- Field positioning
- Required fields
- Sections
- Buttons
- Quick Actions
- Related Lists
- Record-specific user experience


# 1. Student Page Layouts

## Corporate Student

The Corporate Student Page Layout is designed for students associated with corporate training programs.

### Configuration

- Student information
- Contact information
- Corporate-related information
- Enrollment details
- Payment information
- Relevant related lists


## Regular Student

The Regular Student Page Layout is designed for students participating in standard individual training programs.

### Configuration

- Student information
- Contact information
- Course-related information
- Enrollment details
- Payment information
- Relevant related lists



# 2. Course Page Layouts

## Online Course

The Online Course Page Layout is used for courses delivered through online training.

### Configuration

- Course information
- Duration
- Difficulty
- Fee
- Online delivery information
- Related batches
- Related enrollments



## Offline Course

The Offline Course Page Layout is used for classroom-based training programs.

### Configuration

- Course information
- Duration
- Difficulty
- Fee
- Classroom/training information
- Related batches
- Related enrollments



## Hybrid Course

The Hybrid Course Page Layout is used for courses combining online and offline training.

### Configuration

- Course information
- Duration
- Difficulty
- Fee
- Online delivery information
- Offline/classroom information
- Related batches
- Related enrollments


# 3. Trainer Page Layouts

## Internal Trainer

The Internal Trainer Page Layout is used for trainers who belong to the organization.

### Configuration

- Trainer information
- Contact information
- Expertise
- Training assignments
- Related batches


## External Trainer

The External Trainer Page Layout is used for trainers working with OTMP as external resources.

### Configuration

- Trainer information
- Contact information
- Expertise
- External trainer details
- Training assignments
- Related batches

# 4. Enrollment Page Layouts

## Direct Enrollment

The Direct Enrollment Page Layout is used when a student directly enrolls in a training program.

### Configuration

- Student
- Course
- Batch
- Enrollment Status
- Payment Status
- Enrollment information



## Corporate Enrollment

The Corporate Enrollment Page Layout is used for enrollments managed through corporate training programs.

### Configuration

- Student
- Corporate information
- Course
- Batch
- Enrollment Status
- Payment Status


# 5. Payment Page Layouts

## Full Payment

The Full Payment Page Layout is used when the complete course fee is paid in a single payment.

### Configuration

- Payment information
- Enrollment
- Payment Amount
- Payment Date
- Payment Status
- Payment method



## Installment Payment

The Installment Payment Page Layout is used when course fees are paid in multiple installments.

### Configuration

- Payment information
- Enrollment
- Installment amount
- Payment Date
- Payment Status
- Payment method
- Installment details



# 6. Meeting Page Layouts

## Training Session

The Training Session Page Layout is used for scheduled training sessions.

### Configuration

- Session information
- Course
- Batch
- Trainer
- Session date/time
- Session details



## Demo Session

The Demo Session Page Layout is used for demonstration or introductory sessions.

### Configuration

- Session information
- Course
- Trainer
- Session date/time
- Demo details


# 7. Batch Page Layouts

## Weekday Batch

The Weekday Batch Page Layout is used for training batches conducted during weekdays.

### Configuration

- Batch information
- Course
- Trainer
- Start Date
- End Date
- Capacity
- Weekday schedule
- Related enrollments


## Weekend Batch

The Weekend Batch Page Layout is used for training batches conducted during weekends.

### Configuration

- Batch information
- Course
- Trainer
- Start Date
- End Date
- Capacity
- Weekend schedule
- Related enrollments



# Page Layout Summary

| Object | Page Layout | Purpose |
|---|---|---|
| Student | Corporate Student | Corporate training students |
| Student | Regular Student | Individual training students |
| Course | Online Course | Online training |
| Course | Offline Course | Classroom training |
| Course | Hybrid Course | Online + offline training |
| Trainer | Internal Trainer | Organization trainers |
| Trainer | External Trainer | External trainers |
| Enrollment | Direct Enrollment | Individual enrollment |
| Enrollment | Corporate Enrollment | Corporate enrollment |
| Payment | Full Payment | Single full payment |
| Payment | Installment Payment | Multiple payments |
| Meeting | Training Session | Training sessions |
| Meeting | Demo Session | Demo sessions |
| Batch | Weekday Batch | Weekday training |
| Batch | Weekend Batch | Weekend training |
