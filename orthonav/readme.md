# Orthonavigator
| Page | Request | Params | Table/View Refs | Action | Description
| - | - | - | - | - | - |
| /login | POST /api/login | username:string, password:string || on log in | returns AD record for user |
| /nursenav/dashboard ||||||
| /nursenav/alertsdashboard | GET /api/Users | opts:object | Users || Returns users with a Role of 2 and 8 |
| /nursenav/alertsdashboard | GET /api/alertCount | opts:object | AlertsDashboard || gets the counts for the alerts of the current user |
| /nursenav/alertsdashboard | GET /api/Admissions | opts:object | Admissions, Facility, Surgery, Patient, Surgeon, Navigator || Get Overdue Discharge list |
| /nursenav/alertsdashboard | GET /api/MessageDashboardView | opts:object | MessageDashboardView || get data to calculate the Change Messages numbers |
| /nursenav/alertsdashboard ||||||
| /nursenav/alertsdashboard ||||||
| /nursenav/alertsdashboard ||||||
| /nursenav/overduedischarges ||||||
| /nursenav/conversations/plan ||||||
| /nursenav/conversations/other ||||||
| /nursenav/tasks/today ||||||
| /nursenav/surgery/:surgeryId ||||||
| /nursenav/dashboard ||||||
| /nursenav/dashboard ||||||