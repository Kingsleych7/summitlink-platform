# Summitlink Telecom Platform
# Database Design Document

Version: 1.0

Database:
Neon PostgreSQL

Status:
Active Development

---

# Database Philosophy

The database is designed for:

- Scalability
- Security
- High Performance
- Financial Integrity
- Auditability

Every financial transaction must be traceable.

---

# Core Tables

## users

Purpose

Stores registered users.

Columns

id

uuid

Primary Key

---

full_name

text

---

email

text

Unique

---

phone

text

Unique

---

password_hash

text

---

role

customer

business

developer

admin

super_admin

---

status

active

pending

suspended

---

email_verified

boolean

---

phone_verified

boolean

---

created_at

timestamp

updated_at

timestamp

---

## wallets

Purpose

Every user owns one wallet.

Columns

id

uuid

user_id

FK → users

balance

decimal

currency

NGN

status

active

created_at

updated_at

---

## wallet_transactions

Purpose

Complete wallet ledger.

Columns

id

wallet_id

user_id

reference

type

credit

debit

amount

balance_before

balance_after

provider

status

description

created_at

Never delete records.

---

## deposits

Purpose

Wallet funding.

Columns

id

user_id

reference

provider

amount

status

payment_reference

created_at

---

## api_keys

Purpose

Developer authentication.

Columns

id

user_id

key

secret

status

last_used

created_at

---

## sms_logs

Purpose

Every SMS request.

Columns

id

user_id

recipient

sender_id

message

provider

status

cost

reference

created_at

---

## otp_requests

Purpose

OTP history.

Columns

id

user_id

phone

code_hash

purpose

expires_at

verified

created_at

---

## airtime_orders

Purpose

Airtime purchases.

Columns

id

user_id

network

phone

amount

reference

provider

status

created_at

---

## data_orders

Purpose

Internet bundles.

Columns

id

user_id

network

plan

phone

amount

status

reference

created_at

---

## electricity_orders

Purpose

Electricity payments.

Columns

id

user_id

meter_number

distribution_company

amount

token

reference

status

created_at

---

## cable_orders

Purpose

Cable TV.

Columns

id

user_id

provider

smartcard_number

package

amount

reference

status

created_at

---

## education_orders

Purpose

Education PINs.

Columns

id

user_id

provider

quantity

amount

reference

status

created_at

---

## notifications

Purpose

Platform notifications.

Columns

id

user_id

title

message

type

read

created_at

---

## audit_logs

Purpose

Track important system actions.

Columns

id

user_id

action

ip_address

device

metadata

created_at

Never modify audit logs.

---

## support_tickets

Purpose

Customer support.

Columns

id

user_id

subject

category

priority

status

assigned_to

created_at

updated_at

---

## service_status

Purpose

Platform health.

Columns

id

service

status

message

updated_at

---

# Relationships

users

↓

wallets

↓

wallet_transactions

users

↓

airtime_orders

users

↓

data_orders

users

↓

electricity_orders

users

↓

cable_orders

users

↓

education_orders

users

↓

notifications

users

↓

api_keys

users

↓

support_tickets

---

# Indexes

Index:

email

phone

reference

user_id

created_at

status

provider

---

# Security

Passwords:

bcrypt

Sensitive data:

Encrypted where necessary.

Never store plain passwords.

Never store payment secrets.

---

# Future Tables

merchant_accounts

settlements

transfers

virtual_accounts

webhooks

api_usage

voice_logs

whatsapp_logs

email_logs

partner_accounts

referrals

affiliate_program

fraud_cases

risk_scores

---

# Database Rules

Use UUIDs.

Use foreign keys.

Use transactions for financial operations.

Never delete financial history.

Soft delete where appropriate.

All timestamps should use UTC.

Every financial record must have a unique reference.

Database changes must be version-controlled through migrations.

---

# Long-Term Goal

The database should support millions of users, high transaction volumes, enterprise APIs, and future financial products without requiring a complete redesign.
