# IT Audit Automation Tool

## Project Overview
This project is an IT audit automation tool designed to streamline compliance verification, monitor network systems in real-time, and generate comprehensive audit reports. The tool integrates AI for analyzing compliance standards and flags issues in data security, access controls, and more.

## Key Features
- **Network Scanning**: Scans systems for vulnerabilities.
- **Compliance Verification**: Verifies policies against benchmarks (e.g., GDPR, NIST).
- **Reporting & Visualization**: Displays compliance status via dashboards and generates exportable reports.

## Installation Instructions
1. Clone the repository.
2. Install dependencies via `pip install -r requirements.txt`.
3. Run `python app.py` to start the local server.

## Usage Guide
- **To Start a Network Scan**: Go to `/api/scan/network` and provide the required parameters.
- **Generate Compliance Report**: Access `/api/compliance/verify` and submit scan data.
