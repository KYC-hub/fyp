# API Documentation

## Overview
Our API supports network scanning, compliance verification, and reporting.

### Network Scanning Endpoint
- **URL**: `/scan/network`
- **Method**: POST
- **Request Body**: 
{
  "ip_range": "192.168.1.0/24",
  "scan_depth": "full"
}
- **Response**:
{
  "status": "scan_initiated",
  "scan_id": "12345"
}
- **Logic**: When this endpoint is called, it triggers the backend to start scanning the network range provided. The scan result is stored in a database and associated with a unique scan ID.


### Compliance Verification Endpoint
- **URL**: `/compliance/verify`
- **Method**: POST
- **Request Body**:
{
  "scan_id": "12345",
  "compliance_standard": "GDPR"
}
- **Response**:
{
  "compliance_status": "compliant",
  "violations": []
}
- **Logic**: This endpoint will compare the scan results against predefined rules from the specified compliance standard (e.g., GDPR). It returns the compliance status and any violations.

### Alerts
- **URL**: `/alerts`
- **Method**: POST
- **Request Body**:
{
  "alert_type": "unauthorized_access",
  "threshold_value": "5"
}
- **Response**:
{
  "status": "alert_created",
  "alert_id": "67890"
}
- **Logic**: Allows the user to set up different types of alerts (e.g., unauthorized access). These alerts trigger notifications when a violation threshold is reached.

### Retrieve compliance report
- **URL**: `/reports/{scan_id}`
- **Method**: GET
- **Response**:
{
  "report_url": "https://example.com/reports/12345.pdf"
}
- **Logic**: Fetches the generated report for a specific scan ID. The report includes a summary of network scanning results, compliance status, and detailed violations.

### LLM training
- **URL**: `/train-LLM`
- **Method**: POST
- **Request Body**:
{
  "policy_name": "NewGDPRPolicy",
  "policy_text": "Updated compliance rule..."
}
- **Response**:
{
  "status": "policy_added",
  "policy_id": "23456"
}
- **Logic**: Adds new compliance policies to the system, allowing the LLM to process updated compliance rules.

### Authentication
- **JWT Token**: Required for all requests.

### Error Codes
- **400**: Bad Request
- **401**: Unauthorized
- **500**: Server Error
