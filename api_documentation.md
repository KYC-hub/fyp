# API Documentation

## Overview
Our API supports network scanning, compliance verification, and reporting.

### Network Scanning Endpoint
- **URL**: `/scan/network`
- **Method**: POST
- **Parameters**: `ip_range`, `scan_depth`
- **Request Body**: 
{
  "ip_range": "192.168.1.0/24",
  "scan_depth": "full"
}
- **Response**:
- {
  "status": "scan_initiated",
  "scan_id": "12345"
}


### Compliance Verification Endpoint
- **URL**: `/api/compliance/verify`
- **Method**: POST
- **Parameters**: `scan_data`, `benchmark`
- **Response**: `{ "compliance_status": "non-compliant", "details": [...] }`

### Authentication
- **JWT Token**: Required for all requests.

### Error Codes
- **400**: Bad Request
- **401**: Unauthorized
- **500**: Server Error
