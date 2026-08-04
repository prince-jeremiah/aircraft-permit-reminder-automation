# ✈️ Aircraft Permit Reminder Automation

> An automated aircraft permit monitoring and notification system built with **n8n**, **Google Sheets**, **Gmail**, and **JavaScript**.

## 📌 Overview

The Aircraft Permit Reminder Automation is a workflow automation solution designed to monitor aircraft permit expiration dates and automatically notify responsible personnel when action is required.

The system reads aircraft permit records from Google Sheets, calculates the remaining validity period, determines the permit status, checks whether a reminder is required, sends automated email notifications, and updates the permit record.

The project demonstrates how workflow automation can be applied to aviation operations and compliance monitoring.

---

## 🎯 Problem

Aircraft permits and operational documents have expiration dates that need to be monitored carefully.

Manual monitoring can result in:

- Missed expiry dates
- Late renewals
- Repetitive administrative work
- Inconsistent reminder processes
- Duplicate notifications

This automation addresses these problems by continuously processing permit records and applying predefined reminder rules.

---

## 💡 Solution

The workflow automates the complete reminder process:

```text
Aircraft Permit Data
        │
        ▼
┌─────────────────────┐
│    Google Sheets    │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Calculate Days Left  │
│ & Permit Status      │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Reminder Required?  │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Duplicate Check     │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Gmail Notification  │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Update Google Sheet │
└─────────────────────┘
