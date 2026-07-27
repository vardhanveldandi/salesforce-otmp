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
| Payment Method | Picklist | Upi. Net banking , Debit card and credit card |
| Transaction ID | Text | Payment transaction reference |
| Student | Master-Detailed | This relationship is belongs to Payment object |
| Course | Master-Detailed | This relationship is belongs to Payment object |
| Batch | Lookup| This relationship is belongs to Payment object |
| Enrollment | Lookup | This relationship is belongs to Payment object |
| Pending Amount | Number | Pending amount |
| Due Date | Date | Due Date of payment |
| Installement Number | Number | No.of installed numbers |

### Relationships

- Linked to Enrollment
- Linked to Student
- Linked to Course
- Linked to Batch
