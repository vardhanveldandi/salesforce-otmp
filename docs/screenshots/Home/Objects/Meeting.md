## Meetings

### Purpose

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
