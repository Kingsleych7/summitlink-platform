# Summitlink Telecom Platform - AI Development Rules

## Project Overview

Summitlink Telecom LTD is an African Digital Infrastructure Platform combining:

- Telecommunications (CPaaS)
- Fintech Infrastructure
- Value Added Services (VAS)
- Developer APIs

This project is NOT a simple VTU website.

It is an enterprise SaaS platform.

---

# Source of Truth

Do not replace existing working implementations.

Always extend existing code.

Never generate placeholder production logic when working features already exist.

---

# Technology Stack

Framework

- Next.js 16 (App Router)
- React
- TypeScript

Styling

- Tailwind CSS
- shadcn/ui
- Framer Motion

Database

- Neon PostgreSQL

ORM / Database Layer

- Use the project's existing database layer.
- Do not introduce a different ORM or database unless explicitly requested.

Authentication

- Extend the existing authentication system.
- Do not generate a second auth system.

Backend

- Reuse existing API routes.
- Do not duplicate APIs.

Deployment

- Vercel

---

# Architecture Principles

Build reusable components.

Keep components modular.

Separate UI from business logic.

Keep API logic inside API routes.

Do not hardcode production data.

Avoid duplicated code.

Prefer composition over repetition.

---

# Existing Features

The project already includes or is building:

- User Authentication
- Wallet
- Airtime
- Data
- Electricity
- Cable TV
- Transactions
- Customer Dashboard
- Admin Dashboard
- Payment Integration
- API Infrastructure

Never recreate these from scratch.

Extend them.

---

# Platform Modules

## Summitlink Connect

Communication APIs

- SMS API
- OTP
- Bulk Messaging
- WhatsApp
- Voice API

---

## Summitlink Pay

Financial Infrastructure

- Wallet
- Deposits
- Merchant Payments
- Collections
- Transaction History

Future:

- Transfers
- Virtual Accounts
- Payment Links

---

## Summitlink VAS

Digital Services

- Airtime
- Data
- Electricity
- Cable
- Education

Future:

- Gift Cards
- Insurance
- Travel

---

## Summitlink Developers

Developer Portal

- API Documentation
- API Keys
- SDKs
- Webhooks
- Analytics

---

# UI Guidelines

Theme

Premium Enterprise SaaS

Primary Color

Deep Indigo / Violet

Secondary Accent

Warm Gold / Amber

Style

Modern

Minimal

Elegant

Professional

Responsive

Accessible

Avoid bright telecom colours similar to MTN or Airtel.

---

# Logo

Use Concept A.

Mountain Peak

Gold Node

Signal Waves

Modern Minimal

---

# AI Builder Rules

If generating UI:

Create reusable React components.

Use shadcn/ui.

Use Tailwind.

Use Framer Motion carefully.

Do not generate fake backend logic.

Do not generate mock databases.

---

# Cursor Rules

Cursor is responsible for:

Backend

Database

Authentication

Business Logic

Integrations

API Routes

Refactoring

Architecture

---

# v0 Rules

v0 is responsible for:

Landing Pages

Marketing Pages

Reusable UI Components

Animations

Layouts

Cards

Sections

Do not generate production backend code.

---

# Code Quality

Production Ready

Type Safe

Reusable

Readable

Scalable

Maintainable

Enterprise Quality

---

# Long-Term Goal

Build one scalable platform that powers:

Corporate Website

Customer Dashboard

Developer Portal

Admin Dashboard

Fintech

CPaaS

Value Added Services

Future AI Features

without requiring architectural redesign.
