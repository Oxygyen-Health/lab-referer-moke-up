# Oxygen Lab Referral System - Project Requirements Document

## Project Overview
**Project Title:** Oxygen Lab Referral System  
**Owner:** Korle Bu Teaching Hospital – Central Laboratory  
**Date:** [Current Date]

## 1. Introduction

### 1.1 Purpose
The Oxygen Lab Referral System is designed to streamline the laboratory service request process for Korle Bu Teaching Hospital (KBTH) Central Laboratory. The platform enables individuals, hospitals, and lab service providers to:
- Request laboratory services
- Track request progress
- Process payments
- Request sample collection
- Schedule mobile lab services

### 1.2 Scope
The system encompasses:
- Account registration and verification
- Price checking and service availability
- Request creation and tracking
- Secure payment processing
- Sample collection and mobile lab scheduling
- KBTH admin portal for workflow management and reporting

## 2. System Overview

### User Roles and Features

| User Role | Key Features |
|-----------|--------------|
| Requester (Hospital/Individual/Lab) | Account creation, lab test selection, price checking, request creation, sample pick-up requests, payment, tracking reports |
| KBTH Central Lab Admin | Verification, request review, sample tracking, report upload, communication, payments reconciliation |
| Mobile Lab Team | View scheduled pickups, confirm collections, update status |
| Super Admin | Oversee platform performance, analytics, user management |

## 3. System Requirements

### 3.1 Functional Requirements

#### User Registration & Verification Workflow
- Account creation process
- Document verification system
- Role-based access control

#### Core Features
- Login & Role-Based Access
- Test Catalog & Pricing Display
- Test Request Form with Upload Options
- Request Tracker Dashboard
- Secure Payment Integration
- Notification System
- Mobile Lab Request Form
- Report Upload & Delivery
- Admin Panel for KBTH Lab Operations

### 3.2 Non-Functional Requirements

- **Scalability:** Handle high volume from multiple facilities
- **Availability:** 99.9% uptime
- **Security:** SSL encryption, access control, GDPR-compliant
- **Performance:** Sub-3 second page load
- **Data Storage:** Encrypted health data storage with backups
- **Localization:** Language and currency settings for Ghana

## 4. Architecture Design

### 4.1 System Components

- **Frontend:** Web-based (mobile responsive), React or Vue.js
- **Backend:** Node.js / Django / Laravel (API driven)
- **Database:** PostgreSQL or MongoDB
- **Authentication:** OAuth2 + 2FA (for admin users)
- **Hosting:** AWS / Azure / GCP
- **SMS/Email:** Twilio or Africa's Talking / SendGrid
- **Payment:** Integration with Flutterwave, Paystack or Hubtel
- **Audit Logging:** All system actions must be logged

## 5. User Journey

### 5.1 Facility/Individual
1. Sign up → Complete profile → Wait for KBTH verification
2. Log in → Search test → View price → Submit request
3. Choose: send sample / request sample pick-up / mobile lab
4. Make payment → Track request → Download report

### 5.2 KBTH Central Lab
1. Verify account requests
2. Receive and assign new test requests
3. Coordinate with mobile lab or sample pickup team
4. Upload results → Mark request as completed
5. Generate financial and operational reports

## 6. System Modules

| Module | Description |
|--------|-------------|
| User Account & Verification | Sign-up form, document upload, KBTH admin verification dashboard |
| Service Catalog | Browseable list of lab services, searchable, with prices |
| Request Management | Form for creating lab requests; includes urgency, notes, upload prescriptions |
| Sample Logistics | Scheduler for mobile lab or pick-up request with location, date, time |
| Payment Gateway | Integration for mobile money/card payments with receipts |
| Results Management | Upload portal for lab results; PDF auto-generation |
| Notifications | Real-time status updates via SMS/email for every key milestone |
| Admin Dashboard | Request tracker, analytics, user verification, reporting tools |
| Audit & Logs | All actions are timestamped and logged for traceability |

## 7. Integration Points

- SMS/Email Services – For request and report notifications
- Payments – Flutterwave, Hubtel or Paystack for collections
- GIS API – For mapping pickup locations
- EMR/HMIS (Optional) – Integrate with KBTH's medical record system

## 8. Security & Privacy

- Encrypted database (at-rest and in-transit)
- Role-based access control
- GDPR/HIPAA-aligned consent and data protection
- Audit trail for user actions
- Backup and disaster recovery protocol

## 9. Testing Plan

- Unit Testing – Core modules individually
- Integration Testing – Payment, notification, login
- UAT (User Acceptance Testing) – With hospitals and KBTH team
- Security Testing – Penetration testing, access control validation
- Performance Testing – Simulate high request volume

## 10. Deployment & Maintenance

- **Deployment:** Staging & production environments
- **Monitoring:** Real-time monitoring of errors and user activity
- **Maintenance:** Monthly updates, bug fixes, and feature improvements
- **Training:** Manuals and videos for end users and lab staff

## 11. Milestones & Timeline

| Milestone | Expected Date |
|-----------|---------------|
| Requirements Gathering | Week 1 |
| Design & Wireframes | Week 2 |
| Backend Development | Week 3–5 |
| Frontend Development | Week 5–7 |
| Integrations | Week 8 |
| Testing & QA | Week 9 |
| UAT with Facilities | Week 10 |
| Launch & Training | Week 11 |
| Support Phase Begins | Week 12+ |

## 12. Documentation & Training Materials

- System Manual for Admins
- Quick Start Guide for Facilities
- Video Tutorials for Request Submission & Payment
- SOPs for KBTH Lab Teams (Verification, Sample Handling, Report Management)

## 13. Post-Deployment Support

- Helpdesk System (email/chat/call)
- SLA for response times
- Feedback collection and implementation process 