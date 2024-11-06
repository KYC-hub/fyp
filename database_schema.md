# Database Schema Documentation

## ER Diagram
Refer to `architecture_diagram.png`.

## Tables
### Scan Results
- **Fields**: `scan_id`, `ip_address`, `timestamp`, `status`

### User Table
- **Fields**: `user_id`, `username`, `role`, `permissions`

### Alerts
- **Fields**: `alert_id`, `severity`, `date`

## Relationships
1. **User - Scan Results**: `user_id` to `scan_id`.
2. **Alerts**: Linked to `user_id` and `scan_id`.
