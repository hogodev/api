# User Management API
  The User Management API description

## SIGN UP TEAM ADMIN & CREATE NEW TEAM

The API is used for new customers who want to use HoGoPro system.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/signup
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| first_name | String | (Required) admin team' first name |
| last_name | String | (Required) admin team' last name |
| email_address | String | (Required) admin team' email address |
| business_name | String | (Required) team name |
| business_size | String | (Optional) (default value : "1-50 employees") team size |
| phone | String | (Required) admin team' phone numbers |
| password | String | (Required) admin team' password |
| confirm_password | String | (Required) admin team' confirm password |
| payment_id | String | (Optional) payment_id  |
| plan_id | int | (Required) plan_id which team admin decide to register at HoGoPro |

#### Response example
```json
{  
   "result":"OK",
   "description":"New user and team is created",
   "status_code":200,
   "total_records":null
}
```

## ACTIVATE USER & TEAM

After signing up acccount in HoGoPro, Team Admin has to activate the account before using HoGoPro services.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/activation
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| activation_code | String | (Required) the activation code which team admin receive from his/her email address |

#### Response example
```json
{  
   "result":"You have just activate your account successful",
   "description":"OK",
   "status_code":200,
   "total_records":null
}
```

## GET NEW ACTIVATION CODE

The activation is just available for 30 minutes after signing up. Therefore, This API allows Team Admin receive a new activation code.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/getactivationcode
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| activation_code | String | (Required) the expiraton activation code |

#### Response example
```json
{  
   "result":"Check your email address to active your account",
   "description":"OK",
   "status_code":200,
   "total_records":null
}
```

## GET USER LIST IN TEAM

Get all members in team.


### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/list
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) current user' auth_token |
| search_key | String | (Optional) member' name key search |
| sort_key | int | (Optional) (Default value : 6 - sort by Email Address DESC) sort key range from 1-10 |
| page_size | int | (Optional) (Default value : 10) number of members to load when API called |
| page_number | int | (Optional) (Default value : 0) the position to start to load members |


#### Response example
```json
 {  
   "result":{  
      "total_result":5,
      "data":[  
         {  
            "user_id":"5d222a3b13c1473cae74c14447ad8ef0",
            "team_id":"34ee29628110424696ea902bf5b342f2",
            "role_id":3,
            "mail_address":"testuser004@gmail.com",
            "password_hash":"e10adc3949ba59abbe56e057f20f883e",
            "status":1,
            "first_name":"Le",
            "middle_name":null,
            "last_name":"Tran",
            "session_time_out":30,
            "activation_code":"",
            "activation_date":"2015/09/08 09:01:31",
            "num_of_disp_notify":"5",
            "piriod_of_disp_notify":10080,
            "time_zone":-5,
            "signup_date":"2015/09/08 04:01:31",
            "last_activity":null,
            "status_notify":"00000100",
            "notification_flag":"111",
            "card_info_id":null,
            "landing_page":1,
            "lang":"auto",
            "bookend_user_id":"hxeHXKwstCJLMUtnhJAwZIT5SnsyggOf"
         },
         {  
            "user_id":"ec948fc8a79a46cc9add899105a62cdb",
            "team_id":"34ee29628110424696ea902bf5b342f2",
            "role_id":2,
            "mail_address":"testuser003@gmail.com",
            "password_hash":"e10adc3949ba59abbe56e057f20f883e",
            "status":1,
            "first_name":"Quy",
            "middle_name":"Lien",
            "last_name":"Duong",
            "session_time_out":30,
            "activation_code":"",
            "activation_date":"2015/09/08 09:01:29",
            "num_of_disp_notify":"5",
            "piriod_of_disp_notify":10080,
            "time_zone":-5,
            "signup_date":"2015/09/08 04:01:29",
            "last_activity":null,
            "status_notify":"00000100",
            "notification_flag":"111",
            "card_info_id":null,
            "landing_page":1,
            "lang":"auto",
            "bookend_user_id":"xDDn4doaZw7TUOC2jKJJ0jPEkCbXvMAW"
         },
         {  
            "user_id":"76900a7566824852b2457c014d38e03f",
            "team_id":"34ee29628110424696ea902bf5b342f2",
            "role_id":2,
            "mail_address":"testuser002@gmail.com",
            "password_hash":"e10adc3949ba59abbe56e057f20f883e",
            "status":1,
            "first_name":"Le",
            "middle_name":"Hieu",
            "last_name":"Tran",
            "session_time_out":30,
            "activation_code":"",
            "activation_date":"2015/09/08 08:42:07",
            "num_of_disp_notify":"5",
            "piriod_of_disp_notify":10080,
            "time_zone":-5,
            "signup_date":"2015/09/08 03:42:07",
            "last_activity":null,
            "status_notify":"00000100",
            "notification_flag":"111",
            "card_info_id":null,
            "landing_page":1,
            "lang":"auto",
            "bookend_user_id":"crrbqK6RtWNdnVTrfTnPcsGovJeyXwBC"
         },
         {  
            "user_id":"714a93c5b3074edebdeb3ba9c71a5981",
            "team_id":"34ee29628110424696ea902bf5b342f2",
            "role_id":2,
            "mail_address":"testuser001@gmail.com",
            "password_hash":"e10adc3949ba59abbe56e057f20f883e",
            "status":1,
            "first_name":"Le",
            "middle_name":null,
            "last_name":"Hieu",
            "session_time_out":30,
            "activation_code":"",
            "activation_date":"2015/07/27 08:23:15",
            "num_of_disp_notify":"5",
            "piriod_of_disp_notify":10080,
            "time_zone":-5,
            "signup_date":"2015/07/27 03:23:15",
            "last_activity":"2015/09/08 10:27:00",
            "status_notify":"00000100",
            "notification_flag":"111",
            "card_info_id":null,
            "landing_page":1,
            "lang":"auto",
            "bookend_user_id":"THumDesg8YZ71FMsFRJ9hTmo7HRu2PSe"
         },
         {  
            "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
            "team_id":"34ee29628110424696ea902bf5b342f2",
            "role_id":1,
            "mail_address":"le.tran@nit-software.com",
            "password_hash":"e10adc3949ba59abbe56e057f20f883e",
            "status":1,
            "first_name":"Le",
            "middle_name":null,
            "last_name":"Tran",
            "session_time_out":30,
            "activation_code":"",
            "activation_date":"2015/07/27 08:09:48",
            "num_of_disp_notify":"5",
            "piriod_of_disp_notify":10080,
            "time_zone":-5,
            "signup_date":"2015/07/27 03:10:57",
            "last_activity":"2015/09/09 08:33:58",
            "status_notify":"00000100",
            "notification_flag":"111",
            "card_info_id":null,
            "landing_page":1,
            "lang":"auto",
            "bookend_user_id":"L0BweCJyZMJZOqmUd6lIo2MTbNE8ESOu"
         }
      ]
   },
   "status_code":200,
   "total_records":null
}
```
## GET USER LIST IN PROJECT

