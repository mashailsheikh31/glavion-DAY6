# Enterprise Attendance & Supervisor Portal v6.0

## Intern Profile
* **Intern Name:** Mashail Abdul Khaliq
* **Role:** Web Development Intern
* **Organization:** Glavion Solutions

## Project Overview
An enterprise-grade, multi-role web application featuring real-time attendance tracking, leave applications, interactive supervisor approval workflows, client-side data analytics, and responsive dark mode support. Version 6.0 transitions the system to a production-ready Supabase backend with robust Role-Based Access Control (RBAC), Row-Level Security (RLS), and database-level data integrity constraints.

---

## Access Credentials
* **Admin Portal Account:** `admin@gmail.com`
* **Role Management:** Handled via Supabase Auth `user_metadata` (`admin` / `intern`).

---

## Day-by-Day Architecture Breakdown

### Day 01 & Day 02: Core Foundations
* **Real-time Digital Clock:** Live time tracking and session state initialization.
* **Responsive Layout:** Mobile drawer navigation with backdrop overlays.
* **Attendance Metrics:** Dynamic calculation for Present, Late, and Absent statuses.

### Day 03: Feature Expansions
* **Search & Filter Engine:** Multi-condition filtering by date range and attendance status.
* **Leave Module:** Real-time leave request submission and dynamic balance adjustment.
* **Client-Side CSV Export:** RFC 4180-compliant CSV report generation using the Browser Blob API.
* **Theme Customization:** Persistent dark mode toggle leveraging CSS variables and local persistence.

### Day 04: Capstone Front-End Integration
* **Visual Analytics:** Custom SVG/CSS progress indicators and weekly attendance trend bar charts.
* **Toast Notification Engine:** Real-time feedback banners for user interactions.
* **Profile Management:** Profile editor modal for user information updates.

### Day 05 & Day 06: Supabase Cloud Integration & Security Architecture
* **Supabase Authentication & Metadata:** Integrated cloud authentication using JWT sessions, linking user identities via `user_id` (UUID foreign key) across all relational tables.
* **Role-Based Navigation Isolation (`enforceRouteGuard`):** Client-side and server-side navigation security that restricts non-admin roles from accessing `admin.html` and automatically hides/removes administrative DOM elements for Intern accounts.
* **Database Schema Integrity:** Enforced database-level constraints using SQL `UNIQUE(user_id, date)` paired with JavaScript check-in logic to eliminate duplicate check-ins.
* **Cloud Attendance & Leave Engine:** Replaced local mock storage with Supabase SQL queries supporting `upsert` operations for check-in/check-out lifecycle management and real-time status updates for supervisor approvals.

---

## Git Push Mandate
All source code files, SQL migration scripts, and frontend assets are committed directly as raw source code without compressed `.zip` archives.