## GET LICENSE INFO

The API is to get the license info.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/license/info
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
| file_id | String | (Required) the file id to view |
| project_id | String | (Required) the project id |

#### Response example
```json
{  
   "result":{  
      "file_project_pk":{  
         "file_id":"85890caf5aea4d36bdf5fac989a8fa92",
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce"
      },
      "folder_id":null,
      "document_expiry_date":null,
      "printable":0,
      "editable":0,
      "local_copies":0,
      "label":null,
      "status":0
   },
   "description":"OK",
   "status_code":200,
   "total_records":null
}
```

## LICENSE UPDATE

The API is to update the license info.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/license/update
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
| file_ids | String | (Required) list of file id to register license, separated by ',' |
| project_id | String | (Required) the project id |
| label | String | (Optional) |
| printable | int | (Optional) the number of times the file is allowed to print file |
| editable | int | (Optional) the number of times the file is allowed to edit file |
| expiry_date | String | (Optional) the day that the license will be expired |
| local_copy | int | (Optional) the number of times the file is allowed to copy file |
| delete | String | (Optional) accept true/false |

#### Response example
```json
{  
   "result":"OK",
   "description":"",
   "status_code":200,
   "total_records":null
}
```
