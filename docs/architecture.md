# PSChi02 Help Desk Architecture

## Project Overview

PSChi02 Help Desk is a student-to-student support platform designed to provide hands-on IT support experience using an industry-standard ticketing system.

## Infrastructure

### Domains

support.pschi02.com</>

support.pschi02.com/scp

### Cloud Services

- DigitalOcean VPS
- Cloudflare DNS

### Operating System

- Rocky Linux

### Web Services

- Apache Web Server
- PHP

### Database

- MariaDB

### Ticketing Platform

- osTicket

## High-Level Architecture

Internet
│
├── Cloudflare
│
├── DigitalOcean VPS
│
├── Rocky Linux
│
├── Apache
│
├── PHP
│
├── MariaDB
│
└── osTicket

## Purpose

The platform was created to allow students to:

- Practice ticket management
- Develop troubleshooting skills
- Build documentation experience
- Learn escalation workflows
- Gain experience using real-world support software

## Future Enhancements

- Grafana dashboards
- Prometheus monitoring
- Discord integration
- Volunteer management system
- Expanded knowledge base
