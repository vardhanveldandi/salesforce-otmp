## Batch

### Purpose

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


### Relationships

- Linked to Course
- Linked to Trainer
- Linked to Enrollment
