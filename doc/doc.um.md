# doc.um

```
```

## interface Element
```go
type Element = interface {
	to_markdown(): str
}
```



## struct Function
```go
type Function = struct {
	prototype: str
	docs: str
	name: str
}
```



## struct Type
```go
type Type = struct {
	is_interface: bool
	name: str
	docs: str
	body: str
}
```



## fn to_markdown
`fn (f: ^Function) to_markdown(): str`



## fn to_markdown
`fn (t: ^Type) to_markdown(): str`



## fn readall
`fn readall(f: std.File): str`



## fn get_docs
`fn get_docs(inp: []str, start: int): str`



## fn get_elements
`fn get_elements(inp: str): []Element`



## fn get_header
`fn get_header(inp: str): str`



## fn main
`fn main()`