The API is to show all information of members in project

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/project
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) current user auth_token |
| project_id | String | (Required) the project_id to list all member in project |

#### Response example
```json
{  
   "result":[  
      {  
         "first_name":"Le",
         "create_date":"2015/09/04 07:08:06",
         "status":1,
         "project_role_id":1,
         "last_name":"Tran",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "email_address":"le.tran@nit-software.com"
      },
      {  
         "first_name":"Le",
         "create_date":"2015/09/04 07:08:06",
         "status":1,
         "project_role_id":2,
         "last_name":"Hieu",
         "user_id":"714a93c5b3074edebdeb3ba9c71a5981",
         "email_address":"testuser001@gmail.com"
      }
   ],
   "status_code":200,
   "total_records":null
}
```

## CREATE USER

The API allow Team Admin and Team Manager create another user. Team Admin is able to create new Manager, and User while Team Manager is only able to create new User

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/create
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) current user' auth_token |
| first_name | String | (Required) new user' first name |
| last_name | String | (Required) new user' last name |
| middle_name | String | (Optional) new user' middle name |
| mail_address | String | (Required) new user' email address |
| password | String | (Required) new user' password |
| confirm_password | String | (Required) new user' confirm password |
| user_role | int | (Required) new user' role in team. 1 Admin, 2 Manager, 3 Member |

#### Response example
```json
{  
   "result":{  
      "user_id":"7cc1851a91774b69af35835e586d803a",
      "team_id":"34ee29628110424696ea902bf5b342f2",
      "role_id":3,
      "mail_address":"testuser004@gmail.com",
      "password_hash":"e10adc3949ba59abbe56e057f20f883e",
      "status":1,
      "first_name":"Le",
      "middle_name":"Hieu",
      "last_name":"Tran",
      "session_time_out":30,
      "activation_code":"",
      "activation_date":"2015/09/09 09:06:58",
      "num_of_disp_notify":"5",
      "piriod_of_disp_notify":10080,
      "time_zone":-5,
      "signup_date":"2015/09/09 09:06:58",
      "last_activity":null,
      "status_notify":"00000100",
      "notification_flag":"111",
      "card_info_id":null,
      "landing_page":1,
      "lang":"auto",
      "bookend_user_id":"hxeHXKwstCJLMUtnhJAwZIT5SnsyggOf"
   },
   "description":"OK",
   "status_code":200,
   "total_records":null
}
```

