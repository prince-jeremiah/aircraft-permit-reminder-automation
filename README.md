# Aircraft Permit Reminder Automation

An automated aircraft permit monitoring and reminder system built with n8n.

## Overview

This project automates the monitoring of aircraft permits and their expiration dates. It uses n8n to process permit information stored in Google Sheets, determine the current status of each permit, and send automated email reminders when action is required.

The workflow was designed to reduce manual monitoring and help ensure that important aviation permits are not overlooked.

## Key Features

- Aircraft permit expiry monitoring
- Automatic permit status calculation
- Expired permit detection
- Upcoming expiry alerts
- Automated email reminders
- Duplicate reminder prevention
- Last reminder tracking
- Google Sheets integration
- JavaScript-based workflow logic
- Automated status updates

## Technologies 

- n8n
- JavaScript
- Google Sheets
- Gmail
- Webhooks
- JSON
- Workflow Automation

## Workflow

The general workflow is:

Google Sheets
↓
Read Aircraft Permit Data
↓
Check Expiry Date
↓
Calculate Permit Status
↓
Determine Whether Reminder Is Required
↓
Check for Duplicate Reminder
↓
Send Email
↓
Update Google Sheets

## Example Status Logic

| Condition | Status |
|---|---|
| Permit has expired | Expired |
| Expiry is approaching | Urgent |
| Permit is sufficiently valid | Safe |

## Business Value

The automation helps reduce manual administrative work by automatically monitoring permit expiry dates and notifying responsible personnel when action is required.

It also reduces the risk of sending duplicate notifications by maintaining reminder history.

## Project Purpose

This project demonstrates practical application of workflow automation to aviation operations and compliance processes.

## Author

**Prince Jeremiah**

AI Automation Engineer | n8n Developer | Aviation Operations
