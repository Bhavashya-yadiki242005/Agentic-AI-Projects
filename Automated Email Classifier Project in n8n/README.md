## Note: If GitHub does not preview the PDF, please download it to view the full documentation.
# AI-Powered Email Classifier using n8n

This project implements an automated email classification system using **n8n**.  
The workflow monitors incoming Gmail messages, classifies them using an AI model, and automatically labels emails based on their content (such as meeting requests or leave requests). For meeting-related emails, it can also create calendar events.

The complete technical explanation, setup steps, screenshots, and workflow details are documented in the attached PDF.

---

## Project Summary

The system performs the following tasks:

- Listens for new emails using a Gmail trigger
- Extracts email content
- Classifies emails into categories (e.g., Meeting Request, Leave Request)
- Applies Gmail labels automatically
- Creates Google Calendar events for meeting-related emails
- Runs continuously once activated

This project demonstrates how no-code/low-code automation can be combined with AI models to build real-world productivity workflows.

---


## How to Use This Project

1. Open your n8n instance.
2. Import `email-classifier-workflow.json`.
3. Add your own credentials for:
   - Gmail API
   - Google Calendar API
   - Gemini API
4. Activate the workflow.

Note: API keys and credentials are not included in this repository for security reasons.

---

## Technologies Used

- n8n (workflow automation)
- Gmail API
- Google Calendar API
- Google Gemini (for text classification)
- Google Cloud Console (API management)

---

## Documentation

All implementation details, configuration steps, screenshots, and workflow explanations are provided in:

**Project_Documentation.pdf**

Please refer to the PDF for the full project walkthrough.

---

## Use Cases

- Automatic email categorization
- Meeting scheduling from emails
- Leave request handling
- Business workflow automation
- AI-assisted inbox management