## CREATE USERS BY IMPORT CSV FILE

The API supports Team Admin/Team Manager to create users at the same time by importing CSV file.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/importusercsv
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| file | MultipartFile | (Required) The CSV file which contains  |
| auth_token | String | (Required) current user' auth_token |

#### Response example
```json
{  
   "result":200,
   "description":"OK",
   "status_code":200,
   "total_records":null
}
```

## UPDATE USER

The API is to help user to update their information & Team Admin/ Team Manager update name, role for User

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/update
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) current user' auth_token |
| user_update_id | String | (Required) updated user id (used for Team Admin/Manager update another user in team) |
| first_name | String | (Required) user' new first name |
| middle_name | String | (Optional) user' new last name |
| last_name | String | (Required) user' new middle name |
| role_id | Integer | (Optional) new role (used for Team Admin/Manager update another user in team) |
| time_zone | Integer | (Optional) user' new timezone |
| notification_flag | String | (Optional) 3 characters string. The first character is account change, the second character is encode file expire, and the third one is having new comment. 0-no notify, and 1-notify  |
| lang | String | (Optional) language: en-English, ja-Japanese |

#### Response example
```json
{  
   "result":{  
      "user_id":"df52058ac0e7431da9b4d00d5540a6af",
      "team_id":"34ee29628110424696ea902bf5b342f2",
      "role_id":2,
      "mail_address":"testuser004@gmail.com",
      "password_hash":"e10adc3949ba59abbe56e057f20f883e",
      "status":1,
      "first_name":"Le",
      "middle_name":null,
      "last_name":"Tran",
      "session_time_out":30,
      "activation_code":"",
      "activation_date":"2015/09/09 10:02:23",
      "num_of_disp_notify":"5",
      "piriod_of_disp_notify":10080,
      "time_zone":-5,
      "signup_date":"2015/09/09 10:02:23",
      "last_activity":null,
      "status_notify":"00000100",
      "notification_flag":"111",
      "card_info_id":null,
      "landing_page":1,
      "lang":"auto",
      "bookend_user_id":"hxeHXKwstCJLMUtnhJAwZIT5SnsyggOf"
   },
   "description":"OK",
   "status_code":200,
   "total_records":null
}
```

## REMOVE USER

The API is to change the member' status to deleted which means that user cannot be used anymore. Team Admin can delete Manager, and Member, while Team Manager is only able to delete Member.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/remove
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) current user' auth_token |
| user_id | String | (Required) user_id will be deleted |

#### Response example
```json
{  
   "result":"User is inactive now",
   "description":"OK",
   "status_code":200,
   "total_records":null
}
```

## GET USER INFO

The API is to get all information from the current auth_token.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/info
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) current user' auth_token |

#### Response example
```json
{  
   "result":{  
      "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
      "team_id":"34ee29628110424696ea902bf5b342f2",
      "role_id":1,
      "mail_address":"le.tran@nit-software.com",
      "password_hash":"e10adc3949ba59abbe56e057f20f883e",
      "status":1,
      "first_name":"Le",
      "middle_name":null,
      "last_name":"Tran",
      "session_time_out":30,
      "activation_code":"",
      "activation_date":"2015/07/27 08:09:48",
      "num_of_disp_notify":"5",
      "piriod_of_disp_notify":10080,
      "time_zone":-5,
      "signup_date":"2015/07/27 08:10:57",
      "last_activity":"2015/09/11 03:29:38",
      "status_notify":"00000100",
      "notification_flag":"111",
      "card_info_id":null,
      "landing_page":1,
      "lang":"auto",
      "bookend_user_id":"L0BweCJyZMJZOqmUd6lIo2MTbNE8ESOu"
   },
   "status_code":200,
   "total_records":null
}
```

## GET ORTHER USER INFO BY ID

The API is to get other user information by user_id.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/profile
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) current user' auth_token |
| user_id | String | (Required) user_id of user to view |

#### Response example
```json
{  
   "result":{  
      "user_id":"714a93c5b3074edebdeb3ba9c71a5981",
      "team_id":"34ee29628110424696ea902bf5b342f2",
      "role_id":2,
      "mail_address":"testuser001@gmail.com",
      "password_hash":"e10adc3949ba59abbe56e057f20f883e",
      "status":1,
      "first_name":"Le",
      "middle_name":null,
      "last_name":"Hieu",
      "session_time_out":30,
      "activation_code":"",
      "activation_date":"2015/07/27 03:23:15",
      "num_of_disp_notify":"5",
      "piriod_of_disp_notify":10080,
      "time_zone":-5,
      "signup_date":"2015/07/27 08:23:15",
      "last_activity":"2015/09/10 09:46:19",
      "status_notify":"00000100",
      "notification_flag":"111",
      "card_info_id":null,
      "landing_page":1,
      "lang":"auto",
      "bookend_user_id":"THumDesg8YZ71FMsFRJ9hTmo7HRu2PSe"
   },
   "description":"",
   "status_code":200,
   "total_records":null
}
```

