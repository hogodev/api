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
| label | String | (Optional) Document label name in UTF8 encoding, default: empty, string (< 32 bytes) |
| printable | int | 0 or 1 (0: does not allow print, 1: allow print |
| editable | int | 0 or 1 (0: does not allow edit, 1: allow edit  |
| expiry_date | String | (Optional) the encoded file will be expire at this date, format “yyyy/mm/dd hh:mm:ss” |
| local_copy | int | 1 - 10, the number of local copy allow, default is 2 |
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
