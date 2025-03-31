# Lead Qualification Workflow
==========================

## Overview
-----------

This project automates the lead qualification process using n8n, integrating form submissions, Google Sheets for data storage, AI-based email generation, and automated email dispatch via Gmail. The workflow is designed to streamline lead management and enhance personalized communication with potential clients.

### Key Features
---------------

- **Automated Lead Capture:** Captures lead information through a web form.
- **Data Storage:** Stores lead information in Google Sheets for tracking and analysis.
- **AI-Generated Emails:** Generates personalized email responses using AI.
- **Lead Categorization:** Tags leads based on budget, service interest, and project timeline.
- **Automated Email Dispatch:** Sends personalized emails to leads using Gmail integration.

## Workflow Components
---------------------

### 1. Form Submission Trigger
#### Purpose
Captures lead information through a web form.

#### Fields
- Full Name (required)
- Email Address (required)
- Phone Number (required)
- Services Interested In (dropdown: Basic, Silver, Golden Package)
- Budget Range (dropdown: $0–$5000, $5000–$10000, Over $10000)
- Preferred Contact Time (Morning/Evening)
- Project Timeline (W1, W2, W3)
- Comments (optional)

### 2. Google Sheets Integration
#### Purpose
Stores lead information in a Google Sheet for tracking and analysis.

#### Mapped Fields
- Full Name
- Email Address
- Services Interested In
- Budget Range
- Contact Time
- Timeline
- Comments

### 3. AI Agent for Email Generation
#### Purpose
Generates personalized email responses using AI.

#### Email Structure
- **Subject:** Begins with "ABC Corp:" followed by a brief description.
- **Body:** Personalized content based on lead details.
- **Tag:** Categorization of the lead (e.g., High-Value Lead, Medium-Value Lead).

### 4. Lead Categorization
#### Criteria
- **High-Value Lead:** Budget > $10,000 or Golden Package interest.
- **Medium-Value Lead:** Budget $5,000–$10,000 or Silver Package interest.
- **Low-Value Lead:** Budget < $5,000 or Basic Package interest.
- **Hot Lead:** Immediate project timeline (W1/W2).
- **Cold Lead:** Long-term timeline (W3).

### 5. Automated Email Dispatch
#### Purpose
Sends personalized emails to leads using Gmail integration.

#### Updates
- Google Sheets with the status of the email sent and lead categorization.

## Workflow Execution
-------------------

1. **Lead Form Submission:** A lead fills out the form on the website.
2. **Data Capture:** Information is captured and stored in Google Sheets.
3. **Email Generation:** The AI agent generates an email tailored to the lead's details.
4. **Email Dispatch:** The email is sent automatically via Gmail.
5. **Status Update:** Google Sheets is updated with the email status and lead tag.

## Benefits
------------

- **Automation:** Reduces manual effort in lead management.
- **Personalization:** Ensures tailored communication with leads.
- **Prioritization:** Categorizes leads for strategic follow-up.

