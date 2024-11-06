# System Architecture Documentation

## System Overview
This architecture comprises three core layers: frontend, backend, and data storage.

## Components
- **Frontend**: Web interface (React/HTML5).
- **Backend**: Flask/Django for API logic, compliance checks.
- **Database**: MongoDB for storing scan results and user data.

## Data Flow
User Interface (UI):

The frontend communicates with backend services via RESTful API calls, handling requests and displaying data in dashboards.
API Layer:

Acts as the intermediary between the UI and backend logic.
Define endpoints for key functions such as /scan, /compliance/verify, /alerts, and /reports.
Network Scanning Module:

Uses tools like Nmap to perform network scans and retrieve node data.
Sends scan results to the compliance module for analysis.
Compliance Verification Module:

Compares scan results to compliance benchmarks stored in the database.
Uses benchmarks like GDPR, HIPAA, and PDPA for initial validation.
Triggers alerts for non-compliance and logs results for reporting.
LLM Integration:

Processes policy data and provides recommendations.
Interacts with the backend to apply compliance policies.
Database:

Stores network scan results, compliance data, user profiles, and policies.
Utilizes secure storage methods to meet data protection requirements.
Alerting and Notification Module:

Monitors compliance in real-time and triggers alerts for violations.
Sends alerts through channels (e.g., email, in-app notifications).
Report Generation Module:

Formats compliance and scan results into reports.
Allows users to download reports in formats like PDF and CSV.
