### Pateint Photo App
*Data Flow*

| Page | Request | Params | Table | Action | Description
| - | - | - | - | - | - |
| /patient-list | POST /login | password:string, username:string | 
| /patient-list | GET /getRequestCount | providerId: number | patientRequest, forwardedRequest
| /patient-list | POST /getPatientRequests | order:string, orderBy:string | patientRequest, patient, forwardedRequest
| /patient-details/:patientId | GET /forwardedProvider |||| returns ldap users
| /patient-details/:patientId | GET /getPatientRequestById/:patientId || patientRequest, patient, patientRequestAssets, comment |
| /patient-details/:patientId | POST /forwardOrCompleteRequest || patientRequest | onSubmit Comment
| / | POST /uploadImages ||| on upload image | adds image to /public/images
| / | POST /patientUpload ||| on submit form | moves image from /public/images to public/#/images. Where # is the next increment in count of moved images

### Starting the app
start the app with pm2 with the following commands
```
Open the terminal as an administrator
cd C:\apps\qa\patientphotoapp\rothman_UI\Sprint-2_latest
pm2 start node_modules/react-scripts/scripts/start.js --name ppaUI

cd C:\apps\qa\patientphotoapp\restAPI_Dev
pm2 start bin/www --name ppaREST
```
### Deploying the app to qa
```
Open the terminal as an administrator
pm2 stop ppaUI
cd C:\apps\qa\patientphotoapp\rothman_UI\Sprint-2_latest
git pull origin qa
pm2 start ppaUI

pm2 stop ppaREST
cd C:\apps\qa\patientphotoapp\restAPI_Dev
git pull origin qa
pm2 start ppaREST
```
### Deploying the app to master
```
Open the terminal as an administrator
pm2 stop ppaUI
cd C:\apps\qa\patientphotoapp\rothman_UI\Sprint-2_latest
git pull origin master
pm2 start ppaUI

pm2 stop ppaREST
cd C:\apps\qa\patientphotoapp\restAPI_Dev
git pull origin master
pm2 start ppaREST
```
