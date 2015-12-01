# Message Box API
  
## GET message inbox BY TEAM

The API is to get all Inbox in the team.

### URL
- GET
```` URL
  (GET)http://{Server name}:{Port}/{Context root}/api/message/inbox
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
| page_size | Integer | (Required) the number of history will be got at one time |
| codes | String | (Required) history type is to be got, ex: 405,406,407 |
| last_update | Long | (Optional) last update |

#### Response example
```json
{
    "result": [{
            "id": "bb09adf8d5d84f4aa3575de28dab3dd2",
            "from_user_id": "52d15ddda9d8425ca0c182bb4b4457ab",
            "from_user_first_name": "Johnny",
            "from_user_last_name": "Le",
            "to_user_id": "336f6be765594fe4b04dc79bfd99b282",
            "team_id": "hogo",
            "project_id": "d05e89067fe54107aab134ea93889f91",
            "project_name": "New project Oct 2015",
            "message_id": null,
            "status": 0,
            "code": 405,
            "last_update": 1444969075755
        }, {
            "id": "3a343e75959041fc9157b1b008b2e412",
            "from_user_id": "52d15ddda9d8425ca0c182bb4b4457ab",
            "from_user_first_name": "Johnny",
            "from_user_last_name": "Le",
            "to_user_id": "336f6be765594fe4b04dc79bfd99b282",
            "team_id": "hogo",
            "project_id": "24ad685439ee4c2b8c090b29443416b6",
            "project_name": "New project Oct 2015-2",
            "message_id": null,
            "status": 0,
            "code": 405,
            "last_update": 1444969052568
        }],
    "description": "OK",
    "status_code": 200,
    "total_records": 2
}

```


## GET all unread message inbox BY TEAM

The API is to get all unread message.

### URL
- GET
```` URL
  (GET)http://{Server name}:{Port}/{Context root}/api/message/inbox/unread
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
| codes | String | (Required) history type is to be got, ex: 405,406,407 |

#### Response example
```json
{
    "result": [{
            "id": "bb09adf8d5d84f4aa3575de28dab3dd2",
            "from_user_id": "52d15ddda9d8425ca0c182bb4b4457ab",
            "from_user_first_name": "Johnny",
            "from_user_last_name": "Le",
            "to_user_id": "336f6be765594fe4b04dc79bfd99b282",
            "team_id": "hogo",
            "project_id": "d05e89067fe54107aab134ea93889f91",
            "project_name": "New project Oct 2015",
            "message_id": null,
            "status": 0,
            "code": 405,
            "last_update": 1444969075755
        }, {
            "id": "3a343e75959041fc9157b1b008b2e412",
            "from_user_id": "52d15ddda9d8425ca0c182bb4b4457ab",
            "from_user_first_name": "Johnny",
            "from_user_last_name": "Le",
            "to_user_id": "336f6be765594fe4b04dc79bfd99b282",
            "team_id": "hogo",
            "project_id": "24ad685439ee4c2b8c090b29443416b6",
            "project_name": "New project Oct 2015-2",
            "message_id": null,
            "status": 0,
            "code": 405,
            "last_update": 1444969052568
        }],
    "description": "OK",
    "status_code": 200,
    "total_records": 2
}

```