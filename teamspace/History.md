# HISTORY API
  
## GET HISTORY BY TEAM

The API is to get all history in the team.

### URL
- GET
```` URL
  (GET)http://{Server name}:{Port}/{Context root}/api/history/team
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current user auth_token |
| team_id | String | (Required) the team id |
| page_size | Integer | (Optional) the number of history will be got at one time |
| page_number | Integer | (Optional) the page start to get history |
| history_types | String | (Optional) history type is to be got |
| last_update | Long | (Optional) last update |

#### Response example
```json
{  
   "result":[  
      {  
         "history_id":"e6504e98dbba4bf9bd5d457a21f15316",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"",
         "category":4,
         "history_type":403,
         "project_id":"",
         "create_date":"2015/09/11 05:37:58",
         "last_update":1441967878028,
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"adbb8ecfea9849e592a11e0706b301d7",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":3,
         "history_type":302,
         "create_date":"2015/09/10 06:57:13",
         "last_update":1441886233267,
         "data":{  
            "result":[  
               {  
                  "id":"e9ac4e663b26477da37f843e0e7b0908",
                  "name":"Create Project update",
                  "role":0,
                  "new_role":0
               }
            ],
            "description":"Delete project",
            "type":"PROJECT",
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"0e6bd8bcd6a742f19805117cd367fc22",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":3,
         "history_type":301,
         "project_id":"e9ac4e663b26477da37f843e0e7b0908",
         "create_date":"2015/09/10 06:52:29",
         "last_update":1441885949107,
         "data":{  
            "result":[  
               {  
                  "id":"e9ac4e663b26477da37f843e0e7b0908",
                  "name":"Create Project",
                  "new_name":"Create Project update",
                  "role":0,
                  "new_role":0
               }
            ],
            "description":"Update project",
            "type":"PROJECT",
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"347491a90ed24f3aad2c1ba45eb048ad",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":3,
         "history_type":300,
         "project_id":"e9ac4e663b26477da37f843e0e7b0908",
         "create_date":"2015/09/10 06:41:25",
         "last_update":1441885285595,
         "data":{  
            "result":[  
               {  
                  "id":"e9ac4e663b26477da37f843e0e7b0908",
                  "name":"Create Project",
                  "role":0,
                  "new_role":0
               }
            ],
            "description":"Add new project",
            "type":"PROJECT",
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"1f9f733adbfe4149b50f86823337b776",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"",
         "category":4,
         "history_type":403,
         "project_id":"",
         "create_date":"2015/09/10 06:17:37",
         "last_update":1441883857640,
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"5c27d23c52b643e980500ff9191bbbc5",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":4,
         "history_type":404,
         "create_date":"2015/09/10 05:15:39",
         "last_update":1441880139108,
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"c4cad9d9ff614930b536debf9cb35f2a",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":4,
         "history_type":404,
         "create_date":"2015/09/10 05:15:39",
         "last_update":1441880139233,
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"8218ebe29cf1424aa5de348269eef05d",
         "user_id":"714a93c5b3074edebdeb3ba9c71a5981",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"",
         "category":4,
         "history_type":403,
         "project_id":"",
         "create_date":"2015/09/10 04:46:19",
         "last_update":1441878379953,
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"5a81482bca834cb0b73111739f8858d2",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"",
         "category":4,
         "history_type":403,
         "project_id":"",
         "create_date":"2015/09/10 04:45:39",
         "last_update":1441878339040,
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"fedd47dbd54e4c58baffa6a875316429",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":4,
         "history_type":402,
         "project_id":"",
         "create_date":"2015/09/09 06:12:21",
         "last_update":1441797141472,
         "data":{  
            "result":[  
               {  
                  "id":"df52058ac0e7431da9b4d00d5540a6af",
                  "role":2,
                  "new_role":0,
                  "first_name":"Le",
                  "last_name":"Tran"
               }
            ],
            "description":"user delete",
            "type":"USER",
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"23c55130c1984fe588ce8fbfc79e398f",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":4,
         "history_type":401,
         "project_id":"",
         "create_date":"2015/09/09 06:05:37",
         "last_update":1441796737366,
         "data":{  
            "result":[  
               {  
                  "id":"df52058ac0e7431da9b4d00d5540a6af",
                  "role":2,
                  "new_role":0,
                  "first_name":"Le",
                  "last_name":"Tran"
               }
            ],
            "description":"Update User",
            "type":"USER",
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"286fc02aac8844dfb104f85252276620",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"",
         "category":4,
         "history_type":403,
         "project_id":"",
         "create_date":"2015/09/09 06:05:05",
         "last_update":1441796705238,
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"ae2ec9cc7a49488792930aafca9d921c",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":4,
         "history_type":400,
         "project_id":"",
         "create_date":"2015/09/09 05:02:23",
         "last_update":1441792943297,
         "data":{  
            "result":[  
               {  
                  "id":"b4124eb7bfc94896b5a4199cb84e82da",
                  "role":2,
                  "new_role":0,
                  "first_name":"Quy",
                  "last_name":"Duong"
               },
               {  
                  "id":"df52058ac0e7431da9b4d00d5540a6af",
                  "role":3,
                  "new_role":0,
                  "first_name":"Le",
                  "last_name":"Tran"
               }
            ],
            "description":"Create user",
            "type":"USER",
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"5490f0b10a0e4c22b613f5e3e8e91be3",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":4,
         "history_type":402,
         "project_id":"",
         "create_date":"2015/09/09 05:01:41",
         "last_update":1441792901337,
         "data":{  
            "result":[  
               {  
                  "id":"bc031fb4fa6743ed86568a9a25903cd5",
                  "role":3,
                  "new_role":0,
                  "first_name":"Le",
                  "last_name":"Tran"
               },
               {  
                  "id":"0fe96f4dcb054711ae3258c7feafbee1",
                  "role":2,
                  "new_role":0,
                  "first_name":"Quy",
                  "last_name":"Duong"
               }
            ],
            "description":"user delete",
            "type":"USER",
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"a5cc041e28094a6784020ef0edc00ffa",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":4,
         "history_type":400,
         "project_id":"",
         "create_date":"2015/09/09 04:33:20",
         "last_update":1441791200384,
         "data":{  
            "result":[  
               {  
                  "id":"0fe96f4dcb054711ae3258c7feafbee1",
                  "role":2,
                  "new_role":0,
                  "first_name":"Quy",
                  "last_name":"Duong"
               },
               {  
                  "id":"bc031fb4fa6743ed86568a9a25903cd5",
                  "role":3,
                  "new_role":0,
                  "first_name":"Le",
                  "last_name":"Tran"
               }
            ],
            "description":"Create user",
            "type":"USER",
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:38:02"
      },
      {  
         "history_id":"55f7415f187c41b49baf5dd86371cbe0",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":4,
         "history_type":402,
         "project_id":"",
         "create_date":"2015/09/09 04:33:15",
         "last_update":1441791195933,
         "data":{  
            "result":[  
               {  
                  "id":"cee917b5dd694f5ab3da9b581689872d",
                  "role":2,
                  "new_role":0,
                  "first_name":"Quy",
                  "last_name":"Duong"
               },
               {  
                  "id":"a34479b4b42f4ae1b41deeaff1930fca",
                  "role":3,
                  "new_role":0,
                  "first_name":"Le",
                  "last_name":"Tran"
               }
            ],
            "description":"user delete",
            "type":"USER",
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:38:02"
      }
   ],
   "description":"OK",
   "status_code":200,
   "total_records":null
}
```

