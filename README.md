# privacyIDEA Docker Setup (MFA / OTP / IAM Demo)

This repository demonstrates a complete **privacyIDEA deployment using Docker Compose**
with focus on **Multi-Factor Authentication (MFA)**, **user management**, and **security policies**.

The project is intended as a **hands-on IAM / Security portfolio project**.

---

## 🚀 Features

- Docker-based deployment of privacyIDEA
- MariaDB backend
- Secure handling of secrets (ignored in Git)
- OTP-based authentication (TOTP / HOTP)
- SQL-based editable user store
- Policy-driven access control

---

## 🧱 Architecture Overview

- **privacyIDEA** – MFA / OTP server
- **MariaDB** – user and token storage
- **Docker Compose** – orchestration
- **SQL Resolver** – editable user store
- **Separate Realm** – isolation of user groups

---

## 👤 User Management

- Internal `/etc/passwd` resolver (read-only, system users)
- SQL resolver (editable user store)
- Separate realm for SQL-based users

📄 See:  
`docs/sql-resolver.md`

---

## 🔑 Token Enrollment

- HOTP / TOTP tokens
- Token assignment to users
- QR code enrollment
- PIN + OTP authentication flow

📄 See:  
`docs/token-enrollment.md`

---

## 📜 Policies

- WebUI access control
- Self-service permissions
- Token enrollment restrictions

📄 See:  
`docs/policies.md`

---

## 🐳 Docker Setup

```bash
docker compose up -d
