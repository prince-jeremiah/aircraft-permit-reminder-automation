# Workflow Overview

## Project

Aircraft Permit Reminder Automation

## Purpose

This workflow automates the monitoring of aircraft permits and their expiration dates.

The system reads permit records from Google Sheets, calculates the number of days remaining until expiration, determines the current permit status, and sends reminder emails when action is required.

The workflow also records reminder activity and prevents duplicate reminders.

---

## Architecture

The workflow follows this general process:

Schedule Trigger
        ↓
Read Permit Data
        ↓
Calculate Expiry Status
        ↓
Determine Reminder Requirement
        ↓
Check Duplicate Reminder
        ↓
Send Email Reminder
        ↓
Update Permit Record

---

## Main Components

### 1. Trigger

The workflow can be executed automatically according to a schedule or manually during testing.

### 2. Google Sheets

Google Sheets is used as the data source for aircraft permit records.

Example fields include:

- Aircraft Registration
- Aircraft Type
- Permit Type
- Issue Date
- Expiry Date
- Responsible Email
- Status
- Reminder Status
- Last Reminder Sent

---

## 3. Expiry Calculation

The workflow uses JavaScript to calculate the number of days remaining before a permit expires.

The calculated value is used to determine the appropriate permit status and whether a reminder should be sent.

---

## 4. Permit Status

The automation categorizes permits according to their expiry condition.

Typical statuses include:

- Active
- Due Soon
- Expired

---

## 5. Reminder Logic

The system checks whether a permit requires a reminder.

Reminder thresholds include:

- 30 days before expiry
- 14 days before expiry
- 7 days before expiry
- 1 day before expiry

This allows responsible personnel to take action before a permit expires.

---

## 6. Duplicate Reminder Prevention

The workflow maintains reminder information so that the same reminder is not repeatedly sent for the same expiry threshold.

This prevents unnecessary email notifications.

---

## 7. Email Automation

Gmail is used to send automated permit reminder notifications to the responsible person.

The email contains information about the relevant aircraft, permit and expiry date.

---

## 8. Record Updates

After processing a permit, the workflow updates the corresponding Google Sheets record.

Information such as the permit status, reminder status and last reminder date can be maintained for future workflow executions.

---

## Technologies

- n8n
- JavaScript
- Google Sheets
- Gmail
- JSON
- Workflow Automation

---

## Skills Demonstrated

This project demonstrates practical experience in:

- Workflow automation
- Business process automation
- API/service integration
- Data processing
- JavaScript automation
- Conditional logic
- Automated notifications
- Error prevention
- Operational compliance monitoring

---

## Business Value

Manual monitoring of permit expiry dates can result in missed deadlines and unnecessary administrative work.

This automation reduces manual monitoring by continuously processing permit records and notifying responsible personnel when action is required.

It also improves consistency by applying predefined expiry and reminder rules.

---

## Portfolio Notes

This repository contains a sanitized version of the n8n workflow for demonstration purposes.

Credentials, private connection information and operational data have been removed.

The included CSV contains demonstration data only.
