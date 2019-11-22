# Provider Care Portal
| Page | Request | Params | Table Refs | Action | Description
| - | - | - | - | - | - |
| / | POST /api/login | username:string, password:string || on log in | return ldap user |
| / | GET /api/ComplianceReport | startDate:datetime, endTime:datetime, opts:object | AdverseEvents, Surgeries | on log in||
| / | GET /api/ServiceActivitiesSummary | opts:object | ServiceActivitiesSummary (View) | on log in| Service ACC table data |
| / | GET /api/KpiReport | opts:object || on log in | KPI table data |
| / | GET /api/AdverseEvents | opts:object || on log in | List table data |
| / | GET /api/ComplianceReport | opts:object || on log in | Compliance table data |
| / | GET /api/AdverseEventTypes | opts:object || on log in | Adverse Events table data |
| / | GET /api/Categories | opts:object | Categories, Activities, ReportingPeriods, ApprovalLevels | on Service ACC row click ||