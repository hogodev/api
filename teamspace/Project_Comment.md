# Project Comment APIs

## CREATE COMMENT

The API is to create comment on project.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/comment/create
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
| project_id | String | (Required) the project_id |
| text | String | (Required) comment content |

#### Response example
```json
{  
   "result":{  
      "comment_id":"d0326b14d30d489881cdd187e623a5d0",
      "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
      "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
      "text":"123",
      "create_date":"2015/09/11 04:55:10",
      "status":1,
      "last_update":1441965310861
   },
   "status_code":200,
   "total_records":null
}
```

## UPDATE COMMENT

The API is to update comment content. Only comment owner is able to update comment.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/comment/update
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
| project_id | String | (Required) the project_id |
| comment_id | String | (Required) the comment_id will be updated |
| text | String | (Required) new comment content |

#### Response example
```json
{  
   "result":{  
      "comment_id":"d0326b14d30d489881cdd187e623a5d0",
      "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
      "user_id":"4f7d3f4b2d104ea3a5f4ef534b9ae7b1",
      "text":"1234",
      "create_date":"2015/09/11 04:55:10",
      "status":1,
      "last_update":1441965310861
   },
   "status_code":200,
   "total_records":null
}
```

## DELETE COMMENT

The API is to delete comment, and only comment owner can delete the comment.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/comment/delete
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
| project_id | String | (Required) the project_id |
| comment_id | String | (Required) the comment_id will be deleted |

#### Response example
```json
{  
   "status_code":200,
   "total_records":null
}
```

## GET COMMENT

The API is to get comments on project.

### URL
- POST
```` URL
  (POST)http://{Server name}:{Port}/{Context root}/api/project/comment/get
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
| project_id | String | (Required) the project_id |
| sort_key | int | (Optional) (default value: 2, sort by create date DESC) |
| page_size | int | (Optional) (default value: 5) the number of comment will be got |
| page_number | Integer | (Optional) (default value: 0) the page which comment will be got |
| last_update | Long | (Optional) last update |

#### Response example
```json
{  
   "result":[  
      {  
         "comment_id":"0038ee8f4b94422da06b35450de396e4",
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "user_id":"714a93c5b3074edebdeb3ba9c71a5981",
         "text":"test1",
         "create_date":"2015/09/07 02:11:10",
         "status":1,
         "first_name":"Le",
         "middle_name":null,
         "last_name":"Hieu",
         "mail_address":"testuser01@gmail.com"
      },
      {  
         "comment_id":"497826cc380445c993ef8bc9ecc0fc88",
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "user_id":"714a93c5b3074edebdeb3ba9c71a5981",
         "text":"test",
         "create_date":"2015/09/07 02:03:01",
         "status":1,
         "first_name":"Le",
         "middle_name":null,
         "last_name":"Hieu",
         "mail_address":"testuser01@gmail.com"
      },
      {  
         "comment_id":"7173f0fcc9664556a6f71105035e846c",
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "user_id":"714a93c5b3074edebdeb3ba9c71a5981",
         "text":"test",
         "create_date":"2015/09/07 02:01:37",
         "status":1,
         "first_name":"Le",
         "middle_name":null,
         "last_name":"Hieu",
         "mail_address":"testuser01@gmail.com"
      },
      {  
         "comment_id":"f3f111c2465348d1bbb13d494f16820f",
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "user_id":"714a93c5b3074edebdeb3ba9c71a5981",
         "text":"123",
         "create_date":"2015/09/07 02:01:06",
         "status":1,
         "first_name":"Le",
         "middle_name":null,
         "last_name":"Hieu",
         "mail_address":"testuser01@gmail.com"
      },
      {  
         "comment_id":"daf7b051ee444204aa226a9129a33f10",
         "project_id":"bf2ea6d6dcab4c11a38717191cce43ce",
         "user_id":"714a93c5b3074edebdeb3ba9c71a5981",
         "text":"123",
         "create_date":"2015/09/06 23:56:29",
         "status":1,
         "first_name":"Le",
         "middle_name":null,
         "last_name":"Hieu",
         "mail_address":"testuser01@gmail.com"
      }
   ],
   "status_code":200,
   "total_records":5
}
```
