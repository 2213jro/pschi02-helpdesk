# Deployment Guide

## Project Objective

Deploy a student-to-student IT support platform that provides hands-on experience with ticket management, troubleshooting, documentation, and support workflows.

## Infrastructure Overview

### Hosting Provider

* DigitalOcean

### Operating System

* Rocky Linux

### Web Stack

* Apache
* PHP
* MariaDB

### Application

* osTicket

### DNS and Security

* Cloudflare

---

## Deployment Process

### Phase 1: Server Provisioning

A virtual private server (VPS) was deployed through DigitalOcean and configured with Rocky Linux.

Tasks completed:

* Initial server deployment
* System updates
* SSH access configuration
* Basic security hardening

---

### Phase 2: Web Server Installation

Apache was installed and configured to host the application.

Tasks completed:

* Apache installation
* Service configuration
* Firewall configuration
* Web service validation

---

### Phase 3: Database Deployment

MariaDB was installed to support the osTicket application.

Tasks completed:

* Database installation
* Database initialization
* Application database creation
* Connectivity testing

---

### Phase 4: PHP Configuration

Required PHP packages and modules were installed to support osTicket functionality.

Tasks completed:

* PHP installation
* Required module installation
* Application compatibility verification

---

### Phase 5: osTicket Deployment

The osTicket application was deployed and configured.

Tasks completed:

* Application installation
* Web-based setup
* Administrative account creation
* Initial configuration

---

### Phase 6: DNS Configuration

Cloudflare was used to manage DNS records and route traffic to the DigitalOcean server.

Tasks completed:

* Domain configuration
* DNS record management
* Traffic routing validation

---

### Phase 7: Platform Development

The platform was expanded beyond a basic ticketing system.

Features implemented:

* Student onboarding process
* Knowledge base articles
* Tier 1 support workflows
* Tier 2 escalation procedures
* User account management

---

## Lessons Learned

This project provided practical experience with:

* Linux Administration
* Apache Web Server Management
* Database Administration
* DNS Management
* Cloud Hosting
* Ticketing Systems
* Technical Documentation
* Troubleshooting
* User Support Operations

## Current Status

The platform is operational and actively used as a learning environment for students seeking hands-on experience with real-world IT support processes.
