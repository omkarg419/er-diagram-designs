# Clinic Appointment and Diagnostics Platform

This ER diagram models a modern clinic management system designed to handle patient appointments, doctor consultations, diagnostic testing, report generation, and payment processing in a structured and scalable way.

---

## Key Features

- Clear distinction between appointment booking and actual consultation (visit)
- Support for multiple doctors across different specializations
- Patient appointment scheduling with status tracking (Booked, Cancelled, Completed, No-show)
- Consultation records capturing diagnosis and doctor notes
- Diagnostic test prescription during consultations
- Report generation linked to both consultation and test
- Payment tracking associated with patient appointments
- Structured handling of many-to-many relationship between consultations and tests

---

## Includes

- **Patient** and **Doctor** entities for managing clinic users  
- **Appointment** entity for scheduling visits  
- **Consultation** entity representing actual doctor-patient interaction  
- **Test** entity for diagnostic services  
- **Consultation_Test** junction table for handling multiple tests per consultation  
- **Report** entity for storing diagnostic results  
- **Payment** entity for handling billing and transactions  
- Proper cardinality (1:1, 1:M, M:N relationships)  
- Junction table implementation for normalization  
