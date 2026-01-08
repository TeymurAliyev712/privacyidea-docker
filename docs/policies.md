# Policies Configuration

This document describes the **policy-based access control** used in this privacyIDEA deployment.

Policies are a core concept in privacyIDEA and define **who can do what, and when**.

---

## 🎯 Policy Goals

- Restrict administrative access
- Control self-service features
- Secure token enrollment
- Enforce MFA best practices

---

## 🖥 WebUI Access Policies

Example controls:

- Limit WebUI access to specific realms
- Restrict administrative functions
- Enforce login mode via privacyIDEA

Scope examples:
- `webui`
- `admin`

---

## 👤 Self-Service Policies

Self-service policies allow users to:

- Enroll their own tokens
- View assigned tokens
- Reset PIN (if allowed)

Controls include:
- Allowed token types
- Realm-based restrictions
- User-specific permissions

---

## 🔑 Token Policies

Token-related policies define:

- Which token types are allowed
- Whether PIN is mandatory
- Maximum number of tokens per user

These policies ensure consistent MFA enforcement.

---

## ⏱ Session & Security Policies

Additional controls:

- WebUI session timeout
- Automatic logout
- JWT validity duration

These reduce the risk of session hijacking.

---

## 🔐 Security Principles

- Least privilege
- Explicit allow rules
- Realm separation
- Policy-driven access

---

## ✅ Result

Policies provide **fine-grained IAM control**, ensuring security, usability, and scalability.
