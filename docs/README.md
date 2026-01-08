# Documentation

This folder contains documentation for the privacyIDEA Docker setup
and configuration used in this portfolio project.
# privacyIDEA Docker Setup (Portfolio Project)

This repository contains a complete Docker-based setup of **privacyIDEA**
used as an Identity & Access Management (IAM) and Multi-Factor Authentication (MFA) solution.

The project demonstrates:
- secure containerized deployment
- database-backed user management
- token enrollment (TOTP/HOTP)
- policy configuration
- API-based authentication testing
- secure handling of secrets

---

## 🔐 What is privacyIDEA?

privacyIDEA is an open-source authentication system
for managing two-factor authentication (2FA/MFA),
OTP tokens, policies, and authentication flows.

---

## 🧱 Architecture Overview

Components:
- **privacyIDEA** (application container)
- **MariaDB** (database backend)
- **Docker Compose** orchestration
- **SQL User Resolver** (editable user store)
- **TOTP tokens** for MFA
- **REST API** authentication validation

---

## 🚀 How to Run

```bash
cd deploy/docker
docker compose up -d
