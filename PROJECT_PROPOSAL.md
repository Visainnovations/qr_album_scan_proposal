# Project Proposal & Agreement

![Visainnovations](https://img.shields.io/badge/VISAINNOVATIONS-Make%20Tomorrow%20Magical✨-7c3aed?style=for-the-badge)

---

## QR Album Scan - Digital Photo Album Platform

**Prepared by:** Visainnovations  
**Date:** January 19, 2026  
**Version:** 2.0  
**Validity:** 30 Days

---

## Table of Contents

1. [Executive Summary](#1-executive-summary)
2. [Project Overview](#2-project-overview)
3. [Scope of Work](#3-scope-of-work)
4. [Technical Specifications](#4-technical-specifications)
5. [Team Structure](#5-team-structure)
6. [Project Timeline](#6-project-timeline)
7. [Cost Breakdown](#7-cost-breakdown)
8. [Payment Terms](#8-payment-terms)
9. [Deliverables](#9-deliverables)
10. [Terms & Conditions](#10-terms--conditions)
11. [Contact Information](#11-contact-information)

---

## 1. Executive Summary

**Visainnovations** is pleased to present this proposal for the development of **QR Album Scan**, a comprehensive digital photo album platform designed specifically for photo studios and lab administrators. This platform will enable labs to manage multiple studios, studios to create digital flip books with advanced image processing, generate QR codes for easy sharing, and manage their orders efficiently.

| Project | QR Album Scan |
|---------|---------------|
| **Client** | P. Manikandam |
| **Duration** | 55 Days |
| **Team Size** | 3 Members |
| **Total Cost** | ₹78,000 |

---

## 2. Project Overview

### 2.1 Problem Statement

Photo studios and labs face challenges in:
- Delivering digital albums to clients efficiently
- Managing multiple orders and bookings
- Providing modern digital viewing experience
- Sharing albums easily with clients
- Managing multiple studios under one lab
- Processing images from various sources (PDF, uploads)
- Calculating production costs for albums

### 2.2 Proposed Solution

A web-based platform that offers:
- **Digital Flip Book Viewer** - Interactive album viewing with page-flip animations
- **QR Code Generation** - Instant sharing via scannable QR codes with custom URLs
- **Studio Dashboard** - Complete order and booking management
- **Lab Admin Panel** - Multi-studio management with renewal tracking
- **Super Admin Panel** - Complete platform control (Labs + Studios + SMTP)
- **Advanced Image Processing** - Auto-crop, manual crop, PDF extraction
- **Email System** - SMTP integration for notifications and password recovery
- **Mobile Responsive** - Works seamlessly on all devices

### 2.3 Platform Hierarchy

```
┌─────────────────────────────────────────────────────────────────────────┐
│                         PLATFORM HIERARCHY                               │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│                       ┌─────────────────────┐                           │
│                       │     SUPER ADMIN     │                           │
│                       │   (Platform Owner)  │                           │
│                       │                     │                           │
│                       │ ✓ Manage ALL Labs   │                           │
│                       │ ✓ Manage ALL Studios│                           │
│                       │ ✓ Approval Control  │                           │
│                       │ ✓ Renewal Dates     │                           │
│                       │ ✓ SMTP Config       │                           │
│                       │ ✓ Platform Analytics│                           │
│                       └──────────┬──────────┘                           │
│                                  │                                      │
│                                  │ (Manages Both)                       │
│                 ┌────────────────┴────────────────┐                     │
│                 │                                 │                     │
│                 ▼                                 ▼                     │
│    ┌────────────────────────┐       ┌────────────────────────┐         │
│    │         LABS           │       │        STUDIOS         │         │
│    │                        │       │    (Independent)       │         │
│    │  Lab 1 ──┬── Studio A  │       │                        │         │
│    │          ├── Studio B  │       │  Studio X (No Lab)     │         │
│    │          └── Studio C  │       │  Studio Y (No Lab)     │         │
│    │                        │       │  Studio Z (No Lab)     │         │
│    │  Lab 2 ──┬── Studio D  │       │                        │         │
│    │          └── Studio E  │       │                        │         │
│    │                        │       │                        │         │
│    └────────────────────────┘       └────────────────────────┘         │
│                                                                         │
│    ┌────────────────────────────────────────────────────────────┐      │
│    │                      LAB ADMIN                              │      │
│    │  • Can manage ONLY studios under their own lab              │      │
│    │  • Can approve/set renewal for their studios only           │      │
│    │  • Cannot access other labs or independent studios          │      │
│    └────────────────────────────────────────────────────────────┘      │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

### 2.4 Super Admin Control Panel

```
┌─────────────────────────────────────────────────────────────────────────┐
│                      SUPER ADMIN DASHBOARD                               │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │  📊 OVERVIEW                                                     │   │
│  │  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐        │   │
│  │  │ Total    │  │ Total    │  │ Active   │  │ Total    │        │   │
│  │  │ Labs: 25 │  │Studios:150│ │Albums:2.5K│ │ Orders:8K│        │   │
│  │  └──────────┘  └──────────┘  └──────────┘  └──────────┘        │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
│  ┌─────────────────────────────┐  ┌─────────────────────────────┐     │
│  │  🏢 LAB MANAGEMENT          │  │  📷 STUDIO MANAGEMENT       │     │
│  │                             │  │                             │     │
│  │  • View All Labs            │  │  • View All Studios         │     │
│  │  • Approve/Reject Labs      │  │  • Approve/Reject Studios   │     │
│  │  • Set Lab Renewal Dates    │  │  • Set Studio Renewal Dates │     │
│  │  • Activate/Deactivate Labs │  │  • Activate/Deactivate      │     │
│  │  • View Lab Analytics       │  │  • Assign to Lab (optional) │     │
│  │  • Edit Lab Details         │  │  • View Studio Analytics    │     │
│  │                             │  │                             │     │
│  └─────────────────────────────┘  └─────────────────────────────┘     │
│                                                                         │
│  ┌─────────────────────────────┐  ┌─────────────────────────────┐     │
│  │  ⚙️ SMTP CONFIGURATION      │  │  📈 PLATFORM ANALYTICS      │     │
│  │                             │  │                             │     │
│  │  • SMTP Host & Port         │  │  • Total Revenue            │     │
│  │  • Email Credentials        │  │  • Orders by Status         │     │
│  │  • Test Email               │  │  • Top Performing Labs      │     │
│  │  • Email Templates          │  │  • Top Performing Studios   │     │
│  │                             │  │  • Growth Metrics           │     │
│  └─────────────────────────────┘  └─────────────────────────────┘     │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

### 2.5 Key Features

| Module | Features |
|--------|----------|
| **Public Website** | Home, Features, Pricing, Contact pages |
| **Studio Portal** | Dashboard, Orders (100 photos/album limit), Bookings, Image Cropping, Settings |
| **Lab Admin Portal** | Own Studio Management, Approval, Renewal Dates, Analytics |
| **Super Admin Panel** | ALL Labs + ALL Studios Management, Approval, Renewal, SMTP Config, Analytics |
| **Album Viewer** | Flip Book, Custom QR URLs, Background Music, Social Sharing |
| **Image Processing** | Auto-crop, Manual Crop Editor, PDF Upload & Extraction |

### 2.6 URL Structure

Custom short URL format for albums:
```
https://flip.io/{lab_id or studio_id}/{album_id}

Examples:
• https://flip.io/1/drfghdf7g0
• https://flip.io/25/abc1234xyz

- Lab/Studio ID: Numeric identifier
- Album ID: 10-character alphanumeric
```

### 2.7 Renewal Date Management Flow

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    RENEWAL DATE MANAGEMENT FLOW                          │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│  SUPER ADMIN (Full Control)                                             │
│  ═══════════════════════════                                            │
│                                                                         │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │                        MANAGE LABS                               │   │
│  │  ┌─────────────────────────────────────────────────────────┐    │   │
│  │  │ Lab: Creative Photo Labs                                 │    │   │
│  │  │ ───────────────────────────────────────────────────────  │    │   │
│  │  │ Status: ● Active                                         │    │   │
│  │  │ Start Date: 01-Jan-2026                                  │    │   │
│  │  │ End Date:   01-Jan-2027                                  │    │   │
│  │  │ Studios Under Lab: 12                                    │    │   │
│  │  │                                                          │    │   │
│  │  │ [✏️ Edit Dates] [⏸️ Deactivate] [🗑️ Delete]              │    │   │
│  │  └─────────────────────────────────────────────────────────┘    │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │                       MANAGE STUDIOS                             │   │
│  │  ┌─────────────────────────────────────────────────────────┐    │   │
│  │  │ Studio: Sunshine Photography                             │    │   │
│  │  │ ───────────────────────────────────────────────────────  │    │   │
│  │  │ Status: ● Active                                         │    │   │
│  │  │ Belongs to: Creative Photo Labs (or Independent)         │    │   │
│  │  │ Start Date: 15-Jan-2026                                  │    │   │
│  │  │ End Date:   15-Jan-2027                                  │    │   │
│  │  │ Total Albums: 45                                         │    │   │
│  │  │                                                          │    │   │
│  │  │ [✏️ Edit Dates] [⏸️ Deactivate] [🔄 Change Lab]          │    │   │
│  │  └─────────────────────────────────────────────────────────┘    │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
│  ═══════════════════════════════════════════════════════════════════   │
│                                                                         │
│  LAB ADMIN (Limited Control - Own Studios Only)                         │
│  ═════════════════════════════════════════════                          │
│                                                                         │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │ Can only see and manage studios under their own lab              │   │
│  │ • Approve/Reject studio registration                             │   │
│  │ • Set studio renewal dates                                       │   │
│  │ • View studio analytics                                          │   │
│  │ • Cannot access other labs or independent studios                │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
│  ═══════════════════════════════════════════════════════════════════   │
│                                                                         │
│  AUTO-DEACTIVATION LOGIC                                                │
│  ───────────────────────                                                │
│  • When Current Date > End Date → Access automatically blocked          │
│  • Admin extends End Date → Access automatically restored               │
│  • No manual intervention needed for activation/deactivation            │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Scope of Work

### 3.1 Included in Scope

#### Frontend Development (Core)
- ✅ Responsive public website (4 pages)
- ✅ Studio login & dashboard
- ✅ Lab Admin login & dashboard
- ✅ Super Admin login & dashboard
- ✅ Digital flip book album viewer
- ✅ Order management system
- ✅ Booking management system
- ✅ Image upload & management
- ✅ QR code generation & display
- ✅ Mobile responsive design

#### Backend Development (Core)
- ✅ RESTful API development
- ✅ User authentication (JWT)
- ✅ Image storage integration
- ✅ QR code generation API
- ✅ Order & booking APIs

#### Deployment (Core)
- ✅ Application deployment on client's server
- ✅ Environment configuration
- ✅ SSL configuration

---

### 3.2 Additional Features (New Requirements)

#### 👑 Super Admin Panel (Full Control)
- ✅ **Lab Management**
  - View all labs
  - Approve/Reject lab registrations
  - Set lab renewal dates (start & end)
  - Activate/Deactivate labs
  - Edit lab details
  - View lab-wise analytics
- ✅ **Studio Management**
  - View ALL studios (under labs + independent)
  - Approve/Reject studio registrations
  - Set studio renewal dates (start & end)
  - Activate/Deactivate studios
  - Assign/Reassign studio to lab
  - View studio-wise analytics
- ✅ **SMTP Configuration**
  - Configure SMTP server settings
  - Test email functionality
  - Email template management
- ✅ **Platform Analytics**
  - Overview statistics
  - Revenue reports
  - Growth metrics

#### 🏢 Lab Admin Portal
- ✅ Lab administrator login
- ✅ Manage ONLY studios under their lab
- ✅ Approve/Reject their studio registrations
- ✅ Set renewal dates for their studios
- ✅ Lab-level dashboard with statistics
- ✅ View analytics for their studios only

#### 📊 Album Production Module
- ✅ 100 photos/sheets maximum limit per album
- ✅ Production cost calculator
- ✅ Cost configuration per sheet
- ✅ Album size validation

#### 🖼️ Advanced Image Cropping System
- ✅ Auto-crop functionality (smart detection)
- ✅ Manual crop editor with preview
- ✅ Multiple aspect ratio options
- ✅ Batch cropping support

#### 📄 PDF Processing Module
- ✅ PDF file upload support
- ✅ Automatic image extraction from PDF
- ✅ Preview extracted images
- ✅ Direct album creation from PDF

#### 📧 Email System (SMTP Integration)
- ✅ Forgot password functionality
- ✅ Password reset via email
- ✅ SMTP configuration in Super Admin panel
- ✅ Test email functionality

#### 🔗 Custom URL System
- ✅ Short URL format: flip.io/{lab_id or studio_id}/{album_id}
- ✅ 10-character alphanumeric album ID
- ✅ URL validation & uniqueness

---

### 3.3 Excluded from Scope

- ❌ Payment gateway integration
- ❌ SMS/WhatsApp notifications
- ❌ Mobile application (iOS/Android)
- ❌ AI-powered features (beyond auto-crop)
- ❌ Third-party integrations
- ❌ Multi-language support
- ❌ Automated subscription billing
- ❌ Advanced analytics with charts/graphs

> **Note:** Excluded items can be added as future enhancements at additional cost.

---

## 4. Technical Specifications

### 4.1 Technology Stack

| Layer | Technology |
|-------|------------|
| **Frontend** | React 18, TypeScript, Vite, Tailwind CSS |
| **Backend** | Node.js, Express.js, TypeScript |
| **Database** | MongoDB with Mongoose ODM |
| **Cache** | Redis (for sessions & caching) |
| **Storage** | Bunny.net CDN / Cloudinary |
| **PDF Processing** | pdf-lib / pdf2pic |
| **Image Processing** | Sharp.js (for cropping) |
| **Email** | Nodemailer with SMTP |
| **Authentication** | JWT (JSON Web Tokens) |
| **Version Control** | Git & GitHub |

### 4.2 Browser Support

| Browser | Version |
|---------|---------|
| Chrome | Latest 2 versions |
| Firefox | Latest 2 versions |
| Safari | Latest 2 versions |
| Edge | Latest 2 versions |
| Mobile Browsers | iOS Safari, Chrome Mobile |

### 4.3 Performance Targets

| Metric | Target |
|--------|--------|
| Page Load Time | < 3 seconds |
| Image Upload (per image) | < 5 seconds |
| PDF Processing (10 pages) | < 30 seconds |
| Mobile Responsive | 100% |
| Uptime | 99% |

### 4.4 Album Specifications

| Specification | Value |
|---------------|-------|
| Maximum photos per album | 100 |
| Supported image formats | JPG, PNG, WEBP |
| Maximum image size | 5 MB per image |
| Maximum audio size | 10 MB |
| Album ID format | 10 alphanumeric characters |
| URL format | flip.io/{lab_id or studio_id}/{album_id} |

---

## 5. Team Structure

### 5.1 Team Composition

| Role | Name | Responsibility |
|------|------|----------------|
| **Project Lead** | Member 1 | Project management, Client communication, Backend development |
| **Frontend Developer** | Member 2 | React development, UI/UX implementation, Image editor |
| **Full Stack Developer** | Member 3 | Integration, Testing, PDF processing, Deployment |

### 5.2 Communication

| Channel | Purpose | Frequency |
|---------|---------|-----------|
| WhatsApp/Call | Quick updates, Queries | As needed |
| Email | Formal communication, Documents | Weekly |
| Video Call | Progress demo, Reviews | Weekly / Bi-weekly |

---

## 6. Project Timeline

### 6.1 Overview

| Phase | Duration | Days |
|-------|----------|------|
| Phase 1: Frontend Development | Week 1-2 | 14 Days |
| Phase 2: Backend Development | Week 3-4 | 14 Days |
| Phase 3: Additional Features | Week 5-6 | 12 Days |
| Phase 4: Testing & Bug Fixes | Week 7 | 10 Days |
| Phase 5: Deployment & Handover | Week 8 | 5 Days |
| **Total Duration** | | **55 Days** |

### 6.2 Detailed Timeline

#### Phase 1: Frontend Development (Day 1 - Day 14)

| Task | Days | Deliverable |
|------|------|-------------|
| Project setup & configuration | 1 | Base project structure |
| Public pages (Home, Features, Pricing, Contact) | 3 | 4 responsive pages |
| Authentication pages (Studio, Lab, Super Admin) | 2 | Login/Forgot Password UI |
| Studio Dashboard & Orders | 3 | Order management UI |
| Lab Admin Dashboard | 2 | Lab management UI |
| Super Admin Dashboard (Labs + Studios) | 1 | Super Admin UI |
| Album Viewer (Flip Book) | 2 | Digital album viewer |
| **Phase 1 Total** | **14** | **Complete Frontend** |

#### Phase 2: Backend Development (Day 15 - Day 28)

| Task | Days | Deliverable |
|------|------|-------------|
| Project setup & database structure | 2 | Base backend structure |
| Authentication APIs (JWT + 3 Roles) | 2 | Login/Logout/Register |
| Super Admin APIs (Labs + Studios) | 3 | Full management APIs |
| Lab Admin APIs | 2 | Studio management |
| Studio & Order APIs | 2 | CRUD operations |
| Image upload & storage | 2 | File handling with CDN |
| QR code generation & custom URLs | 1 | QR functionality |
| **Phase 2 Total** | **14** | **Complete Backend** |

#### Phase 3: Additional Features (Day 29 - Day 40)

| Task | Days | Deliverable |
|------|------|-------------|
| Image Cropping (Auto + Manual) | 4 | Crop editor with preview |
| PDF Upload & Extraction | 3 | PDF processing module |
| SMTP Integration & Forgot Password | 2 | Email system |
| Production Cost Calculator | 1 | Cost calculation |
| Frontend-Backend Integration | 2 | Working application |
| **Phase 3 Total** | **12** | **All Features** |

#### Phase 4: Testing & Bug Fixes (Day 41 - Day 50)

| Task | Days | Deliverable |
|------|------|-------------|
| Functional testing (all modules) | 4 | Test reports |
| UI/UX testing & fixes | 3 | Refined UI |
| Bug fixes & improvements | 3 | Stable application |
| **Phase 4 Total** | **10** | **Tested Application** |

#### Phase 5: Deployment & Handover (Day 51 - Day 55)

| Task | Days | Deliverable |
|------|------|-------------|
| Code deployment to server | 2 | Live application |
| Configuration & SSL setup | 1 | Secured application |
| Documentation & handover | 1 | User guides |
| Client training | 1 | Knowledge transfer |
| **Phase 5 Total** | **5** | **Live Project** |

### 6.3 Gantt Chart View

```
Week 1  |████████████████| Frontend (Public + Auth + Studio)
Week 2  |████████████████| Frontend (Lab Admin + Super Admin + Album)
Week 3  |████████████████| Backend (Setup + Auth + Super Admin APIs)
Week 4  |████████████████| Backend (Lab + Studio + Orders + QR)
Week 5  |████████████████| Additional (Cropping + PDF)
Week 6  |████████████████| Additional (Email + Integration)
Week 7  |████████████████| Testing & Bug Fixes
Week 8  |████████        | Deployment + Handover
```

---

## 7. Cost Breakdown

### 7.1 Core Development Cost

| Component | Description | Cost (₹) |
|-----------|-------------|----------|
| **Frontend Development** | React UI, All pages, Responsive design | ₹18,000 |
| **Backend Development** | APIs, Authentication, Business logic | ₹15,000 |
| **Album Viewer** | Flip book, QR code integration | ₹5,000 |
| **Testing & QA** | Functional, UI, Performance testing | ₹3,000 |
| **Documentation** | Technical docs, User guide | ₹2,000 |
| **Sub-total (Core)** | | **₹43,000** |

### 7.2 Additional Features Cost

| Component | Description | Cost (₹) |
|-----------|-------------|----------|
| **Super Admin Panel** | Full Labs + Studios management, approval, renewal dates, activation control, SMTP config, analytics | ₹10,000 |
| **Lab Admin Portal** | Own studio management, approval, renewal tracking, lab analytics | ₹6,000 |
| **Advanced Image Cropping** | Auto-crop smart detection, manual crop editor, aspect ratios, batch processing | ₹7,000 |
| **PDF Processing Module** | PDF upload, image extraction, preview, direct album creation | ₹5,000 |
| **Email System (SMTP)** | Forgot password, password reset, test email, SMTP configuration | ₹4,000 |
| **Custom URL System** | Short URLs (flip.io/1/abc), 10-digit IDs, URL validation | ₹2,000 |
| **Album Production Module** | 100 photo limit, cost calculator, size validation | ₹2,000 |
| **Sub-total (Additional)** | | **₹36,000** |

### 7.3 Deployment Cost

| Component | Description | Cost (₹) |
|-----------|-------------|----------|
| **Code Deployment** | Deploying application to client's server | ₹2,000 |
| **Configuration** | Environment setup, SSL configuration | Included |
| **Sub-total** | | **₹2,000** |

> **Note:** Deployment will be done on client's existing server infrastructure.

### 7.4 Cost Summary

| Category | Amount (₹) |
|----------|------------|
| Core Development Cost | ₹43,000 |
| Additional Features Cost | ₹36,000 |
| Deployment Cost | Included |
| **Discount Applied** | -₹1,000 |
| **Grand Total** | **₹78,000** |

### 7.5 Cost Visualization

```
┌─────────────────────────────────────────────────────────────────┐
│                      COST DISTRIBUTION                           │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  Core Development (₹43,000)         ███████████████████  55%   │
│  ├─ Frontend           ₹18,000      ████████                   │
│  ├─ Backend            ₹15,000      ███████                    │
│  ├─ Album Viewer       ₹5,000       ██                         │
│  ├─ Testing            ₹3,000       █                          │
│  └─ Documentation      ₹2,000       █                          │
│                                                                 │
│  Additional Features (₹36,000)      ██████████████  45%        │
│  ├─ Super Admin Panel  ₹10,000      █████                      │
│  ├─ Image Cropping     ₹7,000       ███                        │
│  ├─ Lab Admin Portal   ₹6,000       ███                        │
│  ├─ PDF Processing     ₹5,000       ██                         │
│  ├─ Email System       ₹4,000       ██                         │
│  ├─ Custom URLs        ₹2,000       █                          │
│  └─ Production Module  ₹2,000       █                          │
│                                                                 │
│  Deployment                         Included ✓                  │
│                                                                 │
│  ═══════════════════════════════════════════════════════════   │
│  TOTAL                              ₹78,000                    │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### 7.6 Cost Comparison

| Feature | Market Rate | Our Rate | You Save |
|---------|-------------|----------|----------|
| **Core Features** | | | |
| Frontend Development | ₹30,000+ | ₹18,000 | ₹12,000 |
| Backend Development | ₹25,000+ | ₹15,000 | ₹10,000 |
| Album Viewer | ₹10,000+ | ₹5,000 | ₹5,000 |
| Testing & Docs | ₹8,000+ | ₹5,000 | ₹3,000 |
| **Additional Features** | | | |
| Super Admin Panel | ₹25,000+ | ₹10,000 | ₹15,000 |
| Lab Admin Portal | ₹15,000+ | ₹6,000 | ₹9,000 |
| Image Cropping | ₹15,000+ | ₹7,000 | ₹8,000 |
| PDF Processing | ₹12,000+ | ₹5,000 | ₹7,000 |
| Email System | ₹8,000+ | ₹4,000 | ₹4,000 |
| Custom URLs | ₹5,000+ | ₹2,000 | ₹3,000 |
| Production Module | ₹5,000+ | ₹2,000 | ₹3,000 |
| Deployment | ₹5,000+ | Included | ₹5,000 |
| **Total** | **₹1,63,000+** | **₹78,000** | **₹85,000** |

> 💰 **Total Savings: ₹85,000** (52% below market rate!)

---

## 8. Payment Terms

### 8.1 Payment Schedule (3 Milestones)

| Milestone | Percentage | Amount (₹) | Due Date |
|-----------|------------|------------|----------|
| **Milestone 1** | 40% | ₹31,200 | Project Start |
| **Milestone 2** | 35% | ₹27,300 | After Development Complete |
| **Milestone 3** | 25% | ₹19,500 | After Deployment & Handover |
| **Total** | **100%** | **₹78,000** | |

### 8.2 Milestone Details

#### Milestone 1 - Project Kickoff (40% - ₹31,200)
**Trigger:** Upon agreement signing  
**Deliverables:**
- Project setup completed
- Development environment ready
- Development started

#### Milestone 2 - Development Complete (35% - ₹27,300)
**Trigger:** After Phase 1, 2 & 3 completion  
**Deliverables:**
- Complete frontend (all pages, all roles)
- Complete backend (all APIs)
- All additional features implemented:
  - Super Admin managing Labs + Studios ✓
  - Lab Admin Portal working ✓
  - PDF extraction working ✓
  - Cropping tools working ✓
  - Email system working ✓
  - Custom URLs working ✓
- Working integrated application
- Demo presentation

#### Milestone 3 - Final Delivery (25% - ₹19,500)
**Trigger:** After Phase 4 & 5 completion  
**Deliverables:**
- Tested & bug-free application
- Deployed on live server
- SSL configured
- Custom domain configured
- Documentation & training completed
- All credentials handed over
- 15-day support period begins

### 8.3 Payment Methods

| Method | Details |
|--------|---------|
| Bank Transfer (NEFT/IMPS) | Preferred method |
| UPI | PhonePe / GPay / Paytm |
| Cash | Direct payment |
| Cheque | In favor of "Visainnovations" |

---

## 9. Deliverables

### 9.1 Final Deliverables

| # | Deliverable | Format |
|---|-------------|--------|
| 1 | Live web application | Deployed on server |
| 2 | Custom domain configured | flip.io or client's domain |
| 3 | User manual (Studio) | PDF |
| 4 | User manual (Lab Admin) | PDF |
| 5 | User manual (Super Admin) | PDF |
| 6 | Super Admin credentials | Secure document |
| 7 | SMTP configuration guide | PDF |
| 8 | Application access | URL & login details |

### 9.2 Feature Deliverables Checklist

| Module | Features | Status |
|--------|----------|--------|
| **Public Website** | Home, Features, Pricing, Contact | ⬜ |
| **Authentication** | Login, Register, Forgot Password | ⬜ |
| **Studio Dashboard** | Orders, Albums, Bookings, Settings | ⬜ |
| **Lab Admin Portal** | Own Studios, Renewal Dates, Analytics | ⬜ |
| **Super Admin Panel** | ALL Labs + Studios, Approval, Renewal, SMTP | ⬜ |
| **Album Viewer** | Flip book, Music, QR Code | ⬜ |
| **Image Processing** | Auto-crop, Manual crop, PDF extract | ⬜ |
| **Email System** | SMTP, Forgot Password | ⬜ |
| **Custom URLs** | Short URLs, 10-digit IDs | ⬜ |

### 9.3 Post-Delivery Support

| Support | Duration | Coverage |
|---------|----------|----------|
| Bug fixes | 15 days | Critical & major bugs |
| Technical support | 15 days | Via WhatsApp/Email |
| Minor changes | Not included | Chargeable |
| Feature additions | Not included | Separate quote |

---

## 10. Terms & Conditions

### 10.1 General Terms

1. This proposal is valid for **30 days** from the date of issue.
2. Prices are in **Indian Rupees (₹)** and inclusive of all taxes.
3. Any changes to scope will require a **change request** and may affect timeline/cost.
4. Client must provide required content (images, text) within **3 days** of request.
5. Project timeline starts from date of first milestone payment.

### 10.2 Intellectual Property

1. Source code remains the property of **Visainnovations**.
2. Client receives full rights to **use the deployed web application**.
3. Client owns all uploaded content (images, albums, data).
4. Visainnovations retains right to showcase the project in portfolio.
5. Third-party libraries used are subject to their respective licenses.

### 10.3 Admin Control & Renewal Management

1. **Super Admin** has full control over ALL Labs and ALL Studios.
2. **Lab Admin** can only manage studios under their own lab.
3. Admin manually sets start date and end date for each Lab/Studio.
4. System automatically restricts access when end date passes.
5. Admin can extend dates anytime to restore access.
6. No automated billing or payment integration included.

### 10.4 Confidentiality

1. Both parties agree to keep project details confidential.
2. Client data will not be shared with third parties.
3. NDA can be signed upon request.

### 10.5 Warranty

1. **15 days** free bug-fix support after deployment.
2. Bugs due to client modifications are not covered.
3. Server/hosting issues are not covered under warranty.
4. SMTP server issues (if using client's SMTP) are not covered.

### 10.6 What's NOT Included

1. ❌ Third-party integrations (payment gateways, SMS, etc.)
2. ❌ Automated subscription billing
3. ❌ Mobile applications
4. ❌ Advanced analytics with charts
5. ❌ Multi-language support

---

## 11. Contact Information

### Visainnovations

| | |
|---|---|
| **Company** | Visainnovations |
| **Location** | Tamil Nadu, India |
| **Email** | visainnovations123@gmail.com |
| **Phone** | +91 9894454345 |

---

## Appendix

### A. User Role & Permissions Matrix

| Feature | Super Admin | Lab Admin | Studio |
|---------|:-----------:|:---------:|:------:|
| **Lab Management** | | | |
| View All Labs | ✅ | ❌ | ❌ |
| Create/Edit Labs | ✅ | ❌ | ❌ |
| Approve/Reject Labs | ✅ | ❌ | ❌ |
| Set Lab Renewal Dates | ✅ | ❌ | ❌ |
| Activate/Deactivate Labs | ✅ | ❌ | ❌ |
| **Studio Management** | | | |
| View All Studios | ✅ | Own Only | ❌ |
| Create/Edit Studios | ✅ | Own Only | ❌ |
| Approve/Reject Studios | ✅ | Own Only | ❌ |
| Set Studio Renewal Dates | ✅ | Own Only | ❌ |
| Activate/Deactivate Studios | ✅ | Own Only | ❌ |
| Assign Studio to Lab | ✅ | ❌ | ❌ |
| **Configuration** | | | |
| SMTP Configuration | ✅ | ❌ | ❌ |
| Platform Settings | ✅ | ❌ | ❌ |
| **Operations** | | | |
| Create Orders | ❌ | ❌ | ✅ |
| Create Albums | ❌ | ❌ | ✅ |
| Manage Bookings | ❌ | ❌ | ✅ |
| **Analytics** | | | |
| Platform Analytics | ✅ | ❌ | ❌ |
| Lab Analytics | ✅ | Own Only | ❌ |
| Studio Analytics | ✅ | Own Studios | Own Only |

### B. URL Examples

| Type | URL | Description |
|------|-----|-------------|
| Public Album | `flip.io/1/drfghdf7g0` | Lab/Studio 1, Album drfghdf7g0 |
| Public Album | `flip.io/25/abc1234xyz` | Lab/Studio 25, Album abc1234xyz |
| Studio Login | `flip.io/studio/login` | Studio portal |
| Lab Admin | `flip.io/lab/login` | Lab admin portal |
| Super Admin | `flip.io/admin` | Super admin panel |

### C. System Flow Diagram

```
┌─────────────────────────────────────────────────────────────────────────┐
│                          SYSTEM FLOW                                     │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│  1. REGISTRATION FLOW                                                   │
│  ════════════════════                                                   │
│                                                                         │
│  Lab/Studio Registers → Pending Approval → Super Admin/Lab Admin        │
│                                             Approves → Sets Dates →     │
│                                             Account Active              │
│                                                                         │
│  2. RENEWAL FLOW                                                        │
│  ═══════════════                                                        │
│                                                                         │
│  End Date Passes → System Auto-Deactivates → Admin Extends Date →       │
│                    Access Blocked            Access Restored            │
│                                                                         │
│  3. ALBUM CREATION FLOW                                                 │
│  ══════════════════════                                                 │
│                                                                         │
│  Studio Creates Order → Uploads Images (Max 100) → Creates Album →      │
│                         OR Uploads PDF             QR Generated →       │
│                         (Auto Extract)             Client Scans →       │
│                                                    Views Flip Book      │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## Acceptance

By signing below, the client agrees to the terms and conditions outlined in this proposal.

| | Client | Visainnovations |
|---|--------|-----------------|
| **Name** | P. Manikandam | _________________ |
| **Designation** | _________________ | Project Lead |
| **Date** | _________________ | January 19, 2026 |
| **Signature** | _________________ | _________________ |

---

### Payment Confirmation

| Milestone | Amount (₹) | Date Paid | Mode | Signature |
|-----------|------------|-----------|------|-----------|
| Milestone 1 (40%) | ₹31,200 | | | |
| Milestone 2 (35%) | ₹27,300 | | | |
| Milestone 3 (25%) | ₹19,500 | | | |
| **Total** | **₹78,000** | | | |

---

<div align="center">

### 💰 Investment Summary

| | |
|---|---|
| **Total Project Cost** | **₹78,000** |
| **Project Duration** | **55 Days** |
| **Market Value** | ₹1,63,000+ |
| **Your Savings** | ₹85,000 (52%) |

---

**Thank you for considering Visainnovations!**

*We look forward to building this exciting platform with you.*

---

© 2026 Visainnovations. All Rights Reserved.

</div>
