# API Documentation

## Overview
Our API supports network scanning, compliance verification, and reporting.

### Network Scanning Endpoint
- **URL**: `/api/scan/network`
- **Method**: GET
- **Parameters**: `ip_range`, `scan_type`
- **Response**: `{ "status": "success", "data": [...] }`

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
