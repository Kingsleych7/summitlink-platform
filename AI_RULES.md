# Summitlink Telecom Platform
# AI Development Rules

Version: 1.0

Status: Active

Purpose:
This document defines the rules every AI coding assistant must follow when contributing to the Summitlink Telecom Platform.

These rules apply to Cursor, GitHub Copilot, ChatGPT, Claude Code, and any future AI development tools.

---

# Project Overview

Summitlink Telecom is an enterprise digital infrastructure platform.

It combines:

- Telecommunications
- Fintech
- Communication APIs (CPaaS)
- Value Added Services (VAS)
- Developer Platform

This is NOT a demo project.

This is a production-grade platform.

---

# Golden Rules

Always improve existing code.

Never rewrite working features without instruction.

Never duplicate functionality.

Always build reusable components.

Always write production-quality code.

Always use TypeScript best practices.

Always maintain scalability.

---

# Source of Truth

The following documents define the project:

README.md

PRD.md

AI_RULES.md

ARCHITECTURE.md

DATABASE.md

API_SPEC.md

DESIGN_SYSTEM.md

ROADMAP.md

When conflicts occur:

PRD.md wins.

---

# Technology Stack

Frontend

Next.js 16

React

TypeScript

Tailwind CSS

shadcn/ui

Framer Motion

Backend

Next.js API Routes

Node.js

Database

Neon PostgreSQL

Deployment

Vercel

Repository

GitHub

---

# Database Rules

The project uses Neon PostgreSQL.

Never generate MongoDB code.

Never introduce another database.

Never create duplicate schemas.

Respect the existing database structure.

Reuse existing models and queries whenever possible.

---

# Backend Rules

Never create duplicate API routes.

Reuse existing services.

Separate business logic from UI.

Use proper error handling.

Validate all inputs.

Return consistent API responses.

Never hardcode sensitive information.

Always use environment variables.

---

# Frontend Rules

Use App Router.

Use TypeScript.

Use Tailwind CSS.

Use shadcn/ui components.

Use reusable layouts.

Create accessible interfaces.

Avoid unnecessary dependencies.

Support desktop, tablet, and mobile devices.

---

# UI Philosophy

Premium

Enterprise

Modern

Minimal

Professional

Fast

Accessible

Elegant

The platform should resemble enterprise SaaS products, not a basic VTU website.

---

# Brand Rules

Primary

Deep Indigo / Violet

Secondary

Warm Gold / Amber

Use generous spacing.

Rounded corners.

Soft shadows.

Subtle gradients.

Professional typography.

---

# Logo Rules

Concept A

Mountain Peak

Gold Node

Signal Waves

Always preserve clear space around the logo.

Never distort or stretch the logo.

---

# Component Rules

Always create reusable components.

Prefer composition over duplication.

Create components inside:

src/components

Examples:

Navbar

Footer

Hero

FeatureCard

PricingCard

DashboardCard

WalletCard

AnalyticsCard

DeveloperCard

FAQ

Timeline

StatusBadge

Notification

Modal

Dialog

Button

Input

Table

Chart

---

# Folder Structure

Follow this structure:

src/

app/

components/

lib/

hooks/

services/

types/

utils/

styles/

config/

Never create random folders.

---

# Authentication Rules

Extend the existing authentication system.

Never replace authentication.

Never create duplicate login pages.

Never generate fake authentication.

---

# Wallet Rules

Reuse the existing wallet system.

Do not replace transaction logic.

Do not recreate payment services.

Maintain transaction integrity.

---

# CPaaS Rules

Support:

SMS

OTP

Bulk Messaging

WhatsApp

Voice

Future APIs should follow the same architecture.

---

# Fintech Rules

Support:

Wallet

Deposits

Collections

Merchant Payments

Future:

Transfers

Virtual Accounts

Settlement

Never generate banking features without explicit instruction.

---

# VAS Rules

Support:

Airtime

Data

Electricity

Cable

Education

Future services must use the same service architecture.

---

# Developer Portal Rules

Developer Portal must include:

API Documentation

Authentication

API Keys

SDKs

Webhooks

Analytics

Status Page

Sandbox

Never use placeholder API documentation.

---

# Dashboard Rules

Customer Dashboard

Business Dashboard

Admin Dashboard

Each dashboard must have its own layout.

Never mix admin and customer functionality.

---

# Performance Rules

Lazy load large components.

Optimize images.

Minimize JavaScript.

Avoid unnecessary re-renders.

Write efficient database queries.

Keep bundle size small.

---

# Security Rules

Validate every request.

Sanitize user input.

Protect secrets.

Use HTTPS.

Prevent SQL injection.

Protect API keys.

Never expose sensitive credentials.

---

# Code Quality

Write readable code.

Use meaningful names.

Keep functions small.

Avoid duplicated logic.

Comment only where necessary.

Prefer maintainability over cleverness.

---

# AI Assistant Responsibilities

Cursor

Backend

Architecture

Database

Authentication

Refactoring

Integrations

Performance

Testing

v0

Landing Pages

Marketing Pages

Reusable UI Components

Layouts

Animations

Visual Design

Do not generate production backend logic.

---

# Long-Term Goal

Every contribution should move Summitlink closer to becoming Africa's leading digital infrastructure platform.

Code should be scalable enough to support millions of users without requiring major architectural redesign.
