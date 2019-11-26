# Orthonavigator
| Page | Request | Params | Table/View Refs | Action | Description
| - | - | - | - | - | - |
| /login | POST /api/login | username:string, password:string || on log in | returns AD record for user |
| /nursenav/dashboard | GET /api/Users | opts:object | Users || Returns users with a Role of 2 and 8 |
| /nursenav/dashboard | GET /api/alertCount | opts:object | AlertsDashboard || gets the counts for the alerts of the current user |
| /nursenav/dashboard | GET /api/Admissions | opts:object | Admissions, Facility, Surgery, Patient, Surgeon, Navigator || Get Overdue Discharge list |
| /nursenav/dashboard | GET /api/MessageDashboardView | opts:object | MessageDashboardView || get data to calculate the Change Messages numbers |
| /nursenav/dashboard | GET /api/TodaysTasksView | opts:object | TodaysTasksView || get the count for Today's Tasks |
| /nursenav/dashboard | GET /api/SurgeryDashboardView | opts:object | SurgeryDashboardView || gets the data for the Active, Inactive, Cancelled, and Missing Risk Levels tables |
| /nursenav/dashboard | GET /api/SurgeryFlag || SurgeryFlag || get data for the SurgeryFlag view to display the super high risk flags |
| /nursenav/alertsdashboard | requests defined above |||||
| /nursenav/overduedischarges | requests defined above |||||
| /nursenav/conversations/plan | requests defined above |||||
| /nursenav/conversations/other | requests defined above |||||
| /nursenav/tasks/today | requests defined above |||||
| /nursenav/surgery/:surgeryId | GET /api/Patients |||||
| /nursenav/surgery/:surgeryId | GET /api/NavMessagingLog |||||
| /nursenav/surgery/:surgeryId | GET /api/Facilities |||||
| /nursenav/surgery/:surgeryId | GET /api/NavTemplateMessages |||||
| /nursenav/surgery/:surgeryId | GET /api/Surgeries |||||
| /nursenav/surgery/:surgeryId | GET /api/SurgeryFlag |||||
| /nursenav/surgery/:surgeryId | GET /api/SurgeryAddlInfo |||||
| /nursenav/surgery/:surgeryId | GET /api/DischargeDispositions |||||
| /nursenav/surgery/:surgeryId | GET /api/SurgeryPertinentPositives |||||
| /nursenav/surgery/:surgeryId | GET /api/SurgeryDashboardView |||||
| /nursenav/surgery/:surgeryId | GET /api/Tasks |||||
| /nursenav/surgery/:surgeryId | GET /api/MessageDashboardView |||||
| /nursenav/surgery/:surgeryId | GET /api/Admissions |||||
| /nursenav/surgery/:surgeryId | GET /api/PostAcuteEvents |||||
| /nursenav/surgery/:surgeryId | GET /api/HospitalVisits |||||