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
- **Parameters**: `scan_data`, `benchmark`
- **Response**: `{ "compliance_status": "non-compliant", "details": [...] }`

### Authentication
- **JWT Token**: Required for all requests.

### Error Codes
- **400**: Bad Request
- **401**: Unauthorized
- **500**: Server Error
