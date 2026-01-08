# SQL Resolver Configuration

This document describes the setup of an **SQL-based user resolver** in privacyIDEA.

The SQL resolver is used as an **editable user store**, unlike the internal `/etc/passwd` resolver which is read-only.

---

## 🎯 Purpose

The SQL resolver enables:

- Creation and management of users inside privacyIDEA
- Separation of system users and authentication users
- Flexible IAM architecture using realms

---

## 🗄 Database Backend

- Database: MariaDB
- Managed via Docker
- Credentials are injected via Docker secrets
- No credentials are stored in Git

---

## ⚙️ Resolver Configuration

Resolver type:
- **SQL Resolver**

Typical configuration fields:

- Database type: MariaDB / MySQL
- Host: `db`
- Database name: `pi`
- User table: `users`
- Username column: `username`
- Password column: `password`

> The resolver is configured via the privacyIDEA WebUI under  
> **Config → Users → Resolvers**

---

## 🌐 Realm Setup

A dedicated realm is created for SQL users:

- Realm name example: `sqlrealm`
- Resolver: `sqlresolver`

This allows:
- Applying policies per user group
- Separating internal/system users from IAM users

---

## 🔐 Security Notes

- SQL users are isolated from OS users
- Resolver credentials are handled via Docker secrets
- Principle of least privilege is applied

---

## ✅ Result

The SQL resolver provides a **clean and manageable IAM user base**, suitable for MFA enrollment and self-service operations.
