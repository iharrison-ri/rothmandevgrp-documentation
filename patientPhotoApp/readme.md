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

