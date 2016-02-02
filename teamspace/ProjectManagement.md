# Project Management API

## CREATE PROJECT

The API is to create new project in team.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/create
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| name | String | (Required) project name |
| description | String | (Optional) project description |
| setting | String | (Optional) (default value: 000000) project settings |
|user_ids| String | (Optional) set User Id outside project that would be received notification when there is new update on project |

#### Project setting description
| Value | Description|
|:---|:---|
| 0 | Disable (default) |
| 1 | Enable|

![projectsetting](https://cloud.githubusercontent.com/assets/1794584/12739452/74324724-c99c-11e5-97a0-df933881b8a4.png)



#### Response example
```json
{
    "result": {
        "project_id": "a87570a5121a451088f8bd3c932715c8",
        "team_id": "hogo",
        "name": "Project Name",
        "description": "Project description",
        "project_type": 1,
        "create_date": "2016/02/02 03:57:51",
        "modify_date": null,
        "max_download": 1,
        "status": 1,
        "setting": "000000",
        "notify_user": "[]",
        "forward": ""
    },
    "status_code": 200,
    "total_records": null,
    "server_time": null
}
```

## UPDATE PROJECT

The API is to update project info.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/edit
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| project_id | String | (Required) the project id will be updated |
| name | String | (Required) new project name |
| description | String | (Optional) new project description |
| setting | String | (Optional) (default value: 000000) project settings |
|user_ids| String | (Optional) set User Id outside project that would be received notification when there is new update on project |

#### Project setting description
| Value | Description|
|:---|:---|
| 0 | Disable (default) |
| 1 | Enable|

![projectsetting](https://cloud.githubusercontent.com/assets/1794584/12739452/74324724-c99c-11e5-97a0-df933881b8a4.png)



#### Response example
```json
{
    "result": {
        "project_id": "a87570a5121a451088f8bd3c932715c8",
        "team_id": "hogo",
        "name": "Project Name",
        "description": "Project description",
        "project_type": 1,
        "create_date": "2016/02/02 03:57:51",
        "modify_date": null,
        "max_download": 1,
        "status": 1,
        "setting": "000000",
        "notify_user": "[]",
        "forward": ""
    },
    "status_code": 200,
    "total_records": null,
    "server_time": null
}
```


## DELETE PROJECT

The API is to delete project. Only project owner is able to delete project.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/delete
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| project_id | String | (Required) the project_id of project will be deleted |

#### Response example
```json
{  
   "status_code":200,
   "total_records":null
}
```

## UPLOAD FILES

The API is to upload files from computer to HoGoPro.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/upload
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| file_name | String | (Required) name of file |
| file | MultipartFile |(Required)  a file is uploaded |
| auth_token | String | (Required) the current auth_token |
| folder_id | String | (Required) parent folder_id, could be null |
| project_id | String | (Required) project_id |
| name | String | (Optional) just use for multipart upload|
| chunk | String | (Optional) just use for multipart upload |
| chunks | String | (Optional) just use for multipart upload|
| session_upload | String | (Optional) |

#### Response example
```json
{  
   "result":{  
      "file_id":"73e03f3795d543598ac49661f645d347",
      "team_id":"34ee29628110424696ea902bf5b342f2",
      "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
      "upload_file_id":"73e03f3795d543598ac49661f645d347",
      "be_contents_id":"_",
      "be_contents_id_p":"_",
      "krpdfx_be_contents_id":"_",
      "krpdfx_be_contents_id_p":"_",
      "is_encrypt":0,
      "title":"AngularJS Interview Questions & Answers - By Shailendra Chauhan.pdf",
      "description":"AngularJS Interview Questions & Answers - By Shailendra Chauhan.pdf",
      "file_type":1,
      "create_date":"2015/09/10 12:10:31",
      "modify_date":"2015/09/10 07:10:31",
      "file_size":1871618,
      "thumbnail":null,
      "status":1,
      "in_recycle_bin":0,
      "content_type":"application/pdf"
   },
   "status_code":200,
   "total_records":null
}
```
## UPLOAD FILES FROM CLOUD

The API is to upload files from could(Dropbox, Box, GoogleDrive).

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/upload/cloud
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| file_name | String | (Required) name of file |
| content_url | String | (Required) the loud url of file is uploaded |
| file_type | String | (Required) file type |
| folder_id | String | (Required) parent folder_id, could be set NULL if it's root folder |
| project_id | String | (Optional) project_id |
| session_upload | String | (Optional) |
| cloud_type | int | (Required) DROPBOX(1), BOX(2), GOOGLE_DRIVE(3) |

#### Response example
```json
{  
   "result":{  
      "file_id":"3a838b62c69b48c39db2ffa4834d0396",
      "team_id":"ac8ab8d709f842ea99f1fbea4e358f23",
      "user_id":"d6258f5480f84bf1b566744b53283262",
      "upload_file_id":"3a838b62c69b48c39db2ffa4834d0396",
      "be_contents_id":"_",
      "be_contents_id_p":"_",
      "krpdfx_be_contents_id":"_",
      "krpdfx_be_contents_id_p":"_",
      "is_encrypt":0,
      "title":"HoGoPro_CSV_File_Template.csv",
      "description":"HoGoPro_CSV_File_Template.csv",
      "file_type":5,
      "create_date":"2015/09/10 12:27:55",
      "modify_date":"2015/09/10 19:27:55",
      "file_size":175,
      "thumbnail":null,
      "status":1,
      "in_recycle_bin":0,
      "content_type":"text/csv"
   },
   "status_code":200,
   "total_records":null
}
```

## ENCODE & REGISTER LICENSE

The API is to encode file & register license for member in project

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/encode/start/license
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| file_ids | String | (Required) list of file_id will be encoded |
| transaction_id | String | (Optional) just use in case encode multiple file|
| project_id | String | (Required) project_id |
| label | String | (Optional) Document label name in UTF8 encoding, default: empty, string (< 32 bytes) |
| printable | int | 0 or 1 (0: does not allow print, 1: allow print) |
| editable | int | 0 or 1 (0: does not allow edit, 1: allow edit)  |
| expiry_date | String | (Required)  the encoded file will be expire at this date, format “yyyy/mm/dd hh:mm:ss”. Could be set empty "" for no limited |
| local_copy | int | 1 - 10, the number of local copy allow, default is 2 |

#### Response example
```json
{  
   "result":"OK",
   "description":"",
   "status_code":200,
   "total_records":null
}
```

## CHECK ENCODE STATUS

The API is to check the encode status of a file.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/encode/status
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| file_ids | String | (Required) list of file ids is encoding |

#### Response example
```json
{  
   "result":[  
      {  
         "status_encode":2,
         "description":"Document is encoding",
         "file_id":"58d4d9e1b8284fafad7123a6468fcc4e"
      }
   ],
   "description":"OK",
   "status_code":200,
   "total_records":null
}
```
```json
{  
   "result":[  
      {  
         "status_encode":3,
         "description":"OK - Encode successfully!",
         "file_id":"58d4d9e1b8284fafad7123a6468fcc4e"
      }
   ],
   "description":"OK",
   "status_code":200,
   "total_records":null
}
```

## CREATE FOLDER

The API is to create new folder in project.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/f/create
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| project_id | String | (Required) the project parent id |
| parent_folder_id | String | (Required) folder parent id, could be set NULL if it's root folder |
| name | String | (Required) name of project |

#### Response example
```json
{  
   "result":{  
      "folder_id":"42e4c4c41fe146b0a9705871fce0140a",
      "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
      "parent_folder_id":null,
      "name":"Test Folder",
      "create_date":"2015/09/11 07:12:31",
      "modify_date":null,
      "status":1
   },
   "status_code":200,
   "total_records":null
}
```

## EDIT FOLDER/FILE

The API is to update folder/file name.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/f/edit
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| project_id | String | (Required) the project parent id |
| folder_id | String | (Required) folder_id will be edited |
| file_id | String | (Required) file_id will be edited |
| name | String | (Required) |

#### Response example
```json
{  
   "result":{  
      "folder_id":"42e4c4c41fe146b0a9705871fce0140a",
      "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
      "parent_folder_id":null,
      "name":"Test Folder rename",
      "create_date":"2015/09/11 07:12:31",
      "modify_date":"2015/09/11 02:17:29",
      "status":1
   },
   "status_code":200,
   "total_records":null
}
```
```json
{  
   "result":{  
      "file_id":"bb2dcba1bfc24793aca94567e019b92f",
      "team_id":"34ee29628110424696ea902bf5b342f2",
      "user_id":"714a93c5b3074edebdeb3ba9c71a5981",
      "upload_file_id":"bb2dcba1bfc24793aca94567e019b92f",
      "be_contents_id":"_",
      "be_contents_id_p":"_",
      "krpdfx_be_contents_id":"_",
      "krpdfx_be_contents_id_p":"_",
      "is_encrypt":0,
      "title":"File rename",
      "description":"HoGo2 Requirements.pptx.pptx",
      "file_type":4,
      "create_date":"2015/09/08 10:56:43",
      "modify_date":"2015/09/11 02:18:06",
      "file_size":489298,
      "thumbnail":null,
      "status":1,
      "in_recycle_bin":0,
      "content_type":"application/vnd.openxmlformats-officedocument.presentationml.presentation"
   },
   "status_code":200,
   "total_records":null
}
```

## DELETE FOLDER/FILE

This API is to delete folder/file.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/f/delete
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| project_id | String | (Required) the project parent id |
| folder_id | String | (Required) folder_id will be deleted |
| file_id | String | (Required) file_id will be deleted |

#### Response example
```json
{  
   "status_code":200,
   "total_records":null
}
```

## GET PROJECT INFO

The API is to get project info. However, only auth_token of user in the project is able to call the API.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/info
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| project_id | String | (Required) the project_id will be get data |

#### Response example
```json
{  
   "result":{  
      "number_of_file":6,
      "create_date":"2015/09/04 02:08:06",
      "status":1,
      "number_of_user":2,
      "description":"",
      "modify_date":"2015/09/07 07:13:32",
      "name":"test002 test",
      "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
      "max_download":1,
      "project_type":1,
      "team_id":"34ee29628110424696ea902bf5b342f2"
   },
   "status_code":200,
   "total_records":null
}
```

## GET PROJECT LIST

The API is to get the project list of a user.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/list
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| search_key | String | (Optional) search key to look for project with the name like this |
| sort_key | int | (Optional) (default value: 6) sort by create_date DESC |
| length | int | (Optional) (default value: 10) the number of projects will get  |
| start | int | (Optional) (default value: 10) the position of project will start to be get |
| draw | String | (Optional) |

#### Response example
```json
{  
   "result":{  
      "draw":"1",
      "total_result":2,
      "data":[  
         {  
            "project_id":"07572640562b4df4bc4bc9d8f11a56e4",
            "project_name":"test 002 test",
            "owner_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
            "owner_name":"Le Tran",
            "create_date":"2015/09/07 02:13:52",
            "number_file":1,
            "number_member":2,
            "link":null,
            "project_role_id":1,
            "total_result":2
         },
         {  
            "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
            "project_name":"test002 test",
            "owner_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
            "owner_name":"Le Tran",
            "create_date":"2015/09/04 02:08:06",
            "number_file":6,
            "number_member":2,
            "link":null,
            "project_role_id":1,
            "total_result":2
         }
      ]
   },
   "status_code":200,
   "total_records":null
}
```

## GET FILES&FOLDERS IN PROJECT/FOLDER

The API is to get files/folder in project/folder parent.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/f/browse
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| project_id | String | (Required) the project parent id |
| folder_id | String | (Required) the folder parent id, could be set NULL  |
| search_key | String | (Optional) key word to search for folder/file |
| sort_key | int | (Optional) (default value: 1) |
| active | boolean | (Optional) (default value: 'true') |
| folder_only | boolean | (Optional) (default value: 'false') |
| search_global | boolean | (Optional) (default value: 'false') |

#### Response example
```json
{  
   "result":{  
      "member":[  
         {  
            "create_date":"2015/09/04 07:08:06",
            "status":1,
            "project_role_id":1,
            "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1"
         },
         {  
            "create_date":"2015/09/04 07:08:06",
            "status":1,
            "project_role_id":2,
            "user_id":"714a93c5b3074edebdeb3ba9c71a5981"
         }
      ],
      "project":{  
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "name":"test002 test",
         "description":"",
         "project_type":1,
         "create_date":"2015/09/04 07:08:06",
         "modify_date":"2015/09/07 07:13:32",
         "max_download":1,
         "status":1
      },
      "file_info":[  
         {  
            "id":"77551145cf8849d58f1223064f63a20f",
            "name":"KKKKKK",
            "file_type":0,
            "is_folder":true,
            "last_modified_date":null,
            "parent_folder_id":null,
            "file_size":0,
            "status":1,
            "is_encrypt":0,
            "thumbnail":null,
            "content_type":null
         },
         {  
            "id":"f0e23f457bf54739b9508f3b291e5ff2",
            "name":"QQQ",
            "file_type":0,
            "is_folder":true,
            "last_modified_date":null,
            "parent_folder_id":null,
            "file_size":0,
            "status":1,
            "is_encrypt":0,
            "thumbnail":null,
            "content_type":null
         },
         {  
            "id":"1826fb09c2c146c18076436383aa50c6",
            "name":"Test02",
            "file_type":0,
            "is_folder":true,
            "last_modified_date":null,
            "parent_folder_id":null,
            "file_size":0,
            "status":1,
            "is_encrypt":0,
            "thumbnail":null,
            "content_type":null
         },
         {  
            "id":"68bf066e31fe45e2afea7978e99a09ef",
            "name":"HoGoPro_CSV_File_Template.csv",
            "file_type":5,
            "is_folder":false,
            "last_modified_date":"2015/09/08 05:54:01",
            "parent_folder_id":null,
            "file_size":155,
            "status":1,
            "is_encrypt":0,
            "thumbnail":null,
            "content_type":"text/csv"
         },
         {  
            "id":"7d2c77f899ec46b783d89e6c1791f62f",
            "name":"HoGo_Pro_Alpha_Notifications.pptx",
            "file_type":4,
            "is_folder":false,
            "last_modified_date":"2015/09/08 05:56:42",
            "parent_folder_id":null,
            "file_size":151483,
            "status":1,
            "is_encrypt":0,
            "thumbnail":null,
            "content_type":"application/vnd.openxmlformats-officedocument.presentationml.presentation"
         },
         {  
            "id":"2e851844f62d44d2af3fd938f508d5c2",
            "name":"NIT-Software 's Quotation - Care Reach App (1).xlsx",
            "file_type":3,
            "is_folder":false,
            "last_modified_date":"2015/09/04 05:37:12",
            "parent_folder_id":null,
            "file_size":18175,
            "status":1,
            "is_encrypt":0,
            "thumbnail":null,
            "content_type":"application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
         },
         {  
            "id":"4f3e9310a5114207a9238baf8bfdba26",
            "name":"NIT-Software 's Quotation - Care Reach App (1).xlsx",
            "file_type":3,
            "is_folder":false,
            "last_modified_date":"2015/09/04 05:32:28",
            "parent_folder_id":null,
            "file_size":18175,
            "status":1,
            "is_encrypt":0,
            "thumbnail":null,
            "content_type":"application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
         },
         {  
            "id":"903fe7a4336a4e5f8462ff8d2a85c801",
            "name":"NIT-Software 's Quotation - Care Reach App (1).xlsx",
            "file_type":3,
            "is_folder":false,
            "last_modified_date":"2015/09/04 05:36:17",
            "parent_folder_id":null,
            "file_size":18175,
            "status":1,
            "is_encrypt":0,
            "thumbnail":null,
            "content_type":"application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
         }
      ]
   },
   "status_code":200,
   "total_records":null
}
```

## MOVE FOLDER/FILE

The API is to move folder/file.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/f/move
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| project_id | String | (Required) the project parent id |
| folder_id | String | (Required) folder_id of folder will be moved, could be set NULL  |
| file_id | String | (Required) file_id of folder will be moved |
| new_parent_folder_id | String | (Optional) new parent folder id |

#### Response example
```json
{  
   "status_code":200,
   "total_records":null
}
```

## GET FILE INFO

The API is to get file info.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/f/info
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| project_id | String | (Required) the project parent id  |
| f_id | String | (Required) file_id |
| active | boolean | (Optional) (default value: 'true') file status |

#### Response example
```json
{  
   "result":{  
      "file":{  
         "file_id":"68bf066e31fe45e2afea7978e99a09ef",
         "team_id":"34ee29628110424696ea902bf5b342f2",
         "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
         "upload_file_id":"68bf066e31fe45e2afea7978e99a09ef",
         "be_contents_id":"_",
         "be_contents_id_p":"_",
         "krpdfx_be_contents_id":"_",
         "krpdfx_be_contents_id_p":"_",
         "is_encrypt":0,
         "title":"HoGoPro_CSV_File_Template.csv",
         "description":"HoGoPro_CSV_File_Template.csv",
         "file_type":5,
         "create_date":"2015/09/08 10:54:01",
         "modify_date":"2015/09/08 10:54:01",
         "file_size":155,
         "thumbnail":null,
         "status":1,
         "in_recycle_bin":0,
         "content_type":"text/csv"
      },
      "path":[  

      ]
   },
   "status_code":200,
   "total_records":null
}
```

## RESTORE FOLDER/FILE

The API is to restore folder/file which is temporarily deleted.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/f/restore
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| project_id | String | (Required) the project parent id |
| folder_ids | String | (Required) list of folder_ids will be restored |
| file_ids | String | (Required) list of file_ids will be restored, could be set NULL |

#### Response example
```json
{  
   "status_code":200,
   "total_records":null
}
```

## DELETE FOLDERS/FILES FOREVER

The API is to delete folders/files forever from the project.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/f/deleteforever
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| project_id | String | (Required) the project parent id |
| folder_ids | String | (Required) list of folder_ids will be deleted forever, could be set NULL  |
| file_ids | String | (Required) list of file_ids will be deleted forever, could be set NULL  |

#### Response example
```json
{  
   "status_code":200,
   "total_records":null
}
```

## DOWNLOAD FILE 

The API is used to download file.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/download
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| file_id | String | (Required) file_id will be downloaded |
| project_id | String | (Required) the project parent id |
| download_type | int | (Required) NORMAL(1), TO_VIEWER (2), ZIP(3)|
| require_auth | boolean | (Optional) (default value : 'true') |

#### Response example
Return File binary data stream

## INVITE USERS TO PROJECT

The API is to invite members in team to specify project.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/project/invite
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| user_ids | String | (Required) list of member id to be invited |
| project_id | String | (Required) the project parent id |
| project_role_id | int | (Required) Owner(1), Editor (2), Member(3), LimitedMember(4) |
| team_id | String | (Required) team id |
| message | String | (Optional) message to send to member through email |

#### Response example
```json
{  
   "result":"OK",
   "description":"",
   "status_code":200,
   "total_records":null
}
```
## REMOVE USERS FROM PROJECT

The API is to remove users from project.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/project/kick
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| user_ids | String | (Required) list of user ids will be remove from project |
| project_id | String | (Required) the project id |

#### Response example
```json
{  
   "status_code":200,
   "total_records":null
}
```

## UPDATE USER ROLE IN PROJECT

The API is to update member role in project.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/user/project/update
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| auth_token | String | (Required) the current auth_token |
| user_role | String | (Required) list of user change. For intance: xxxx_1, yyyy_2,... which xxxx is user_id, and Owner(1), Editor (2), Member(3), LimitedMember(4) |
| project_id | String | (Required) the project id |

#### Response example
```json
{  
   "status_code":200,
   "total_records":null
}
```
