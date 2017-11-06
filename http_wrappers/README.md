# HTTP Wrappers

An abstract HTTP interaction is represented by the following structure:
```json
{
	"transition": [],
	"ignored": [],
	"selector": [],
	"strvaluetransfrmr": [],
	"columns": [],
	"override": []
}
```

`transition` contains information of a representative HTTP interaction, `ignored` is a list of parameters which can be ignored from the HTTP request, `selector` is a list of data selector for parameter propogation, `strvaluetransfrmr` is a list of corresponding value transformers, `columns` is a list of parameters to be extracted as output, `override` models a dependency arc.

Each item in `columns` has the following structure:
```json
{
	"param_name": "STRING",
	"sel": {},
	"valtransform": {}

}

```

`param_name` is the name of the parameter to be extracted, `sel` is a selector and `valtransform` is a value transformation function.

`override`:
```json
{
	"param_name": "STRING",
	"param_type": "STRING",
	"model": {}
}
```

`param_name` is the name of a variable parameter, `param_type` is its origin, `model` is an abstract HTTP interaction.