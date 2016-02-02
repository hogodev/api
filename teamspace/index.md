## HoGo TeamSpace REST API


Following is the design philosophy applied to HoGo API.
* API protocol must be HTTP or HTTPS
* API request parameters must be passed using query string for APIs that require GET
* API request parameters must be “application/x-www-form-urlencoded” for APIs that require POST
* API response body format must be JSON except when binary data returned
* All API response object has following properties


Server URL: https://dev2.hogodoc.com/hogopro/api/{API_NAME}

For example Login API: https://dev2.hogodoc.com/hogopro/api/user/login

Chat with the team
<p><a href="https://gitter.im/hogodev/api" target="_blank"><img src="https://camo.githubusercontent.com/da2edb525cde1455a622c58c0effc3a90b9a181c/68747470733a2f2f6261646765732e6769747465722e696d2f4a6f696e253230436861742e737667" alt="Join the chat" data-canonical-src="https://badges.gitter.im/Join%20Chat.svg" style="max-width:100%;"></a></p>

### COMMON APIs 

<ul>
<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/Authentication.md#authentication-api" target="_blank">       Authentication
  </a>
</li>

<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/ProjectManagement.md#create-project" target="_blank">
  Create Project
  </a>
</li>

<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/ProjectManagement.md#get-project-list" target="_blank">
  Get list of projects
  </a>
</li>

<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/ProjectManagement.md#get-filesfolders-in-projectfolder" target="_blank">
  Get files/folders in project
  </a>
</li>

<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/ProjectManagement.md#upload-files" target="_blank">
  Upload file into project
  </a>
</li>

<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/ProjectManagement.md#encode--register-license" target="_blank">
  Encode file & register lincese for all member in project
  </a>
</li>

<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/ProjectManagement.md#create-folder" target="_blank">
  Create a folder in project
  </a>
</li>

<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/Project_RegisterLicense.md#get-license-info" target="_blank">
  Get file License setting
  </a>
</li>

<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/Project_RegisterLicense.md#license-update" target="_blank">
  Update file License setting
  </a>
</li>

<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/ProjectManagement.md#download-file" target="_blank">
  Download File
  </a>
</li>

<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/Project_ShareFile.md#filefolder-sharing-apis" target="_blank">
  File & Folder sharing
  </a>
</li>


</ul>

### VIEW ALL OTHER APIs 
<ul>

<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/ProjectManagement.md#create-folder" target="_blank">
  Project Management APIs
  </a>
</li>

<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/UserManagement.md#user-management-api" target="_blank">
  User Management APIs
  </a>
</li>

<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/Project_Comment.md#create-comment" target="_blank">
  Project Comment APIs
  </a>
</li>

<li> 
  <a href="https://github.com/hogodev/api/blob/master/teamspace/History.md#history-api" target="_blank">
  History APIs
  </a>
</li>

</ul>

### COMMON API STATUS CODE


| Status | Code | Description |
|:---|:---|:---|
| ERR_INVALID_DATA | 100 | Input data is not valid |
| ERR_USER_NOT_EXIST| 110 | User does not exist |     
| ERR_USER_NOT_VALID | 111 | User name or password is not correct |
| ERR_USER_ROLE_NOT_VALID | 112 | You do not have permission to access this page | 
| OK | 200 |  null | 
| ERR_ENCODE | 300 | Error encoding file | 
| ERR_UPLOAD_FILE | 301 | Upload file error |     
| INVALID_PARAMETER | 400 | Invalid parameter |
| INVALID_ACCESS_TOKEN |  401 | Invalid access token |
| ERR_EXPIRE_TOKEN | 401 | The token is expired | 
| ERR_TOKEN_NOT_EXIST | 401 | Token does not exist |
| ERR_INVALID_FOLDER | 401 | New folder is child of moved folder |
| INVALID_ROLE_USER | (403 | User do not have permission |
| MISSING_PARAMETER | 404 | Parameter missing |    
| PROJECT_NOT_FOUND | 404 | Project not found |
| FOLDER_NOT_FOUND | 404 | Folder not found |
| FILE_NOT_FOUND | 404 | File not found |
| USER_NOT_FOUND | 404 | User not found |
| USER_NOT_FOUND_IN_PROJECT | 404 | User not found in the project |
| LINK_NOT_FOUND | 404 | Link not found |
| COMMENT_NOT_FOUND_OF_USER | 404 | Comment not found |
| LINK_EXPIRED | 410 | link is expired |
| WRONG_ACTIVATION_CODE | 411 | activation code is not correct |
| USER_ACTIVE | 412 | User has been active |
| INVALID_LIMIT_USER | 413 | Out of number of members in team |
| CREATE_HISTORY_FAILED  | 417 | Create history failed |
| CREATE_SESSION_FAILED  | 417 | Create session failed |
| INVALID_QUERY_SQL | 500 | Invalid query SQL |
| SYSTEM_EXCEPTION | 500 | System error |
| ERR_INVALID_EMAIL  | 501 | Invalid email |
| ERR_INVALID_FIRSTNAME | 502 | First Name contains speacial character |
| ERR_INVALID_LASTNAME | 503 | Last Name contains speacial character |
| ERR_INVALID_PASSWORD | 504 | Password is too short |
| ERR_INVALID_CONFIRMPASSWORD | 505 | Your confirm password is incorrect |
| ERR_INVALID_ROLEID | 506 | You do not have the permission to do this action |
| ERR_INVALID_EMAIL_EXIST | 507 | This email is already exist |
| ERR_INVALID_WRONGPASSWORD | 508 | Wrong password |
| ERR_INVALID_CANNOT_REMOVE_YOURSELFT | 509 | Cannot change yourself status from active to remove |
| ERR_ROLEID_NOT_EXIST | 510 | This role is not exist |
| ERR_INVALID_MIDDLENAME | 511 | Middle Name contains speacial character |
| ERR_LIMITED_USER  | 512 | Limited Create User |
| ERR_TEAM_NOT_EXIST | 513 | This Team does not exist |
| ERR_TEAM_EXIST | 514 | This Team is existent |



For more infomation about HoGo please reference at http://www.hogodoc.com <br/>
If any question regarding to APIs usage and customization support, please get in touch with us at http://www.hogodoc.com/contact-us
