## Payment

### Purpose

Stores payment details.

### Fields

| Field Name | Data Type | Description |
|------------|-----------|-------------|
| Payment Name | Text | Name of the payment  |
| Payment Date | Date | Date of payment |
| Payment Status | Picklist | Paid, Pending and completed |
| Payment Amount | Number | Payment amount |
| Transaction ID | Text | Payment transaction reference |
| Student | Master-Detailed | This relationship is belongs to Payment object |
| Course | Master-Detailed | This relationship is belongs to Payment object |
| Batch | Lookup| This relationship is belongs to Payment object |
| Enrollment | Lookup | This relationship is belongs to Payment object |

### Relationships

- Linked to Enrollment
- Linked to Student
- Linked to Course
- Linked to Batch
