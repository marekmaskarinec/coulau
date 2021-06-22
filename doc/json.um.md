# json.um

```

                                                   
 json.um - public domain json parser for umka      
 by Marek Maskarinec                               
 https:github.commarekmaskarineclibs           
                                                   
 How to use:                                       
   First you need to replace map.um and std.um     
   for the location, where you have them. Then     
   you can use the parse function. It takes a      
   string for input and returns an interface.      
   The interface is either []interface{}, or       
   map.Map.                                        
                                                   
 TODO:                                             
   improve performance                             
                                                   
 Disclaimer:                                       
   this doesn't adhere to json specs perfectly and 
   check for errors much. Please pass it correct   
   json :]                                         
                                                   

```

## struct lexer
```go
type lexer = struct {
	inp: str
	len: int
	pos: int
	lineno: int
}
```



## struct token
```go
type token = struct {
	t: int
	pos: int
	value: str
}
```



## fn get
`fn (l: ^lexer) get(): char`



## fn lex_str
`fn (l: ^lexer) lex_str(): str`



## fn is_num
`fn is_num(inp: char): bool`



## fn lex_num
`fn (l: ^lexer) lex_num(): (str, bool)`



## fn lex_space
`fn (l: ^lexer) lex_space(): str`



## fn lex_next
`fn (l: ^lexer) lex_next(): (token, bool)`



## fn parser_error
`fn parser_error(msg: str)`



## fn parse_object
`fn (l: ^lexer) parse_object(): map.Map`



## fn parse_array
`fn (l: ^lexer) parse_array(): []interface`



## fn parse_val
`fn (l: ^lexer) parse_val(): interface`



## fn parse_object
`fn (l: ^lexer) parse_object(): map.Map`



## fn parse_array
`fn (l: ^lexer) parse_array(): []interface`



## fn parse
`fn parse*(inp: str): interface`

parser json provided as an input and returns either map.Map or []interface{}



