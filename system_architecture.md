# System Architecture Documentation

## System Overview
This architecture comprises three core layers: frontend, backend, and data storage.

## Components
- **Frontend**: Web interface (React/HTML5).
- **Backend**: Flask/Django for API logic, compliance checks.
- **Database**: MongoDB for storing scan results and user data.

## Data Flow
1. **Scanning**: Initiates from frontend, calls `/api/scan`.
2. **Compliance Check**: Backend processes data, checks benchmarks.
3. **Report Generation**: Generates PDF/CSV files based on scan.
