# One-Click Hosting Account Setup
**Automated WHM Account Creation & cPanel Email Provisioning with Persistent Recording**

## Overview
This service provisions cPanel hosting accounts via WHM, generates user-level API tokens, creates email accounts, and records all relevant metadata into PostgreSQL. It’s designed for business onboarding: one-click account creation, billing integration, and auditability.

## Features
- WHM API-driven cPanel account creation (packages, domains, contact email).  
- Automated generation of user-level cPanel API tokens.  
- Email account provisioning via cPanel UAPI.  
- Persistent recording of hosting/email provisioning responses.  
- Schema migrations with Knex.js for safe evolution.  
- Extensible for billing, invoicing, suspension/termination workflows.

## Prerequisites
- Node.js (16+ recommended)  
- PostgreSQL  
- WHM/cPanel server with API token access  
- Environment capable of HTTPS requests to WHM/cPanel endpoints  

## Environment Variables

```env
# WHM root/reseller access
WHM_HOST=https://your-whm-server:2087
WHM_API_TOKEN=
