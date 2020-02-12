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
| /nursenav/patients | GET /api/Patients | opts:object | Patients || returns all patient data |
| /nursenav/export/hospital | GET /api/Hospitals | opts:object | Hospital || returns all hospital data |
| /nursenav/import/hospital | GET /api/HospitalImport | opts:object | HospitalImport || returns all hospitalImport data for current user |
| /nursenav/surgeons | GET /api/Surgeons | opts:object | Surgeons || returns all surgeon data |
| /nursenav/hospitals | GET /api/Hospitals | opts:object | Hospitals || returns all hospital data |

### Starting the qa service
```
1. Open the terminal as an administrator
2. Check to see if pm2 is avaliable by running *pm2* in the terminal
3. If the pm2 service is available continue to step 9
4. If the service is not avalible the terminal may be confused on how to find the pm2 log file
5. Open the H drive folder (where the log file is located)
6. Right click in the file "Open Bash Here"
7. This will open the bash terminal. Type pm2 in the terminal. The terminal should now have access to the pm2 module
8. In the terminal you have opened as an administrator, navigate to the folder. In qa run the follwing command
9. cd C:\apps\qa\orthonav\roth-nav-ui && npm run-script build:dev
10. Run this command next
11. cd C:\apps\qa\orthonav\roth-nav-rest && pm2 start rothman-rest.js
PM2 should now be running your app!!

For the master branch number 9 and 11 will change to the following
cd C:\apps\production\orthonav\roth-nav-ui && npm run-script build:prod
cd C:\apps\production\orthonav\roth-nav-rest && pm2 start rothman-rest.js

### Deploying the app to qa
```
Open the terminal as an administrator
Take note of the "idNumber" of the app after running "pm2 ls"
pm2 stop "idNumber"
cd C:\apps\qa\orthonav\roth-nav-ui && npm pull origin qa && npm run-script build:dev
cd C:\apps\qa\orthonav\roth-nav-rest && npm pull origin qa && pm2 start "idNumber"

```
### Deploying the app to production
```
Open the terminal as an administrator
Take note of the "idNumber" of the app after running "pm2 ls"
pm2 stop "idNumber"
cd C:\apps\production\orthonav\roth-nav-ui && npm pull origin qa && npm run-script build:prod
cd C:\apps\production\orthonav\roth-nav-rest && npm pull origin qa && pm2 start "idNumber"
```