## GET HISTORY BY PROJECT

The API is to get history by project.

### URL
- GET
```` URL
  (GET)http://{Server name}:{Port}/{Context root}/api/history/project
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current user auth_token |
| project_id | String | (Required) the team id |
| folder_ids | String | (Optional) the folder_id is to get history |
| file_ids | String | (Optional) the file_id is to get history |
| page_size | Integer | (Optional) the number of history will be got at one time |
| page_number | Integer | (Optional) the page start to get history |
| history_types | String | (Optional) history type to get |
| last_update | Long | (Optional) last update |

#### Response example
```json
{  
   "result":[  
      {  
         "history_id":"f5b35d20350e44c6825d745afd7f1707",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":4,
         "history_type":410,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 04:13:51",
         "last_update":1441962831128,
         "data":{  
            "result":[  
               {  
                  "name":"testuser002@gmail.com",
                  "role":0,
                  "new_role":0
               }
            ],
            "description":"User Share Link",
            "type":"USER",
            "shared_object":{  
               "id":"7d2c77f899ec46b783d89e6c1791f62f",
               "name":"HoGo_Pro_Alpha_Notifications.pptx",
               "role":0,
               "new_role":0,
               "content_type":"application/vnd.openxmlformats-officedocument.presentationml.presentation"
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:20"
      },
      {  
         "history_id":"98d694a6d9414a0db1d153205185c647",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":4,
         "history_type":408,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 04:13:45",
         "last_update":1441962825918,
         "data":{  
            "description":"User Create Link",
            "type":"USER",
            "shared_object":{  
               "id":"7d2c77f899ec46b783d89e6c1791f62f",
               "name":"HoGo_Pro_Alpha_Notifications.pptx",
               "role":0,
               "new_role":0,
               "content_type":"application/vnd.openxmlformats-officedocument.presentationml.presentation"
            },
            "link":{  
               "link_id":"32797704c38145908fd497527b67cf57",
               "link_url":"view-link/32797704c38145908fd497527b67cf57",
               "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
               "folder_id":null,
               "file_id":"7d2c77f899ec46b783d89e6c1791f62f",
               "emails":"",
               "password":"123",
               "create_date":"2015/09/11 09:13:45",
               "expiry_date":"2015/09/12 23:59:59",
               "is_public":1,
               "status":1,
               "linktype":3
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:20"
      },
      {  
         "history_id":"881843d824f843d1a80fe85f72b778e6",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":4,
         "history_type":410,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 03:47:50",
         "last_update":1441961270788,
         "data":{  
            "result":[  
               {  
                  "name":"testuser002@gmail.com",
                  "role":0,
                  "new_role":0
               }
            ],
            "description":"User Share Link",
            "type":"USER",
            "shared_object":{  
               "id":"7d2c77f899ec46b783d89e6c1791f62f",
               "name":"HoGo_Pro_Alpha_Notifications.pptx",
               "role":0,
               "new_role":0,
               "content_type":"application/vnd.openxmlformats-officedocument.presentationml.presentation"
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:20"
      },
      {  
         "history_id":"6df797792d364dffbc222f3370587538",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "category":4,
         "history_type":408,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 03:47:38",
         "last_update":1441961258598,
         "data":{  
            "description":"User Create Link",
            "type":"USER",
            "shared_object":{  
               "id":"7d2c77f899ec46b783d89e6c1791f62f",
               "name":"HoGo_Pro_Alpha_Notifications.pptx",
               "role":0,
               "new_role":0,
               "content_type":"application/vnd.openxmlformats-officedocument.presentationml.presentation"
            },
            "link":{  
               "link_id":"3eb0a82f92fd4fac8f0f986176e05f47",
               "link_url":"view-link/3eb0a82f92fd4fac8f0f986176e05f47",
               "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
               "folder_id":null,
               "file_id":"7d2c77f899ec46b783d89e6c1791f62f",
               "emails":"",
               "password":"123",
               "create_date":"2015/09/11 08:47:38",
               "expiry_date":"2015/09/12 23:59:59",
               "is_public":1,
               "status":1,
               "linktype":3
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:20"
      },
      {  
         "history_id":"0ddc5fbe708d47a48eb2ab08fd8bbabe",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"2e851844f62d44d2af3fd938f508d5c2",
         "category":2,
         "history_type":803,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 03:34:24",
         "last_update":1441960464057,
         "data":{  
            "result":[  
               {  
                  "id":"2e851844f62d44d2af3fd938f508d5c2",
                  "name":"NIT-Software 's Quotation - Care Reach App (1).xlsx",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
               }
            ],
            "description":"Delete file",
            "type":"FILE",
            "parent":{  
               "id":"bf2ea6d6dcab4c11a38717191cce43ce",
               "name":"test002 test",
               "content_type":"application/project"
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:20"
      },
      {  
         "history_id":"a1305810729e4e3bb8b5fbe814a18efa",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"",
         "folder_ids":"2fbf5c793d8f41a581a1ecf82fbcbbcc",
         "category":5,
         "history_type":803,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 03:34:23",
         "last_update":1441960463470,
         "data":{  
            "result":[  
               {  
                  "id":"2fbf5c793d8f41a581a1ecf82fbcbbcc",
                  "name":"XXX",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/folder"
               }
            ],
            "description":"Delete folder",
            "type":"FOLDER",
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      },
      {  
         "history_id":"7061dfd50eba4296aa96d288d69838d3",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "folder_ids":"146abd0f33184ac38efd67738dbbeeaf",
         "category":5,
         "history_type":804,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 03:30:26",
         "last_update":1441960226496,
         "data":{  
            "result":[  
               {  
                  "id":"146abd0f33184ac38efd67738dbbeeaf",
                  "name":"YY",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/folder"
               }
            ],
            "description":"Restore folder",
            "type":"FOLDER",
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      },
      {  
         "history_id":"865dc1ee86ac4d3e8d2b0a2f4f830764",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"bb2dcba1bfc24793aca94567e019b92f",
         "category":2,
         "history_type":804,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 03:30:26",
         "last_update":1441960226806,
         "data":{  
            "result":[  
               {  
                  "id":"bb2dcba1bfc24793aca94567e019b92f",
                  "name":"File rename",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/vnd.openxmlformats-officedocument.presentationml.presentation"
               }
            ],
            "description":"Restore file",
            "type":"FILE",
            "parent":{  
               "id":"bf2ea6d6dcab4c11a38717191cce43ce",
               "name":"test002 test",
               "content_type":"application/project"
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      },
      {  
         "history_id":"7ab24505d3524e9cbc2ce89bff68463e",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"7d2c77f899ec46b783d89e6c1791f62f",
         "category":2,
         "history_type":802,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 03:19:12",
         "last_update":1441959552969,
         "data":{  
            "result":[  
               {  
                  "id":"7d2c77f899ec46b783d89e6c1791f62f",
                  "name":"HoGo_Pro_Alpha_Notifications.pptx",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/vnd.openxmlformats-officedocument.presentationml.presentation"
               }
            ],
            "description":"Move file",
            "type":"FILE",
            "parent":{  
               "id":"bf2ea6d6dcab4c11a38717191cce43ce",
               "name":"test002 test",
               "content_type":"application/project"
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      },
      {  
         "history_id":"e48a32352d4b42698277cff15855c38b",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"2e851844f62d44d2af3fd938f508d5c2,4f3e9310a5114207a9238baf8bfdba26,903fe7a4336a4e5f8462ff8d2a85c801",
         "category":2,
         "history_type":801,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 03:19:03",
         "last_update":1441959543560,
         "data":{  
            "result":[  
               {  
                  "id":"bf2ea6d6dcab4c11a38717191cce43ce",
                  "name":"NIT-Software 's Quotation - Care Reach App (1).xlsx",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
               },
               {  
                  "id":"bf2ea6d6dcab4c11a38717191cce43ce",
                  "name":"NIT-Software 's Quotation - Care Reach App (1).xlsx",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
               },
               {  
                  "id":"bf2ea6d6dcab4c11a38717191cce43ce",
                  "name":"NIT-Software 's Quotation - Care Reach App (1).xlsx",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
               }
            ],
            "description":"Remove file",
            "type":"FILE",
            "parent":{  
               "id":"bf2ea6d6dcab4c11a38717191cce43ce",
               "name":"test002 test",
               "content_type":"application/project"
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      },
      {  
         "history_id":"677e3681f895477597f518d80aea55e5",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"fb9f5987f9f6469bb84baa5dca27266e",
         "category":2,
         "history_type":802,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 03:18:44",
         "last_update":1441959524534,
         "data":{  
            "result":[  
               {  
                  "id":"fb9f5987f9f6469bb84baa5dca27266e",
                  "name":"NIT-Software 's Quotation - Care Reach App (1).xlsx",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
               }
            ],
            "description":"Move file",
            "type":"FILE",
            "parent":{  
               "id":"bf2ea6d6dcab4c11a38717191cce43ce",
               "name":"test002 test",
               "content_type":"application/project"
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      },
      {  
         "history_id":"57daff70793f4546bb85dc3ab5bef0b3",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"7d2c77f899ec46b783d89e6c1791f62f",
         "category":2,
         "history_type":802,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 03:08:16",
         "last_update":1441958896785,
         "data":{  
            "result":[  
               {  
                  "id":"7d2c77f899ec46b783d89e6c1791f62f",
                  "name":"HoGo_Pro_Alpha_Notifications.pptx",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/vnd.openxmlformats-officedocument.presentationml.presentation"
               }
            ],
            "description":"Move file",
            "type":"FILE",
            "parent":{  
               "id":"1826fb09c2c146c18076436383aa50c6",
               "name":"Test02",
               "content_type":"application/folder"
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      },
      {  
         "history_id":"7bdb792909e143aba11679aa300d0d29",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "folder_ids":"f0e23f457bf54739b9508f3b291e5ff2",
         "category":5,
         "history_type":802,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 03:08:16",
         "last_update":1441958896606,
         "data":{  
            "result":[  
               {  
                  "id":"f0e23f457bf54739b9508f3b291e5ff2",
                  "name":"QQQ",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/folder"
               }
            ],
            "description":"Move folder",
            "type":"FOLDER",
            "parent":{  
               "id":"1826fb09c2c146c18076436383aa50c6",
               "name":"Test02",
               "content_type":"application/folder"
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      },
      {  
         "history_id":"1d9bdb6c8a56495fa038ddf89cd4a53f",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"bb2dcba1bfc24793aca94567e019b92f",
         "category":2,
         "history_type":801,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 02:21:54",
         "last_update":1441956114294,
         "data":{  
            "result":[  
               {  
                  "id":"bf2ea6d6dcab4c11a38717191cce43ce",
                  "name":"File rename",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/vnd.openxmlformats-officedocument.presentationml.presentation"
               }
            ],
            "description":"Remove file",
            "type":"FILE",
            "parent":{  
               "id":"bf2ea6d6dcab4c11a38717191cce43ce",
               "name":"test002 test",
               "content_type":"application/project"
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      },
      {  
         "history_id":"4b2b06de97054bec91e97dbbc4e50d58",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"",
         "folder_ids":"42e4c4c41fe146b0a9705871fce0140a",
         "category":5,
         "history_type":801,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 02:21:49",
         "last_update":1441956109555,
         "data":{  
            "result":[  
               {  
                  "id":"42e4c4c41fe146b0a9705871fce0140a",
                  "name":"Test Folder rename",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/folder"
               }
            ],
            "description":"Remove folder",
            "type":"FOLDER",
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      },
      {  
         "history_id":"e7a1f35cfefe41919b579c5ce0d7c9c5",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"bb2dcba1bfc24793aca94567e019b92f",
         "category":2,
         "history_type":800,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 02:18:06",
         "last_update":1441955886789,
         "data":{  
            "result":[  
               {  
                  "id":"bb2dcba1bfc24793aca94567e019b92f",
                  "name":"HoGo2 Requirements.pptx.pptx",
                  "new_name":"File rename",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/vnd.openxmlformats-officedocument.presentationml.presentation"
               }
            ],
            "description":"Update file",
            "type":"FILE",
            "parent":{  
               "id":"bf2ea6d6dcab4c11a38717191cce43ce",
               "name":"test002 test",
               "content_type":"application/project"
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      },
      {  
         "history_id":"a2b37b4f04ef40b1bb25b1783bc82bfc",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "folder_ids":"42e4c4c41fe146b0a9705871fce0140a",
         "category":5,
         "history_type":800,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 02:17:29",
         "last_update":1441955849624,
         "data":{  
            "result":[  
               {  
                  "id":"42e4c4c41fe146b0a9705871fce0140a",
                  "name":"Test Folder",
                  "new_name":"Test Folder rename",
                  "role":0,
                  "new_role":0
               }
            ],
            "description":"Update folder",
            "type":"FOLDER",
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      },
      {  
         "history_id":"e866100c115f4a688a6010b124a5057e",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "folder_ids":"42e4c4c41fe146b0a9705871fce0140a",
         "category":5,
         "history_type":500,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/11 02:12:32",
         "last_update":1441955552389,
         "data":{  
            "result":[  
               {  
                  "id":"42e4c4c41fe146b0a9705871fce0140a",
                  "name":"Test Folder",
                  "role":0,
                  "new_role":0,
                  "content_type":"application/folder"
               }
            ],
            "description":"Create folder",
            "type":"FOLDER",
            "parent":{  
               "id":"bf2ea6d6dcab4c11a38717191cce43ce",
               "name":"test002 test",
               "content_type":"application/project"
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      },
      {  
         "history_id":"e44fb01be1b04b009df5a2783ba938d0",
         "user_id":"714a93c5b3074edebdeb3ba9c71a5981",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"7d2c77f899ec46b783d89e6c1791f62f,bb2dcba1bfc24793aca94567e019b92f",
         "category":2,
         "history_type":200,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/08 05:56:42",
         "last_update":1441709803918,
         "data":{  
            "result":[  
               {  
                  "id":"7d2c77f899ec46b783d89e6c1791f62f",
                  "name":"HoGo_Pro_Alpha_Notifications.pptx",
                  "role":0,
                  "new_role":0,
                  "cloud_type":0,
                  "content_type":"application/vnd.openxmlformats-officedocument.presentationml.presentation"
               },
               {  
                  "id":"bb2dcba1bfc24793aca94567e019b92f",
                  "name":"HoGo2 Requirements.pptx.pptx",
                  "role":0,
                  "new_role":0,
                  "cloud_type":0,
                  "content_type":"application/vnd.openxmlformats-officedocument.presentationml.presentation"
               }
            ],
            "description":"Add new file",
            "type":"FILE",
            "parent":{  
               "id":"bf2ea6d6dcab4c11a38717191cce43ce",
               "name":"test002 test",
               "content_type":"application/project"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      },
      {  
         "history_id":"7e82ee0b7f044c77a9b5b96b2df9eaa1",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "file_ids":"68bf066e31fe45e2afea7978e99a09ef",
         "category":2,
         "history_type":200,
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "create_date":"2015/09/08 05:54:01",
         "last_update":1441709641803,
         "data":{  
            "result":[  
               {  
                  "id":"68bf066e31fe45e2afea7978e99a09ef",
                  "name":"HoGoPro_CSV_File_Template.csv",
                  "role":0,
                  "new_role":0,
                  "cloud_type":0,
                  "content_type":"text/csv"
               }
            ],
            "description":"Add new file",
            "type":"FILE",
            "parent":{  
               "id":"bf2ea6d6dcab4c11a38717191cce43ce",
               "name":"test002 test",
               "content_type":"application/project"
            },
            "user_action":{  
               "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
               "team_id":"34ee29628110424696ea902bf5b342f2",
               "role_id":1,
               "email_address":"le.tran@nit-software.com",
               "first_name":"Le",
               "last_name":"Tran",
               "sign_up_date":"2015/07/27 08:10:57"
            }
         },
         "server_time":"2015/09/11 12:44:21"
      }
   ],
   "description":"OK",
   "status_code":200,
   "total_records":85
}
```