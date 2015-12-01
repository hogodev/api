# Authentication API
  The Authentication API description


## Check Email

HogoPro support users to use one email address to join in different teams, so the first step to login HoGoPro (teamspace) to get list of team belong to. If the email address is in many teams, user has to pick up the team to login.


### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/login/checkmail
````


### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| email_address | String | (Required) user' email address |


#### Response example
```json
 {  
   "result":[  
      {  
         "first_name":"John",
         "middle_name":null,
         "team_name":"HoGo Inc",
         "last_name":"Smith",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "lang":"auto",
         "email_address":"john.smith@@hogo-teamspace.com"
      },
      {  
         "first_name":"John",
         "middle_name":null,
         "team_name":"HoGo Inc",
         "last_name":"Doe",
         "team_id":"1c136806bd3a4b3d89530392103a781c",
         "lang":"auto",
         "email_address":"john.d@hogodoc.com"
      }
   ],
   "status_code":200,
   "total_records":3
}
```

## Login

The API is to login in team and generate auth_token to access through system.
The auth_token will be value of ```session_id``` response

#### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/login
````

#### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

#### Request parameters

  -------------------------------------------------------------------------- --------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------
| Name | Data Format | Description |
|:---|:---|:---|
| email_address | String | (Required) user' email address |
| password | String | (Required) MD5 string password |
| team_id | String | (Required) user' team ID |
| keep_me_login | boolean | (Required) keep login status |



##### Response example

```json
  {  
   "result":{  
      "first_name":"John",
      "session_id":"12523dd59f874e1194f5f7dbf64194e0",
      "role_id":1,
      "middle_name":null,
      "last_name":"Doe",
      "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
      "lang":"auto",
      "email_address":"john.d@hogodoc.com"
   },
   "status_code":200,
   "total_records":null
}
```


### Logout

Destroy auth_token and log out from the system.

#### URL
- POST
```` URL
  POST)http://{Server name}:{Port}/{Context root}/api/user/logout
````


#### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

#### Request parameters

  -------------------------------------------------------------------------- --------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------
| Name | Data Format | Description |
|:---|:---|:---|
| access_token | String | (Required) The current auth_token |



##### Response example

```json
  {  
   "status_code":200,
   "total_records":null
}
```
