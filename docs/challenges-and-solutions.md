# Challenges and Solutions

## Email Delivery Issues

### Challenge

New users were unable to receive account activation and password reset emails.

### Solution

Implemented a temporary onboarding process using manually created accounts and temporary passwords while evaluating long-term email delivery solutions.

### Outcome

Users were able to access the platform and begin testing without waiting for email configuration.

---

## Email-to-Ticket Automation

### Challenge

The platform initially relied on users manually creating tickets through the web portal. To better simulate real-world help desk environments, support requests needed to be accepted through email and automatically converted into tickets.

The implementation required configuring a custom domain email address, validating DNS records, integrating Namecheap Private Email with osTicket, configuring IMAP connectivity, and creating automated email fetching through Linux cron jobs.

### Solution

A dedicated mailbox was created using:

[support@pschi02.com](mailto:support@pschi02.com)

The mailbox was integrated with osTicket using IMAP over SSL and configured to automatically fetch messages every five minutes.

Additional work included:

* DNS and MX record configuration
* SPF validation
* IMAP authentication troubleshooting
* Linux cron job configuration
* osTicket email fetching configuration
* Automatic email archiving after processing

Extensive testing was performed using multiple email providers to validate mail delivery and ticket creation.

### Outcome

Users can now create tickets by simply emailing [support@pschi02.com](mailto:support@pschi02.com).

The workflow is fully automated:

1. User sends an email.
2. Email is delivered to the support mailbox.
3. osTicket retrieves the message using IMAP.
4. A ticket is automatically generated.
5. The processed email is archived.

This enhancement provides a more realistic help desk experience while introducing hands-on experience with DNS, email administration, IMAP, Linux automation, and ticket management systems.

---

## Knowledge Base Development

### Challenge

Students often encountered the same lab issues repeatedly.

### Solution

Created troubleshooting articles and knowledge base documentation covering common CompTIA lab problems.

### Outcome

Students could reference existing solutions before opening support tickets.

---

## Monitoring and Visibility

### Challenge

Limited visibility into server performance and health.

### Solution

Implemented Prometheus and Grafana monitoring to provide real-time visibility into system resources, service health, uptime, and infrastructure performance.

---

## Discord Notification Integration

### Challenge

Monitoring dashboards provided visibility into system performance, but administrators still needed to actively check the platform to determine whether new support activity had occurred.

A lightweight notification solution was needed to provide immediate awareness of ticket activity without requiring constant dashboard monitoring.

The implementation required integrating Discord webhooks with the server environment, validating webhook communication, and ensuring notifications could be received on both desktop and mobile devices.

### Solution

A dedicated Discord webhook was created and integrated with the osTicket environment.

Additional work included:

* Discord webhook creation and configuration
* Server-side webhook integration
* PHP configuration validation
* Notification delivery testing
* Mobile notification verification
* Troubleshooting webhook formatting and authentication issues

Multiple rounds of testing were performed to validate successful communication between the server and Discord.

### Outcome

The server can now successfully deliver notifications to Discord channels, providing near real-time awareness of support activity.

Benefits include:

* Immediate notification delivery
* Mobile push notifications
* Improved operational visibility
* Reduced need for manual dashboard monitoring

This enhancement introduced hands-on experience with webhook integrations, notification systems, application configuration, and operational monitoring.

### Current Limitation

Direct webhook notifications are functioning successfully; however, email-generated tickets are not currently triggering Discord notifications.

Future development will focus on extending notification coverage to additional ticket workflows and automation events.


### Outcome

Improved insight into server status, uptime, resource utilization, and service availability while providing a foundation for future security monitoring and observability initiatives.