## USER CHANGE PASSWORD

The API is to help user to change the password

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/changepassword
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) current user' auth_token |
| confirm_old_password | String | (Required) old password of user |
| new_password | String | (Required) new password of user |
| confirm_new_password | String | (Required) confirm new password of user |

#### Response example
```json
{  
   "result":{  
      "user_id":"714a93c5b3074edebdeb3ba9c71a5981",
      "team_id":"34ee29628110424696ea902bf5b342f2",
      "role_id":2,
      "mail_address":"testuser001@gmail.com",
      "password_hash":"e10adc3949ba59abbe56e057f20f883e",
      "status":1,
      "first_name":"Le",
      "middle_name":null,
      "last_name":"Hieu",
      "session_time_out":30,
      "activation_code":"",
      "activation_date":"2015/07/27 08:23:15",
      "num_of_disp_notify":"5",
      "piriod_of_disp_notify":10080,
      "time_zone":-5,
      "signup_date":"2015/07/27 08:23:15",
      "last_activity":"2015/09/11 03:42:07",
      "status_notify":"00000100",
      "notification_flag":"111",
      "card_info_id":null,
      "landing_page":1,
      "lang":"auto",
      "bookend_user_id":"THumDesg8YZ71FMsFRJ9hTmo7HRu2PSe"
   },
   "description":"OK",
   "status_code":200,
   "total_records":null
}
```

## USER CHANGE EMAIL ADDRESS

The API is to help user to change email address.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/changeemail
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) current user' auth_token |
| mail_adress | String  | (Required) new email address |

#### Response example
```json
{  
   "result":{  
      "user_id":"714a93c5b3074edebdeb3ba9c71a5981",
      "team_id":"34ee29628110424696ea902bf5b342f2",
      "role_id":2,
      "mail_address":"testuser01@gmail.com",
      "password_hash":"e10adc3949ba59abbe56e057f20f883e",
      "status":1,
      "first_name":"Le",
      "middle_name":null,
      "last_name":"Hieu",
      "session_time_out":30,
      "activation_code":"",
      "activation_date":"2015/07/27 08:23:15",
      "num_of_disp_notify":"5",
      "piriod_of_disp_notify":10080,
      "time_zone":-5,
      "signup_date":"2015/07/27 08:23:15",
      "last_activity":"2015/09/11 03:42:07",
      "status_notify":"00000100",
      "notification_flag":"111",
      "card_info_id":null,
      "landing_page":1,
      "lang":"auto",
      "bookend_user_id":"6saJo7GD0dT56rj27ykmOQeGfXPgxddx"
   },
   "description":"OK",
   "status_code":200,
   "total_records":null
}
```

## GET TEAM PROFILE

The API is to get all information about the team.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/getteam
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) current user' auth_token |
| team_id | String | (Required) team_id to get information |

#### Response example
```json
{  
   "result":{  
      "team_id":"34ee29628110424696ea902bf5b342f2",
      "name":"NIT SOFTWARE",
      "create_date":"2015/07/27 08:09:48",
      "email_address":"le.tran@nit-software.com",
      "website":null,
      "business_size":"1-50 employees",
      "phone_number":"0908296906",
      "status":2,
      "projects_usage":2,
      "payment_team_id":1,
      "number_of_user":4
   },
   "description":"OK",
   "status_code":200,
   "total_records":null
}
```

## UPDATE TEAM PROFILE

The API is to update the team profile. Only Team Admin & Super Admin(HoGoPro admin) are able to update team profile.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/updateteamprofile
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) current user' auth_token |
| team_update_id | String | (Required) team_id of team which will be updated |
| team_name | String | (Required) new team name |
| phone_number | String | (Required) new team phone number |
| company_size | String | (Required) new company size |
| website | String | (Optional) new company website |
| plan_id | int | (Optional) new plan_id |

#### Response example
```json
{  
   "result":{  
      "team_id":"34ee29628110424696ea902bf5b342f2",
      "name":"NIT SOFTWARE",
      "create_date":"2015/07/27 08:09:48",
      "email_address":"le.tran@nit-software.com",
      "website":"www.nit-software.com",
      "status":2,
      "business_size":"1-50 employees",
      "phone_number":"0908296906"
   },
   "description":"OK",
   "status_code":200,
   "total_records":null
}
```