## Summary

Investigated outbound email delivery limitations affecting the PSChi02 Help Desk environment hosted on DigitalOcean.

## Background

While configuring email notifications and ticket-related communications for osTicket, outbound SMTP connectivity issues were identified. Initial troubleshooting suggested network-level restrictions rather than application or credential misconfiguration.

## Troubleshooting Performed

### Connectivity Testing

- Verified osTicket email configuration settings.
- Confirmed DNS resolution for external mail services.
- Tested outbound SMTP connectivity from the DigitalOcean Droplet.
- Reviewed local firewall configuration and confirmed no blocking rules were present.
- Confirmed that DigitalOcean Cloud Firewalls were not restricting outbound traffic.

### Provider Engagement

- Opened a support request with DigitalOcean to investigate SMTP connectivity limitations.
- Provided business and application use-case information as requested by support.
- Received confirmation from DigitalOcean that outbound SMTP ports are restricted under current platform policy.

### Confirmed Restrictions

The following outbound SMTP ports are blocked and cannot be unblocked for this environment:

- Port 25 (SMTP)
- Port 465 (SMTPS)
- Port 587 (SMTP Submission)

## Impact

Traditional SMTP-based email delivery from the server cannot be used for:

- Ticket notifications
- Password reset messages
- User onboarding emails
- Automated system notifications

when relying on standard SMTP ports.

## Alternative Solutions Identified

Potential alternatives include:

- API-based email providers (Mailgun, SendGrid, Postmark, etc.)
- SMTP services supporting alternate ports such as 2525
- Third-party mail relay services

## Lessons Learned

This investigation highlighted a common cloud-hosting limitation designed to reduce spam and abuse. The troubleshooting process involved:

- Application-layer verification
- Network connectivity testing
- Firewall validation
- Vendor escalation and support communication
- Documentation of platform-specific constraints

## Current Status

SMTP integration remains under evaluation.

Discord notifications continue to provide real-time ticket alerting while alternative email delivery methods are assessed.
