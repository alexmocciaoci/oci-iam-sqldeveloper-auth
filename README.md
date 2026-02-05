# oci-iam-sqldeveloper-auth

# Enterprise OCI IAM DB Token Authentication with SQL Developer and JDBC

This repository documents a real-world implementation of Oracle Cloud Infrastructure (OCI) IAM Database Token authentication with SQL Developer and JDBC in enterprise environments protected by NTLM proxies and enforced mutual TLS (mTLS).

The content is based on hands-on production experience and provides a reproducible reference architecture for secure database access in constrained corporate networks.

---

## 📌 Scope and Objectives

The primary objectives of this project are:

- Demonstrate practical usage of OCI IAM DB Token authentication
- Provide a validated workaround for enterprise proxy environments
- Document secure JDBC and SQL Developer configuration patterns
- Enable reproducible deployment in regulated environments

---

## 🏗 Architecture Overview

The authentication flow implemented in this project follows this model:

1. OCI CLI generates a short-lived IAM database token
2. The token is stored in a secured local cache
3. JDBC extensions consume the external token
4. SQL Developer loads the custom JDBC configuration
5. Oracle Net enforces mTLS and token-based authentication

This decoupled architecture enables secure database access even in NTLM-protected networks.

---

## Documentation

- Technical Guide (PDF): [Download](docs/OCI_IAM_DB_Token_SQLDeveloper_Enterprise.pdf)
- Technical Guide (docx): [Download](docs/OCI_IAM_DB_Token_SQLDeveloper_Enterprise.docx)

## Architecture Diagram

![IAM DB Token Authentication Flow](images/iam_sqldeveloper_sequence.png)

Unified enterprise sequence diagram illustrating interactive IAM login, session-based OCI CLI fallback, manual token profile usage, NTLM proxy mediation, and mutual TLS enforcement for SQL Developer connectivity.


## ⚙ Repository Structure


