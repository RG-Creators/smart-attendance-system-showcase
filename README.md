# Smart Attendance System SaaS — Multi-Tenant Workforce & Academic Attendance Platform

[![PHP Version](https://img.shields.io/badge/PHP-8.2%2B-777bb4?style=for-the-badge&logo=php&logoColor=white)](https://php.net)
[![Architecture](https://img.shields.io/badge/Architecture-Multi--Tenant%20SaaS-0052CC?style=for-the-badge)](https://github.com/RG-Creators)
[![Database](https://img.shields.io/badge/MySQL-8.0%2B-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://mysql.com)
[![Status](https://img.shields.io/badge/Build-Production%20Hardened-success?style=for-the-badge)](https://github.com/RG-Creators)

> **Public Showcase Repository**: This repository provides high-level architectural documentation, system capabilities, and workflow specifications for the **Smart Attendance System SaaS**. Full underlying source code and proprietary subscription modules are held securely in a private production repository.

---

## 🏗️ System Architecture & Multi-Tenant Model

The Smart Attendance System is engineered with an isolated multi-tenant architecture designed to handle dual business verticals simultaneously without structural collisions:

```
+-------------------------------------------------------------------------------+
|                       SUPER ADMIN GOVERNANCE ENGINE                           |
|       - Global Tenant Provisioning & Health Telemetry                         |
|       - Tiered Subscription Plan Management (Basic / Pro / Enterprise)        |
+-------------------------------------------------------------------------------+
                                        |
                 +----------------------+----------------------+
                 |                                             |
                 v                                             v
+----------------------------------+          +----------------------------------+
|    TRACK 1: ACADEMIC INSTITUTION |          |   TRACK 2: CORPORATE MULTI-OFFICE|
|  - Multi-Grade Class & Section   |          |  - Multi-Branch Geofencing       |
|  - Subject-Teacher Matrix        |          |  - Shift & Break Calculations    |
|  - Student Daily & Subject Logs  |          |  - Employee Real-Time Clock-in   |
|  - Teacher Attendance Verification|         |  - Receptionist Kiosk Mode       |
+----------------------------------+          +----------------------------------+
                 |                                             |
                 +----------------------+----------------------+
                                        |
                                        v
+-------------------------------------------------------------------------------+
|                         UNIFIED REPORTING & ANALYTICS                         |
|   - Consolidated Attendance Percentages & Leave Analytics                     |
|   - Automated Deficiency Alerts & Summary Reports                             |
+-------------------------------------------------------------------------------+
```

---

## ⚡ Flagship Enterprise Capabilities

### 1. Dual-Track Tenant Segmentation
- **Academic Institutions (Schools, Colleges, Universities)**: Structured hierarchical mapping from Classes to Sections, Class-Subject associations, and period-by-period attendance with teacher substitution support.
- **Corporate Offices & Enterprises**: Multi-branch office management (`office_branches`), customizable shift timings (`office_timings`), configurable break limits (`break_times`), and employee status monitoring.

### 2. Multi-Role RBAC Authorization
- **Super Administrator**: Complete tenant provisioning, access codes, subscription lifecycle control, and system audits.
- **Tenant Administrator**: Organization branding, department setup, staff enrollment, and summarized data export.
- **Receptionist / Kiosk Mode**: Secure terminal interface for rapid QR or manual clock-in with zero admin privilege exposure.
- **Staff / Teachers**: Self-service schedule views, personal attendance history, and department roll-call inputs.

### 3. Hardened Security & Isolation
- **Tenant Partitioning**: Relational foreign-key boundaries ensuring organizations can never access neighboring tenant data.
- **Zero SQL Injection**: 100% prepared SQL statements with strict parameter binding.
- **Environment Isolation**: Cryptographic access tokens and secrets isolated via environment configuration (`vlucas/phpdotenv`).

---

## 🛠️ Tech Stack

- **Backend Platform**: Core PHP 8.2+ (Modular Domain Model, PDO Prepared Statements, Session Protection)
- **Frontend Layer**: Responsive Glassmorphism Design System, CSS3 Grid, Bootstrap, FontAwesome 6
- **Database Architecture**: MySQL 8.0+ / 9.0 (20+ Normalized Relational Tables with Composite B-Tree Indexes)
- **Dependency Management**: Composer (PHP Dotenv)

---

## 🔒 Proprietary Code Notice
The complete source code, proprietary algorithms, and deployment automation for this platform are privately maintained. For commercial licensing, enterprise white-labeling, or architectural inquiries, please contact:
- **Developer**: RG
- **Email**: [rgcreatorsofficial@gmail.com](mailto:rgcreatorsofficial@gmail.com)
- **Portfolio**: [rgcreators.netlify.app](https://rgcreators.netlify.app/)
