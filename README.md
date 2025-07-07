# oracle-ebs-lookup-guide
Guide to creating user-defined lookups in Oracle EBS

# Oracle E-Business Suite (EBS) – Lookup Creation Guide

This repository contains a step-by-step guide to creating **custom lookups** in **Oracle EBS** using the Application Developer responsibility.

## 📘 Document Included

- **Oracle_EBS_Lookup_Creation_Guide.docx**  
  A comprehensive manual explaining how to create user-defined lookups, define lookup codes, and validate them using SQL queries.

## 🧭 Covered Topics

- What is a Lookup in Oracle EBS?
- Lookup Types vs. Lookup Codes
- Example: `VEHICLE_TYPE` with sample codes like CAR, BIKE, TRUCK
- SQL query to validate lookup values
- Benefits of using lookups in Oracle EBS
- Types of Lookups: System, User, Extensible

## 🧰 Tools & Navigation

- **Oracle EBS Navigation Path:**  
  `Application Developer` → `Application` → `Lookup` → `Custom`
- SQL Validation Query (to run in backend)

```sql
SELECT * FROM fnd_lookup_values 
WHERE lookup_type = 'VEHICLE_TYPE'
  AND enabled_flag = 'Y'
  AND SYSDATE BETWEEN start_date_active AND NVL(end_date_active, SYSDATE);
🧩 Lookup Structure
Element	Description
Lookup Type	Category or grouping (e.g., ORDER_STATUS)
Lookup Code	Internal stored value (e.g., OPEN, CLOSED)
Meaning	User-visible label (e.g., Open, Closed)
Description	Optional detail

📂 File Structure

📦oracle-ebs-lookup-guide
 ┣ 📄 README.md
 ┣ 📄 Oracle_EBS_Lookup_Creation_Guide.docx
🧑‍💻 Author
Perarul Selvan R
📧 perarulselvan34@gmail.com
