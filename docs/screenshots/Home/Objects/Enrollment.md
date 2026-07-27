## Enrollment

### Purpose

Tracks student enrollments.

### Fields

| Field Name          | Data Type | Description |
|------------         |-----------|-------------|
|Enrollment|Text|Name of the enrollment|
| Enrollment Date     | Date | Enrollment date |
| Enrollment Status | Picklist | Enrolled, Dropped, Completed |
| Payment Status | Picklist | Paid , Pending and completed |
|Student email|Formula|Email of the student.|
|Course Name|Lookup|This Relationship is belongs to Enrollment Object.|
|Student|Master-Detailed|This Relationship is belongs to Enrollment Object.|
|Meeting |Lookup|This Relationship is belongs to Enrollment Object.|

### Relationships

- Linked to Student
- Linked to Batch
