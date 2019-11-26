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
| /nursenav/surgery/:surgeryId | GET /api/Patients | opts:object | Patients || Returns the pcurrent patient personal information |
| /nursenav/surgery/:surgeryId | GET /api/NavMessagingLog | opts:object | NavMessagingLog |||
| /nursenav/surgery/:surgeryId | GET /api/Facilities || Facilities || returns all facilities |
| /nursenav/surgery/:surgeryId | GET /api/NavTemplateMessages || NavTemplateMessages || returns the templates for the Navigator messaging widget |
| /nursenav/surgery/:surgeryId | GET /api/Surgeries | opts:object | Surgeries, Hospital, Patient, Surgeon, Tasks, User |||
| /nursenav/surgery/:surgeryId | GET /api/SurgeryFlag || SurgeryFlag || returns all surgery flag data |
| /nursenav/surgery/:surgeryId | GET /api/SurgeryAddlInfo | opts:object | SurgeryFlag |||
| /nursenav/surgery/:surgeryId | GET /api/DischargeDispositions || DischargeDispositions |||
| /nursenav/surgery/:surgeryId | GET /api/SurgeryPertinentPositives | opts:object | SurgeryPertinentPositives, PertinentPositive, QuestionGroup, Questions, QuestionOptions, Answers, AnswerValues, PertinentPositiveValue |||
| /nursenav/surgery/:surgeryId | GET /api/SurgeryDashboardView | opts:object | SurgeryDashboardView |||
| /nursenav/surgery/:surgeryId | GET /api/Tasks | opts:object | Tasks, TaskType |||
| /nursenav/surgery/:surgeryId | GET /api/MessageDashboardView | opts:object | MessageDashboardView |||
| /nursenav/surgery/:surgeryId | GET /api/Admissions | opts:object | Admissions, Facility, Answers, AnswerValues, Question, QuestionOptions, Conversations |||
| /nursenav/surgery/:surgeryId | GET /api/PostAcuteEvents | opts:object | PostAcuteEvents, ReadmissionFacility, PrimaryReason, SecondaryReasons, Reasons |||
| /nursenav/surgery/:surgeryId | GET /api/HospitalVisits | opts:object | HospitalVisits, Admission, ReadmissionFacility, Reason, SecondaryReasons, Reasons |||
| /nursenav/users | GET /api/Users | opts:object | Users, Facility |||
| /nursenav/patients | GET /api/Patients | opts:object | Patients |||
| /nursenav/export/hospital | GET /api/Hospitals | opts:object | Hospital |||
| /nursenav/import/hospital | GET /api/HospitalImport | opts:object | HospitalImport |||
| /nursenav/surgeons | GET /api/Surgeons | opts:object | Surgeons |||
| /nursenav/hospitals | GET /api/Hospitals | opts:object | Hospitals |||