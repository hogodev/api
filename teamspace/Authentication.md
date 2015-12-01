# Authentication API
  The Authentication API description


## Check Email

HogoPro support users to use one email address to join in different teams, so the first step to login HoGoPro is check email address. If the email address is in many teams, user has to pick up the team to login. Otherwise, user just input password to login in the team.


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
         "first_name":"Le",
         "middle_name":null,
         "team_name":"NIT SOFTWARE",
         "last_name":"Tran",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "lang":"auto",
         "email_address":"le.tran@nit-software.com"
      },
      {  
         "first_name":"Le",
         "middle_name":null,
         "team_name":"NIT SOFTWARE 2",
         "last_name":"Tran",
         "team_id":"1c136806bd3a4b3d89530392103a781c",
         "lang":"auto",
         "email_address":"le.tran@nit-software.com"
      },
      {  
         "first_name":"Le",
         "middle_name":null,
         "team_name":"NIT SOFTWARE 1",
         "last_name":"Tran",
         "team_id":"fbc9f626c39e47b9ab4a919461b4360f",
         "lang":"auto",
         "email_address":"le.tran@nit-software.com"
      }
   ],
   "status_code":200,
   "total_records":3
}
```

## Login

The API is to login in team and generate auth_token to access through system.

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
      "first_name":"Le",
      "session_id":"12523dd59f874e1194f5f7dbf64194e0",
      "role_id":1,
      "middle_name":null,
      "last_name":"Tran",
      "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
      "lang":"auto",
      "email_address":"le.tran@nit-software.com"
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