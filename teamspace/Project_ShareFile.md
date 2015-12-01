# SHARE LINK & MANAGEMENT API

## CREATE LINK

The API is to create link to share to other people.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/link/create
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
| type_share | int | (Required) share type |
| project_id | String | (Required) the parent project_id |
| folder_id | String | (Optional) folder_id will be shared |
| file_id | String | (Optional) file_id will be shared |
| password | String | (Optional) password to access link |
| expiry_date | String | (Optional) the date the link will expire |
| is_public | int | (Optional) (default value: 1) |

#### Response example
```json
{  
   "result":{  
      "link":"view-link/3eb0a82f92fd4fac8f0f986176e05f47",
      "link_id":"3eb0a82f92fd4fac8f0f986176e05f47"
   },
   "status_code":200,
   "total_records":null
}
```

## SHARE LINK

The API is used to share to another people.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/link/share
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
| link_id | String | (Required) the link will be shared |
| emails | String | (Required) list of email which will received the link |
| message | String | (Optional) message in email |

#### Response example
```json
{  
   "status_code":200,
   "total_records":null
}
```

## REMOVE LINK

The API is to remove the active link.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/link/remove
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
| link_id | String | (Required) the link_id will be deactivate |

#### Response example
```json
{  
   "status_code":200,
   "total_records":null
}
```

## GET LINK

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/link/get
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| link_id | String | (Required) the link_id |

#### Response example
```json
{  
   "result":{  
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
   "status_code":200,
   "total_records":null
}
```

## BROWSE LINK

The API is browse folders/files in shared link.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/link/browse
````

### Header

  --------------------------------------------------------------------------------------------------
  *application/x-www-form-urlencoded;charset=UTF-8*
  --------------------------------------------------------------------------------------------------

### Request parameters

  ---------------------------------------------------------------------------- --------------------------------------------------------------------------------- -----------------------
| Name | Data Format | Description |
|:---|:---|:---|
| link_id | String | (Required) the link_id |
| child_folder_id | String | (Optional child folder id |

#### Response example
```json
{  
   "result":[  
      {  
         "id":"d38ca7704f674240a78eae2a21583cda",
         "name":"Folder Test 1.1",
         "file_type":0,
         "is_folder":true,
         "last_modified_date":null,
         "parent_folder_id":"2a36460739cf4f2d92ad06be490b1842",
         "file_size":0,
         "status":1,
         "is_encrypt":0,
         "thumbnail":null,
         "content_type":null
      },
      {  
         "id":"3b07f7c6b2cd4fb489ad7323bfed8324",
         "name":"angularjs-141019044637-conversion-gate01.pdf",
         "file_type":1,
         "is_folder":false,
         "last_modified_date":"2015/09/10 12:44:18",
         "parent_folder_id":"2a36460739cf4f2d92ad06be490b1842",
         "file_size":5663687,
         "status":1,
         "is_encrypt":1,
         "thumbnail":"",
         "content_type":"application/pdf"
      },
      {  
         "id":"f1ab3586a1ae45b5a6fbc68d629cce3d",
         "name":"NIT Software - Purchasing.xlsx",
         "file_type":3,
         "is_folder":false,
         "last_modified_date":"2015/05/14 04:11:41",
         "parent_folder_id":"2a36460739cf4f2d92ad06be490b1842",
         "file_size":58077,
         "status":1,
         "is_encrypt":1,
         "thumbnail":"",
         "content_type":"application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
      }
   ],
   "status_code":200,
   "total_records":null
}
```