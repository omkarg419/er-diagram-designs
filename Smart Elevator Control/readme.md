# 🏢 LiftGrid Smart Elevator Control System ER Diagram

This ER diagram models a scalable infrastructure management system used by LiftGrid Systems to control and monitor elevators across large commercial buildings such as corporate towers, malls, airports, hospitals, and residential complexes.

---

## 📌 Key Features

- Multi-building support
- Multiple elevators per building
- Floor-level request tracking
- Intelligent ride assignment to elevators
- Real-time elevator status monitoring
- Maintenance tracking without overwriting history
- Ride logging for analytics and performance tracking
- Support for high-frequency real-time requests

---

## 🧩 Entities Included

- **Buildings** – Stores building-level information
- **Floors** – Represents floors within each building
- **Elevator Shafts** – Physical shafts containing elevators
- **Elevators** – Core elevator units
- **Elevator-Floor Map** – Maps which elevators serve which floors
- **Floor Requests** – Requests generated from floors
- **Ride Assignments** – Assigns requests to elevators
- **Ride Logs** – Tracks completed elevator trips
- **Elevator Status** – Tracks real-time status (Idle, Moving, Maintenance)
- **Maintenance Records** – Tracks maintenance history

---

## 🔗 Relationships Overview

- One **Building** contains many **Floors**
- One **Building** contains many **Elevators**
- One **Shaft** contains one **Elevator**
- One **Elevator** serves multiple **Floors**
- One **Floor** can be served by multiple **Elevators**
- One **Request** is assigned to one **Elevator**
- One **Elevator** completes many **Rides**
- One **Elevator** has multiple **Status updates**
- One **Elevator** has multiple **Maintenance records**

---

## ⚙️ Design Highlights

- **Separation of static and dynamic data**
  - Static: Buildings, Floors, Elevators
  - Dynamic: Requests, Assignments, Ride Logs

- **Central Flow**
  - Floor Request → Ride Assignment → Ride Log

- **Many-to-Many Relationship**
  - Elevator ↔ Floor handled via junction table

- **Independent Status Tracking**
  - Elevator status is not mixed with configuration

- **Maintenance History Preserved**
  - Stored separately to avoid overwriting