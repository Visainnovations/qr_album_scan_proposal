# Project Proposal & Agreement

![Visainnovations](https://img.shields.io/badge/VISAINNOVATIONS-Make%20Tomorrow%20Magical✨-7c3aed?style=for-the-badge)

---

## FXFlipbook - Digital Flipbook SaaS Platform

**Prepared by:** Visainnovations  
**Date:** January 20, 2026  
**Version:** 3.0  
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

**Visainnovations** is pleased to present this proposal for the development of **FXFlipbook**, a comprehensive SaaS platform for digital photo flipbooks. This platform enables photo studios and labs/resellers to create stunning digital albums, share them via QR codes, and manage their businesses with event-based subscription plans.

| Project | FXFlipbook |
|---------|------------|
| **Client** | P. Manikandam |
| **Duration** | 65 Days |
| **Team Size** | 3 Members |
| **Total Cost** | ₹1,35,000 |

---

## 2. Project Overview

### 2.1 Problem Statement

Photo studios and labs face challenges in:
- Creating and delivering digital albums efficiently
- Managing multiple orders and client relationships
- Providing modern digital viewing experience
- Sharing albums easily via mobile-friendly methods
- Managing subscription-based business model
- Labs coordinating with multiple studios

### 2.2 Proposed Solution

A complete SaaS platform that offers:

| Feature | Description |
|---------|-------------|
| **Digital Flipbook Viewer** | Interactive album with page-flip animations & sound |
| **QR Code Sharing** | Instant sharing via scannable QR codes |
| **Studio Dashboard** | Create albums, manage bookings, view analytics |
| **Lab/Reseller Dashboard** | Create albums for studios, manage studio network |
| **Admin Panel** | Platform management, analytics, SMTP configuration |
| **Razorpay Integration** | Automated subscription billing with UPI/Cards |
| **Event-Based Plans** | Pay per events (albums) with yearly subscription |
| **Auto Data Lifecycle** | Expiry warnings, auto-deletion after 30 days |

### 2.3 Platform Architecture

```
┌─────────────────────────────────────────────────────────────────────────┐
│                      FXFLIPBOOK PLATFORM ARCHITECTURE                    │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│                       ┌─────────────────────┐                           │
│                       │       ADMIN         │                           │
│                       │  (Platform Owner)   │                           │
│                       │                     │                           │
│                       │ • View All Users    │                           │
│                       │ • Manage Plans      │                           │
│                       │ • Country Reports   │                           │
│                       │ • SMTP Config       │                           │
│                       │ • Platform Analytics│                           │
│                       └─────────────────────┘                           │
│                                                                         │
│         ┌─────────────────────────────────────────────────┐            │
│         │          SELF-REGISTRATION + AUTO PAYMENT        │            │
│         │              (Razorpay → Instant Access)         │            │
│         └─────────────────────────┬───────────────────────┘            │
│                                   │                                     │
│                   ┌───────────────┴───────────────┐                    │
│                   │                               │                     │
│                   ▼                               ▼                     │
│      ┌────────────────────────┐     ┌────────────────────────┐        │
│      │    LAB / RESELLER      │     │        STUDIO          │        │
│      │                        │     │                        │        │
│      │ Plans: 500-10000       │     │ Plans: 25-250          │        │
│      │ events/year            │     │ events/year            │        │
│      │                        │     │                        │        │
│      │ • Create OWN albums    │     │ • Create OWN albums    │        │
│      │ • Create FOR studios   │     │ • View Lab-Shared      │        │
│      │ • Manage studio network│     │   albums               │        │
│      │ • Lab analytics        │     │ • Share with customers │        │
│      └───────────┬────────────┘     └────────────────────────┘        │
│                  │                                                      │
│                  │ Creates Album for Studio                            │
│                  ▼                                                      │
│      ┌────────────────────────────────────────────────────┐           │
│      │  📧 New User → Login Creds Email                    │           │
│      │  📧 Existing User → "Album Shared" Notification     │           │
│      └────────────────────────────────────────────────────┘           │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

### 2.4 User Types & Capabilities

| Feature | Admin | Lab/Reseller | Studio |
|---------|:-----:|:------------:|:------:|
| **Account Management** | | | |
| View all users | ✅ | ❌ | ❌ |
| Manage subscription plans | ✅ | ❌ | ❌ |
| SMTP configuration | ✅ | ❌ | ❌ |
| Country-wise reports | ✅ | ❌ | ❌ |
| **Album Creation** | | | |
| Create own albums | ❌ | ✅ | ✅ |
| Create albums for studios | ❌ | ✅ | ❌ |
| View lab-shared albums | ❌ | ❌ | ✅ |
| Share album QR with customers | ❌ | ✅ | ✅ |
| **Studio Management** | | | |
| Add studio details | ❌ | ✅ | ❌ |
| Send login creds to studios | ❌ | ✅ (auto) | ❌ |
| View studio list | ✅ | ✅ (own) | ❌ |
| **Analytics** | | | |
| Platform analytics | ✅ | ❌ | ❌ |
| Lab analytics (studios + events) | ❌ | ✅ | ❌ |
| Studio analytics (own albums) | ❌ | ❌ | ✅ |
| QR scan view count | ✅ | ✅ | ✅ |
| Booking details | ❌ | ❌ | ✅ |

### 2.5 Subscription Plans

#### Studio Plans

| Plan | Events/Year | Sheets/Event | Price/Event | Yearly Price |
|------|:-----------:|:------------:|:-----------:|:------------:|
| Starter | 25 | 100 | ₹50 | ₹1,250 |
| Basic | 50 | 100 | ₹40 | ₹2,000 |
| Standard | 100 | 100 | ₹30 | ₹3,000 |
| Premium | 250 | 100 | ₹25 | ₹6,250 |

#### Lab/Reseller Plans

| Plan | Events/Year | Sheets/Event | Price/Event | Yearly Price |
|------|:-----------:|:------------:|:-----------:|:------------:|
| Lab Basic | 500 | 100 | ₹20 | ₹10,000 |
| Lab Standard | 1,000 | 100 | ₹19 | ₹19,000 |
| Lab Pro | 3,000 | 100 | ₹18 | ₹54,000 |
| Lab Business | 5,000 | 100 | ₹17 | ₹85,000 |
| Lab Enterprise | 10,000 | 100 | ₹15 | ₹1,50,000 |

### 2.6 URL Structure

```
Album URL: https://flip.io/{user_id}/{album_id}

Examples:
• https://flip.io/1/drfghdf7g0
• https://flip.io/142/abc1234xyz

Components:
- user_id: Lab or Studio ID (numeric)
- album_id: 10-character alphanumeric unique identifier
```

### 2.7 Subscription Lifecycle

```
┌─────────────────────────────────────────────────────────────────────────┐
│                      SUBSCRIPTION LIFECYCLE                              │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│  Day 1                Day 360              Day 365           Day 395    │
│    │                     │                    │                 │       │
│    ▼                     ▼                    ▼                 ▼       │
│  ┌──────┐            ┌──────┐             ┌──────┐          ┌──────┐  │
│  │ START│            │ 📧   │             │ ⚠️   │          │ 🗑️   │   │
│  │      │            │EMAIL │             │EXPIRY│          │DELETE│   │
│  └──────┘            └──────┘             └──────┘          └──────┘  │
│    │                     │                    │                 │       │
│  Account             "5 days              Access            "Data      │
│  Created &           left to              Blocked           Deleted"   │
│  Active              renew!"                                Email      │
│                                                                         │
│  ───────────────────────────────────────────────────────────────────   │
│                                                                         │
│  IF USER RENEWS (anytime before Day 395):                              │
│  → Access Restored Immediately                                          │
│  → Data Preserved                                                       │
│                                                                         │
│  IF USER DOESN'T RENEW (after Day 395):                                │
│  → All Albums Deleted                                                   │
│  → All Images Deleted from CDN                                          │
│  → All Orders Deleted                                                   │
│  → Account Kept (can re-subscribe fresh)                               │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Scope of Work

### 3.1 Included in Scope

#### 🌐 Public Website
- ✅ Home page with features showcase
- ✅ Pricing page (Studio & Lab plans)
- ✅ Features page
- ✅ Contact page
- ✅ Mobile responsive design

#### 🔐 Authentication System
- ✅ 3 Login portals (Admin, Lab/Reseller, Studio)
- ✅ Registration with country selection
- ✅ **Google Sign-in / Sign-up (OAuth 2.0)**
- ✅ Email + Password authentication
- ✅ Forgot password (email reset link)
- ✅ JWT token-based sessions

#### 💳 Payment Integration (Razorpay)
- ✅ **Razorpay payment gateway integration**
- ✅ **UPI QR code payment** (GPay, PhonePe, Paytm)
- ✅ Credit/Debit card payments
- ✅ Net banking
- ✅ **Subscription/recurring billing**
- ✅ **Event-based plan management**
- ✅ Payment webhooks for auto-activation
- ✅ Invoice generation

#### 👑 Admin Panel
- ✅ Admin dashboard with platform statistics
- ✅ View all Labs and Studios
- ✅ Subscription plan management (add/edit/delete plans)
- ✅ **Country-wise user reports**
- ✅ Revenue analytics
- ✅ SMTP configuration panel
- ✅ Email template management
- ✅ Test email functionality

#### 🏢 Lab/Reseller Portal
- ✅ Lab dashboard with analytics
- ✅ **Create own albums** (uses Lab's event quota)
- ✅ **Create albums FOR studios** (uses Lab's event quota)
- ✅ Add/manage studio details
- ✅ View studios under lab with event counts
- ✅ **Auto-send login credentials to new studios**
- ✅ **Auto-notify existing studios** when album shared
- ✅ Events remaining counter
- ✅ QR code generation for all albums
- ✅ Subscription management (view/renew)

#### 📷 Studio Portal
- ✅ Studio dashboard
- ✅ **"My Albums" section** (self-created)
- ✅ **"Lab Shared" section** (created by lab for this studio)
- ✅ Create albums (uses Studio's event quota)
- ✅ Share album QR with customers
- ✅ Booking management
- ✅ Events remaining counter
- ✅ QR scan analytics
- ✅ Subscription management (view/renew)

#### 📖 Digital Flipbook Album
- ✅ Interactive page-flip animation
- ✅ **Maximum 100 photos per album**
- ✅ Background music support (**1MB max**)
- ✅ **Page turn sound (ON/OFF toggle)**
- ✅ Mobile responsive viewer
- ✅ Fullscreen mode
- ✅ Social sharing options
- ✅ Studio branding on album

#### 🖼️ Image Processing
- ✅ **Auto-crop with smart detection**
- ✅ **Manual crop editor with preview**
- ✅ Multiple aspect ratios (1:1, 4:3, 16:9, custom)
- ✅ Batch image upload (up to 100)
- ✅ Image reordering (drag & drop)

#### 📄 PDF Processing
- ✅ PDF file upload
- ✅ **Automatic image extraction from PDF**
- ✅ Preview extracted images
- ✅ Select pages to include
- ✅ Direct album creation from PDF

#### 📧 Email Automation System
- ✅ **Registration confirmation email**
- ✅ **Subscription expiry warning (5 days before)**
- ✅ **Data deletion notification (30 days after expiry)**
- ✅ **Login credentials email (new studio by lab)**
- ✅ **Album shared notification (existing studio)**
- ✅ Password reset email
- ✅ Payment confirmation email

#### 🗑️ Automated Data Management
- ✅ **Auto-block access on subscription expiry**
- ✅ **30-day grace period after expiry**
- ✅ **Auto-delete ALL data after 30 days**
  - Albums, Images, Orders, QR codes, Bookings
- ✅ Scheduled cleanup jobs (daily)
- ✅ Keep account for re-subscription

#### 📊 Analytics
- ✅ **QR scan view count** (per album)
- ✅ **Booking details tracking**
- ✅ **Country-wise reports** (Admin)
- ✅ **Studios + Events count** (Lab dashboard)
- ✅ Events used vs remaining
- ✅ Popular albums

#### 🔗 Custom URL System
- ✅ Short URL: flip.io/{user_id}/{album_id}
- ✅ 10-character unique album ID
- ✅ URL validation

#### 🚀 Deployment
- ✅ Application deployment on client's server
- ✅ Environment configuration
- ✅ SSL configuration
- ✅ Domain setup

---

### 3.2 Excluded from Scope

- ❌ SMS/WhatsApp notifications
- ❌ Mobile application (iOS/Android)
- ❌ Video album support
- ❌ AI-powered features (beyond auto-crop)
- ❌ Multi-language support
- ❌ White-label customization
- ❌ Offline mode
- ❌ Third-party integrations (except Razorpay & Google OAuth)

> **Note:** Excluded items can be added as future enhancements at additional cost.

---

## 4. Technical Specifications

### 4.1 Technology Stack

| Layer | Technology |
|-------|------------|
| **Frontend** | React 18, TypeScript, Vite, Tailwind CSS |
| **Backend** | Node.js, Express.js, TypeScript |
| **Database** | MongoDB with Mongoose ODM |
| **Cache** | Redis (sessions, rate limiting) |
| **Storage** | Bunny.net CDN |
| **Payment** | Razorpay (Subscriptions + One-time) |
| **Authentication** | JWT + Google OAuth 2.0 |
| **PDF Processing** | pdf-lib / pdf2pic |
| **Image Processing** | Sharp.js |
| **Email** | Nodemailer + SMTP |
| **Scheduler** | node-cron (for auto-deletion jobs) |
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
| Album Load Time | < 5 seconds |
| Image Upload | < 5 seconds per image |
| PDF Processing | < 30 seconds (100 pages) |
| Payment Processing | < 10 seconds |
| Mobile Responsive | 100% |
| Uptime | 99% |

### 4.4 Album Specifications

| Specification | Value |
|---------------|-------|
| Maximum photos per album | 100 |
| Maximum music file size | 1 MB |
| Supported image formats | JPG, PNG, WEBP |
| Maximum image size | 5 MB per image |
| Album ID format | 10 alphanumeric characters |
| Page turn sound | Toggle ON/OFF |

---

## 5. Team Structure

### 5.1 Team Composition

| Role | Responsibility |
|------|----------------|
| **Project Lead** | Project management, Client communication, Backend architecture, Payment integration |
| **Frontend Developer** | React development, UI/UX implementation, Flipbook viewer, Crop tools |
| **Full Stack Developer** | API development, PDF processing, Email system, Testing, Deployment |

### 5.2 Communication

| Channel | Purpose | Frequency |
|---------|---------|-----------|
| WhatsApp/Call | Quick updates, Queries | As needed |
| Email | Formal communication, Documents | Weekly |
| Video Call | Progress demo, Reviews | Weekly |

---

## 6. Project Timeline

### 6.1 Overview

| Phase | Duration | Days |
|-------|----------|------|
| Phase 1: Core Frontend | Week 1-2 | 14 Days |
| Phase 2: Core Backend | Week 3-4 | 14 Days |
| Phase 3: Payment & Subscription | Week 5 | 7 Days |
| Phase 4: Advanced Features | Week 6-7 | 12 Days |
| Phase 5: Testing & Bug Fixes | Week 8-9 | 12 Days |
| Phase 6: Deployment & Handover | Week 9-10 | 6 Days |
| **Total Duration** | | **65 Days** |

### 6.2 Detailed Timeline

#### Phase 1: Core Frontend (Day 1 - Day 14)

| Task | Days | Deliverable |
|------|------|-------------|
| Project setup & configuration | 1 | Base project structure |
| Public pages (Home, Features, Pricing, Contact) | 3 | 4 responsive pages |
| Authentication UI (Login, Register, Forgot Password) | 2 | All auth pages |
| Admin Dashboard UI | 2 | Admin panel layout |
| Lab/Reseller Dashboard UI | 2 | Lab panel layout |
| Studio Dashboard UI | 2 | Studio panel layout |
| Flipbook Album Viewer | 2 | Interactive viewer |
| **Phase 1 Total** | **14** | **Complete Frontend** |

#### Phase 2: Core Backend (Day 15 - Day 28)

| Task | Days | Deliverable |
|------|------|-------------|
| Project setup & database schema | 2 | Backend structure |
| Authentication APIs (JWT + Google OAuth) | 2 | Auth system |
| Admin APIs | 2 | Admin endpoints |
| Lab/Reseller APIs | 3 | Lab management |
| Studio APIs | 2 | Studio management |
| Album & Order APIs | 2 | CRUD operations |
| Image upload & CDN integration | 1 | File handling |
| **Phase 2 Total** | **14** | **Complete Backend** |

#### Phase 3: Payment & Subscription (Day 29 - Day 35)

| Task | Days | Deliverable |
|------|------|-------------|
| Razorpay integration | 2 | Payment gateway |
| Subscription plan management | 2 | Plan CRUD |
| Event quota tracking | 1 | Usage tracking |
| Webhooks & auto-activation | 1 | Payment callbacks |
| Invoice generation | 1 | Billing system |
| **Phase 3 Total** | **7** | **Payment System** |

#### Phase 4: Advanced Features (Day 36 - Day 47)

| Task | Days | Deliverable |
|------|------|-------------|
| Image cropping (Auto + Manual) | 3 | Crop editor |
| PDF upload & extraction | 2 | PDF processing |
| Email automation system | 2 | All email templates |
| Auto data deletion system | 2 | Scheduled cleanup |
| Lab-Studio sharing workflow | 2 | Album sharing |
| QR code & custom URLs | 1 | URL system |
| **Phase 4 Total** | **12** | **All Features** |

#### Phase 5: Testing & Bug Fixes (Day 48 - Day 59)

| Task | Days | Deliverable |
|------|------|-------------|
| Functional testing | 4 | Test reports |
| Payment flow testing | 2 | Payment verification |
| UI/UX testing & fixes | 3 | Refined UI |
| Bug fixes & improvements | 3 | Stable application |
| **Phase 5 Total** | **12** | **Tested Application** |

#### Phase 6: Deployment & Handover (Day 60 - Day 65)

| Task | Days | Deliverable |
|------|------|-------------|
| Server setup & deployment | 2 | Live application |
| SSL & domain configuration | 1 | Secured site |
| Razorpay production setup | 1 | Live payments |
| Documentation & training | 2 | User guides |
| **Phase 6 Total** | **6** | **Live Project** |

### 6.3 Gantt Chart

```
Week 1  |████████████████| Frontend (Public + Auth)
Week 2  |████████████████| Frontend (Admin + Lab + Studio + Viewer)
Week 3  |████████████████| Backend (Auth + Admin + Lab)
Week 4  |████████████████| Backend (Studio + Albums + CDN)
Week 5  |████████████████| Payment (Razorpay + Subscriptions)
Week 6  |████████████████| Advanced (Cropping + PDF + Email)
Week 7  |████████████████| Advanced (Auto-delete + Sharing + QR)
Week 8  |████████████████| Testing
Week 9  |████████████████| Testing + Bug Fixes
Week 10 |████████        | Deployment + Handover
```

---

## 7. Cost Breakdown

### 7.1 Core Development Cost

| Component | Description | Cost (₹) |
|-----------|-------------|----------|
| **Frontend Development** | React 18 UI, Public website (4 pages), 3 Dashboard portals (Admin, Lab, Studio), Responsive design, Mobile optimization | ₹28,000 |
| **Backend Development** | Node.js/Express APIs, MongoDB database design, Redis caching, Authentication system, Business logic | ₹22,000 |
| **Flipbook Album Viewer** | Interactive page-flip animation, Page turn sound toggle, Fullscreen mode, Music player, Social sharing | ₹8,000 |
| **Testing & QA** | Functional testing, UI/UX testing, Performance testing, Payment flow testing, Cross-browser testing | ₹6,000 |
| **Documentation** | Technical documentation, API docs, User guides (Admin, Lab, Studio), Deployment guide | ₹4,000 |
| **Sub-total (Core)** | | **₹68,000** |

### 7.2 Additional Features Cost

| Component | Description | Cost (₹) |
|-----------|-------------|----------|
| **Razorpay Payment Integration** | Complete payment gateway setup, UPI QR code payments, Credit/Debit cards, Net banking, Subscription billing with auto-renewal, Payment webhooks, Auto-activation on payment, Invoice generation, Refund handling | ₹22,000 |
| **Lab/Reseller Portal** | Complete lab dashboard, Create albums for studios, Studio network management, Auto-send login credentials to new studios, Auto-notify existing studios, Lab analytics with studio performance, Events tracking per studio | ₹15,000 |
| **Event-Based Subscription System** | Plan management (9 plans - Studio & Lab), Event quota tracking, Usage limits & alerts, Renewal system, Plan upgrades/downgrades, Subscription history | ₹12,000 |
| **Email Automation System** | 7 automated emails (Welcome, Expiry warning, Data deletion, Studio credentials, Album shared, Password reset, Payment confirmation), SMTP configuration panel, Email templates, Test email functionality | ₹10,000 |
| **Advanced Image Cropping** | Auto-crop with AI edge detection, Manual crop editor with live preview, Multiple aspect ratios (1:1, 4:3, 16:9, custom), Batch processing, Undo/redo functionality | ₹10,000 |
| **PDF Processing Module** | PDF file upload, Multi-page image extraction, Page preview before extraction, Selective page import, Quality optimization, Direct album creation | ₹8,000 |
| **Auto Data Deletion System** | Scheduled cleanup jobs (daily cron), 30-day grace period tracking, CDN file deletion, Database cleanup, Email notification triggers, Deletion logs | ₹7,000 |
| **Google OAuth Integration** | Google Sign-in/Sign-up, Profile data sync, Secure token management, Seamless authentication flow | ₹5,000 |
| **Country Selection & Reports** | Country dropdown on registration, Country-wise admin analytics, Geographic distribution reports, Regional statistics | ₹5,000 |
| **Custom URL System** | Short URL generation (flip.io/id/album), 10-digit unique album ID generator, URL validation & uniqueness check, SEO-friendly structure | ₹4,000 |
| **Sub-total (Additional)** | | **₹98,000** |

### 7.3 Deployment Cost

| Component | Description | Cost (₹) |
|-----------|-------------|----------|
| **Server Deployment** | Application deployment on client server, Environment configuration, Performance optimization | ₹4,000 |
| **Configuration** | SSL certificate setup, Domain configuration, Razorpay production mode, CDN setup, SMTP configuration | Included |
| **Sub-total** | | **₹4,000** |

### 7.4 Cost Summary

| Category | Amount (₹) |
|----------|------------|
| Core Development | ₹68,000 |
| Additional Features | ₹98,000 |
| Deployment | ₹4,000 |
| **Sub-Total** | **₹1,70,000** |
| **Special Discount** | -₹35,000 |
| **Grand Total** | **₹1,35,000** |

### 7.5 Cost Visualization

```
┌─────────────────────────────────────────────────────────────────┐
│                      COST DISTRIBUTION                           │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  Core Development (₹68,000)         ████████████████  40%      │
│  ├─ Frontend           ₹28,000      ███████████                │
│  ├─ Backend            ₹22,000      █████████                  │
│  ├─ Flipbook Viewer    ₹8,000       ███                        │
│  ├─ Testing & QA       ₹6,000       ██                         │
│  └─ Documentation      ₹4,000       ██                         │
│                                                                 │
│  Additional Features (₹98,000)      ████████████████████  58%  │
│  ├─ Razorpay Payment   ₹22,000      █████████                  │
│  ├─ Lab Portal         ₹15,000      ██████                     │
│  ├─ Subscription Sys   ₹12,000      █████                      │
│  ├─ Email Automation   ₹10,000      ████                       │
│  ├─ Image Cropping     ₹10,000      ████                       │
│  ├─ PDF Processing     ₹8,000       ███                        │
│  ├─ Auto Deletion      ₹7,000       ███                        │
│  ├─ Google OAuth       ₹5,000       ██                         │
│  ├─ Country Features   ₹5,000       ██                         │
│  └─ Custom URLs        ₹4,000       ██                         │
│                                                                 │
│  Deployment (₹4,000)                ██  2%                     │
│                                                                 │
│  ───────────────────────────────────────────────────────────   │
│  Sub-Total                          ₹1,70,000                  │
│  Special Discount                   -₹35,000                   │
│  ═══════════════════════════════════════════════════════════   │
│  GRAND TOTAL                        ₹1,35,000                  │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### 7.6 Market Comparison

| Feature | Market Rate | Our Rate | Savings |
|---------|-------------|----------|---------|
| Frontend (3 Dashboards + Public) | ₹50,000+ | ₹28,000 | ₹22,000 |
| Backend + APIs | ₹40,000+ | ₹22,000 | ₹18,000 |
| Razorpay + Subscriptions | ₹40,000+ | ₹22,000 | ₹18,000 |
| Lab Portal + Studio Sharing | ₹30,000+ | ₹15,000 | ₹15,000 |
| Event-Based Subscription System | ₹20,000+ | ₹12,000 | ₹8,000 |
| Email Automation (7 types) | ₹18,000+ | ₹10,000 | ₹8,000 |
| Image Cropping (Auto + Manual) | ₹20,000+ | ₹10,000 | ₹10,000 |
| PDF Processing | ₹15,000+ | ₹8,000 | ₹7,000 |
| Google OAuth | ₹10,000+ | ₹5,000 | ₹5,000 |
| Auto Data Deletion | ₹12,000+ | ₹7,000 | ₹5,000 |
| Other Features | ₹15,000+ | ₹9,000 | ₹6,000 |
| Testing & Deployment | ₹15,000+ | ₹10,000 | ₹5,000 |
| **Total** | **₹2,85,000+** | **₹1,35,000** | **₹1,50,000** |

> 💰 **Total Savings: ₹1,50,000** (53% below market rate!)

---

## 8. Payment Terms

### 8.1 Payment Schedule (3 Milestones)

| Milestone | Percentage | Amount (₹) | Trigger |
|-----------|:----------:|:----------:|---------|
| **Milestone 1** | 40% | ₹54,000 | Project Start |
| **Milestone 2** | 35% | ₹47,250 | Development Complete |
| **Milestone 3** | 25% | ₹33,750 | Deployment & Handover |
| **Total** | **100%** | **₹1,35,000** | |

### 8.2 Milestone Details

#### Milestone 1 - Project Kickoff (40% - ₹54,000)
**Trigger:** Upon agreement signing  
**Deliverables:**
- Project setup completed
- Development environment ready
- Development started
- Weekly progress updates begin

#### Milestone 2 - Development Complete (35% - ₹47,250)
**Trigger:** After Phase 1-4 completion  
**Deliverables:**
- Complete frontend (all 3 dashboards + public pages)
- Complete backend (all APIs)
- Razorpay integration working
- Google OAuth working
- All features implemented:
  - Lab creating albums for studios ✓
  - Email automation (7 types) ✓
  - Auto data deletion ✓
  - Auto-crop + Manual crop ✓
  - PDF processing ✓
  - Subscription system ✓
  - Country-wise reports ✓
- Working integrated application
- Demo presentation

#### Milestone 3 - Final Delivery (25% - ₹33,750)
**Trigger:** After Phase 5-6 completion  
**Deliverables:**
- Fully tested & bug-free application
- Deployed on live server
- SSL & domain configured
- Razorpay live mode activated
- All documentation delivered
- Admin, Lab & Studio user guides
- Training session completed
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
| 2 | Custom domain configured | flip.io or client domain |
| 3 | Admin credentials | Secure document |
| 4 | Admin user guide | PDF |
| 5 | Lab/Reseller user guide | PDF |
| 6 | Studio user guide | PDF |
| 7 | Technical documentation | PDF |
| 8 | API documentation | PDF |
| 9 | Razorpay dashboard access | Credentials |
| 10 | SMTP configuration guide | PDF |

### 9.2 Feature Checklist

| Module | Features | Status |
|--------|----------|:------:|
| **Public Website** | Home, Features, Pricing, Contact | ⬜ |
| **Authentication** | Email/Password, Google OAuth, Forgot Password | ⬜ |
| **Admin Dashboard** | Users, Plans, Reports, SMTP, Analytics | ⬜ |
| **Lab Dashboard** | Albums, Studios, Analytics, Subscription | ⬜ |
| **Studio Dashboard** | My Albums, Lab Shared, Bookings, Analytics | ⬜ |
| **Payment System** | Razorpay, UPI, Cards, Subscriptions | ⬜ |
| **Flipbook Viewer** | Page-flip, Music, Sound toggle, Fullscreen | ⬜ |
| **Image Processing** | Auto-crop, Manual crop, Batch upload | ⬜ |
| **PDF Processing** | Upload, Extract, Preview, Create album | ⬜ |
| **Email Automation** | 7 email types, SMTP config, Templates | ⬜ |
| **Auto Deletion** | 30-day cleanup, CDN deletion, Notifications | ⬜ |
| **Analytics** | QR scans, Country reports, Usage tracking | ⬜ |

### 9.3 Post-Delivery Support

| Support | Duration | Coverage |
|---------|----------|----------|
| Bug fixes | 15 days | Critical & major bugs |
| Technical support | 15 days | WhatsApp/Email |
| Payment issues | 15 days | Razorpay configuration |
| Email issues | 15 days | SMTP configuration |
| Minor changes | Not included | Chargeable |
| New features | Not included | Separate quotation |

---

## 10. Terms & Conditions

### 10.1 General Terms

1. This proposal is valid for **30 days** from the date of issue.
2. Prices are in **Indian Rupees (₹)** and inclusive of all taxes.
3. Any changes to scope require a **change request** and may affect timeline/cost.
4. Client must provide content within **3 days** of request.
5. Timeline starts from first milestone payment.

### 10.2 Intellectual Property

1. Source code remains property of **Visainnovations**.
2. Client receives full rights to **use the deployed application**.
3. Client owns all uploaded content (images, albums, user data).
4. Visainnovations may showcase project in portfolio.
5. Third-party libraries subject to their respective licenses.

### 10.3 Payment & Subscription System

1. **Razorpay integration** included for automated billing.
2. Platform supports **event-based subscription plans** (9 plans total).
3. Labs and Studios pay for their **own subscriptions**.
4. Labs can create albums for studios using **Lab's event quota**.
5. Payment collection via Razorpay (2% transaction fee applies - paid by platform owner).

### 10.4 Data Management

1. User data auto-deletes **30 days after subscription expiry**.
2. Users receive **warning email 5 days before expiry**.
3. Users receive **deletion confirmation email** after data is removed.
4. Account is preserved for re-subscription with fresh start.

### 10.5 Confidentiality

1. Both parties agree to keep project details confidential.
2. User data will not be shared with third parties.
3. NDA can be signed upon request.

### 10.6 Warranty

1. **15 days** free bug-fix support after deployment.
2. Bugs due to client modifications are not covered.
3. Server/hosting issues are not covered.
4. Razorpay/Google service outages are not covered.
5. SMTP server issues (if using client's SMTP) are not covered.

### 10.7 What's NOT Included

- ❌ SMS/WhatsApp notifications
- ❌ Mobile applications (iOS/Android)
- ❌ Video album support
- ❌ AI features (beyond auto-crop)
- ❌ Multi-language support
- ❌ White-label customization
- ❌ Third-party integrations (except Razorpay & Google OAuth)

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

### A. Complete Flow Diagrams

#### A.1 Lab Creates Album for Studio

```
┌─────────────────────────────────────────────────────────────────────────┐
│                   LAB CREATES ALBUM FOR STUDIO                           │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│  Lab Dashboard → [+ Create Album]                                       │
│         │                                                               │
│         ▼                                                               │
│  Select/Add Studio Details                                              │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │  ○ Existing Studio: [Dropdown - Previously added studios]       │   │
│  │                                                                  │   │
│  │  ○ Add New Studio:                                              │   │
│  │    Studio Name: [________________]                              │   │
│  │    Email:       [________________]                              │   │
│  │    Phone:       [________________]                              │   │
│  │    City:        [________________]                              │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│         │                                                               │
│         ▼                                                               │
│  Fill Album Details                                                     │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │  Album Name:    [Wedding - Raj & Priya        ]                 │   │
│  │  Client Name:   [Raj Kumar                    ]                 │   │
│  │  Client Phone:  [9876543210                   ]                 │   │
│  │  Event Date:    [15-Feb-2026                  ]                 │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│         │                                                               │
│         ▼                                                               │
│  Upload Images (Max 100) OR Upload PDF                                  │
│         │                                                               │
│         ▼                                                               │
│  [Create Album] → Uses Lab's Event Quota (-1 Event)                    │
│         │                                                               │
│         ├─── Studio Email NEW ───► Create Account                      │
│         │                          + Email Login Credentials            │
│         │                                                               │
│         └─── Studio Email EXISTS ─► Email "Album Shared" Notification  │
│                                                                         │
│  ═══════════════════════════════════════════════════════════════════   │
│                                                                         │
│  IN STUDIO DASHBOARD (After Login):                                     │
│                                                                         │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │                                                                  │   │
│  │  ┌─────────────────┐    ┌─────────────────┐                     │   │
│  │  │  📁 My Albums   │    │  🔗 Lab Shared  │                     │   │
│  │  │    (Tab 1)      │    │     (Tab 2)     │                     │   │
│  │  └─────────────────┘    └─────────────────┘                     │   │
│  │                                                                  │   │
│  │  Tab 1: Albums created by Studio (uses Studio's quota)          │   │
│  │  Tab 2: Albums created by Lab FOR this Studio                   │   │
│  │                                                                  │   │
│  │  Lab Shared Albums:                                              │   │
│  │  ┌─────────────────────────────────────────────────────────┐    │   │
│  │  │ 📷 Wedding - Raj & Priya                                 │    │   │
│  │  │    From: Creative Labs | Date: 15-Feb-2026              │    │   │
│  │  │    Views: 234 | [View] [Share QR] [Download QR]         │    │   │
│  │  └─────────────────────────────────────────────────────────┘    │   │
│  │                                                                  │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
│  Studio can share QR with their customer (end client)                  │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

#### A.2 Registration & Payment Flow

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    REGISTRATION & PAYMENT FLOW                           │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│  NEW USER REGISTRATION                                                  │
│  ═════════════════════                                                  │
│                                                                         │
│  1. Visit Website → Click "Sign Up"                                     │
│         │                                                               │
│         ▼                                                               │
│  2. Choose Sign Up Method                                               │
│     ┌─────────────────────────────────────────────┐                    │
│     │  ○ Sign up with Email                       │                    │
│     │  ○ Sign up with Google                      │                    │
│     └─────────────────────────────────────────────┘                    │
│         │                                                               │
│         ▼                                                               │
│  3. Fill Registration Form                                              │
│     ┌─────────────────────────────────────────────┐                    │
│     │  Name:     [________________]               │                    │
│     │  Email:    [________________]               │                    │
│     │  Phone:    [________________]               │                    │
│     │  Country:  [India          ▼]               │                    │
│     │  Password: [________________]               │                    │
│     └─────────────────────────────────────────────┘                    │
│         │                                                               │
│         ▼                                                               │
│  4. Select User Type                                                    │
│     ┌─────────────────────────────────────────────┐                    │
│     │  ○ I'm a Photo Studio                       │                    │
│     │  ○ I'm a Lab / Reseller                     │                    │
│     └─────────────────────────────────────────────┘                    │
│         │                                                               │
│         ▼                                                               │
│  5. Select Plan (based on user type)                                   │
│     ┌─────────────────────────────────────────────┐                    │
│     │  STUDIO PLANS:          LAB PLANS:          │                    │
│     │  ○ 25 Events - ₹1,250   ○ 500 Events - ₹10K │                    │
│     │  ○ 50 Events - ₹2,000   ○ 1000 Events - ₹19K│                    │
│     │  ○ 100 Events - ₹3,000  ○ 3000 Events - ₹54K│                    │
│     │  ○ 250 Events - ₹6,250  ○ 5000 Events - ₹85K│                    │
│     │                         ○ 10000 Events-₹1.5L│                    │
│     └─────────────────────────────────────────────┘                    │
│         │                                                               │
│         ▼                                                               │
│  6. Pay via Razorpay                                                   │
│     ┌─────────────────────────────────────────────┐                    │
│     │  Amount: ₹XXXX                              │                    │
│     │                                             │                    │
│     │  ○ UPI (GPay, PhonePe, Paytm)              │                    │
│     │  ○ Credit/Debit Card                        │                    │
│     │  ○ Net Banking                              │                    │
│     │                                             │                    │
│     │  [Pay Now]                                  │                    │
│     └─────────────────────────────────────────────┘                    │
│         │                                                               │
│         ▼                                                               │
│  7. Payment Success                                                     │
│     → Razorpay Webhook triggers                                        │
│     → Account auto-activated                                           │
│     → Welcome email sent                                               │
│         │                                                               │
│         ▼                                                               │
│  8. Redirect to Dashboard (Ready to create albums!)                    │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

#### A.3 Subscription Expiry & Data Deletion Flow

```
┌─────────────────────────────────────────────────────────────────────────┐
│                 SUBSCRIPTION EXPIRY & DATA DELETION                      │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│  TIMELINE                                                               │
│  ════════                                                               │
│                                                                         │
│  Day 1        Day 360       Day 365        Day 395                     │
│    │             │             │              │                         │
│    ▼             ▼             ▼              ▼                         │
│  ┌────┐      ┌────────┐    ┌────────┐    ┌────────┐                   │
│  │ 🟢 │      │  📧    │    │  🔴    │    │  🗑️   │                    │
│  │START│     │WARNING │    │EXPIRED │    │DELETED │                   │
│  └────┘      └────────┘    └────────┘    └────────┘                   │
│    │             │             │              │                         │
│  Account      Email:        Access         Email:                      │
│  Active      "5 days       Blocked        "Your data                   │
│              left!"                        deleted"                     │
│                                                                         │
│  ═══════════════════════════════════════════════════════════════════   │
│                                                                         │
│  EMAIL 1: EXPIRY WARNING (Day 360)                                     │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │  📧 Subject: Your FXFlipbook subscription expires in 5 days!    │   │
│  │                                                                  │   │
│  │  Hi [Name],                                                      │   │
│  │                                                                  │   │
│  │  Your subscription will expire on [Date].                        │   │
│  │  You have [X] events remaining.                                  │   │
│  │                                                                  │   │
│  │  Renew now to keep your albums and data safe!                   │   │
│  │                                                                  │   │
│  │  [Renew Now - ₹XXXX]                                            │   │
│  │                                                                  │   │
│  │  If you don't renew:                                            │   │
│  │  • Your account will be locked on [Expiry Date]                 │   │
│  │  • All data will be deleted after 30 days                       │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
│  ═══════════════════════════════════════════════════════════════════   │
│                                                                         │
│  WHAT HAPPENS ON EXPIRY (Day 365):                                     │
│  • User cannot login to dashboard                                       │
│  • Existing albums still viewable (QR codes work)                      │
│  • Cannot create new albums                                            │
│  • 30-day grace period begins                                          │
│                                                                         │
│  ═══════════════════════════════════════════════════════════════════   │
│                                                                         │
│  IF USER RENEWS (Before Day 395):                                      │
│  • Access restored immediately                                          │
│  • All data preserved                                                   │
│  • Subscription extended by 1 year                                     │
│                                                                         │
│  ═══════════════════════════════════════════════════════════════════   │
│                                                                         │
│  EMAIL 2: DATA DELETED (Day 395)                                       │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │  📧 Subject: Your FXFlipbook data has been deleted              │   │
│  │                                                                  │   │
│  │  Hi [Name],                                                      │   │
│  │                                                                  │   │
│  │  Your subscription expired 30 days ago.                          │   │
│  │  As per our policy, all your data has been deleted:             │   │
│  │                                                                  │   │
│  │  • [X] Albums deleted                                           │   │
│  │  • [Y] Images removed                                           │   │
│  │  • All QR codes deactivated                                     │   │
│  │                                                                  │   │
│  │  Your account is still active. Subscribe again to start fresh!  │   │
│  │                                                                  │   │
│  │  [Subscribe Now]                                                 │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
│  ═══════════════════════════════════════════════════════════════════   │
│                                                                         │
│  DATA DELETED (Day 395):                                               │
│  ✗ All Albums                                                          │
│  ✗ All Images (from CDN)                                               │
│  ✗ All Orders                                                          │
│  ✗ All QR Codes                                                        │
│  ✗ All Bookings                                                        │
│  ✗ Studio associations (for Labs)                                      │
│                                                                         │
│  DATA KEPT:                                                            │
│  ✓ Account (email, name, phone)                                        │
│  ✓ Can re-subscribe anytime                                            │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

### B. Email Templates Summary

| # | Email Type | Trigger | Key Content |
|---|------------|---------|-------------|
| 1 | **Welcome** | Registration + Payment | Login details, getting started guide, plan details |
| 2 | **Expiry Warning** | 5 days before expiry | Renewal reminder, payment link, data warning |
| 3 | **Data Deleted** | 30 days after expiry | Deletion confirmation, re-subscribe link |
| 4 | **Studio Credentials** | Lab adds new studio | Auto-generated password, login link |
| 5 | **Album Shared** | Lab shares with existing studio | Album details, view link |
| 6 | **Password Reset** | Forgot password request | Reset link (valid 1 hour) |
| 7 | **Payment Confirmation** | Successful payment | Invoice, plan details, validity |

### C. Admin Dashboard Overview

```
┌─────────────────────────────────────────────────────────────────────────┐
│                        ADMIN DASHBOARD                                   │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│  📊 PLATFORM OVERVIEW                                                   │
│  ┌────────────┐  ┌────────────┐  ┌────────────┐  ┌────────────┐       │
│  │ Total Labs │  │  Total     │  │   Total    │  │  Revenue   │       │
│  │            │  │  Studios   │  │   Albums   │  │ This Month │       │
│  │    125     │  │    850     │  │   12,500   │  │  ₹4.5L     │       │
│  │ +12 this mo│  │ +45 this mo│  │ +1.2K this │  │ +15% ↑     │       │
│  └────────────┘  └────────────┘  └────────────┘  └────────────┘       │
│                                                                         │
│  🌍 COUNTRY-WISE REPORT                                                │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │  Country     │ Labs │ Studios │ Albums  │ Revenue   │ % Share  │   │
│  │  ────────────────────────────────────────────────────────────── │   │
│  │  🇮🇳 India    │  110 │   780   │  11,200 │ ₹3.8L    │   84%    │   │
│  │  🇦🇪 UAE      │    8 │    40   │     650 │ ₹35K     │    8%    │   │
│  │  🇺🇸 USA      │    4 │    18   │     400 │ ₹22K     │    5%    │   │
│  │  🇬🇧 UK       │    3 │    12   │     250 │ ₹13K     │    3%    │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
│  📈 SUBSCRIPTION ANALYTICS                                             │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │  Plan             │ Active │ Expiring Soon │ Expired │ Revenue  │   │
│  │  ─────────────────────────────────────────────────────────────  │   │
│  │  Studio Plans     │   720  │      45       │    85   │ ₹18L     │   │
│  │  Lab Plans        │   105  │      12       │     8   │ ₹42L     │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
│  ⚙️ QUICK ACTIONS                                                       │
│  ┌──────────────┐ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐  │
│  │ Manage Plans │ │ SMTP Config  │ │ Email        │ │ View All     │  │
│  │              │ │              │ │ Templates    │ │ Users        │  │
│  └──────────────┘ └──────────────┘ └──────────────┘ └──────────────┘  │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## Acceptance

By signing below, the client agrees to the terms outlined in this proposal.

| | Client | Visainnovations |
|---|--------|-----------------|
| **Name** | P. Manikandam | _________________ |
| **Designation** | _________________ | Project Lead |
| **Date** | _________________ | January 20, 2026 |
| **Signature** | _________________ | _________________ |

---

### Payment Confirmation

| Milestone | Amount (₹) | Date | Mode | Signature |
|-----------|------------|------|------|-----------|
| Milestone 1 (40%) | ₹54,000 | | | |
| Milestone 2 (35%) | ₹47,250 | | | |
| Milestone 3 (25%) | ₹33,750 | | | |
| **Total** | **₹1,35,000** | | | |

---

<div align="center">

### 💰 Investment Summary

| | |
|---|---|
| **Total Project Cost** | **₹1,35,000** |
| **Project Duration** | **65 Days** |
| **Market Value** | ₹2,85,000+ |
| **Your Savings** | ₹1,50,000 (53%) |

---

### Key Highlights

✅ **Razorpay Integration** - UPI, Cards, Net Banking, Subscriptions  
✅ **Google Sign-in** - Easy one-click authentication  
✅ **Event-Based Plans** - 9 Plans (4 Studio + 5 Lab)  
✅ **Lab-Studio Workflow** - Album sharing with auto-notifications  
✅ **Auto Data Management** - Expiry warnings & 30-day deletion  
✅ **Email Automation** - 7 automated email types  
✅ **Country-wise Reports** - Geographic analytics for Admin  
✅ **PDF to Album** - Upload PDF, extract images, create album  
✅ **Smart Cropping** - Auto-crop + Manual editor  

---

**Thank you for considering Visainnovations!**

*Let's build an amazing SaaS platform together.*

---

© 2026 Visainnovations. All Rights Reserved.

</div>