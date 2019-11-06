# JSON ORM
JSON ORM is a json orm specification.



# fuwu

```json
{
	"table": "user",
    "with": [
        {
            "table": "user_extend",
            "relationship": "one",
            "condition": "id,user_id"
        },{
            "table": "user_login_log",
            "relationship": "many",
            "condition": "id,user_id"
        }
    ],
	"where": [
		["id", 1],
		["id", ">=", 1],
		["id", "=", 1],
		["id", "=<", 1],
		["id", "!=", 1],
		["id", "!>=", 1],
		["id", "!=<", 1],
		["id", "like", 1],
		["id", "in", 1],
		["id", "not in", 1]
	],
	"orWhere": [
		["id", 1],
		["id", ">=", 1],
		["id", "=", 1],
		["id", "=<", 1],
		["id", "!=", 1],
		["id", "!>=", 1],
		["id", "!=<", 1],
		["id", "like", 1],
		["id", "in", ["12",123]],
		["id", "not in", ["12",123]]
	],
	"select": "id,name,sex,created_at",
	"offset": 0,
	"limit": 10,
	"orderBy": "id,desc",
	"handle": "get" // get first delete update create
}
```