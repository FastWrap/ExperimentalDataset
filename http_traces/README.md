# HTTP Traces

Each trace is represented as a JSON pbject with input, output parameters and HTTP interactions as follows:
```json
[
	{
		"input":{},
		"output":{},
		"transitions":[]
	}
]
```

`transitions` is a list of HTTP interactions, each of which is as follows:
```json
{
	"url": "URL_STRING",
	"request_headers": [],
	"verb": "STRING",
	"raw_data": "STRING",
	"post_data_type": "STRING",
	"data": [],
	"response_headers": [],
	"content_type": "STRING",
	"content": "STING"
}
```