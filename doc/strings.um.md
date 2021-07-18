# strings.um

```

                                                                  
 strings.um - public domain string manipulation library for umka  
 by Marek Maskarinec                                              
 https:github.commarekmaskarineclibs                          
                                                                  
 How to use:                                                      
   just import this.                                              
                                                                  
 TODO:                                                            
  - increase performance                                          
                                                                  

```

## struct builder*
```go
type builder* = struct {
	len: int
	buf: []char
}
```

builder allows for faster string addition.


## fn mk_builder*
`fn mk_builder*(): builder`

creates an allocated builder


## fn write_str*
`fn (b: ^builder) write_str*(inp: str)`

writes a string to a builder


## fn write_char*
`fn (b: ^builder) write_char*(inp: char)`

writes a char to the builder


## fn to_str*
`fn (b: ^builder) to_str*(): str`

returns the content of a builder as a string


## fn sslice*
`fn sslice*(inp: str, start, end: int): str`

same as standard slice, but usable with string. the numbers are inclusive


## fn contains*
`fn contains*(inp, check: str): bool`

returns true, if string is contained in another string


## fn join*
`fn join*(inp: []str, joiner: str): str`

joins an array of string into one and adds a joiner between them


## fn replace*
`fn replace*(inp, pattern, replacer: str): str`

replaces an pattern with a string


## fn split*
`fn split*(inp: str, splitter: str): []str`

splits a string, every time a pattern occurs. it deletes it (equivalent to replace(s, pattern, ""))


## fn toupper*
`fn toupper*(inp: str): str`

returns the same string, but characters are upper case


## fn tolower*
`fn tolower*(inp: str): str`

returns the same string, but all characters are lower case


## fn repeat*
`fn repeat*(inp: str, count: int): str`

repeats string count number of times


## fn trimspaces*
`fn trimspaces*(inp: str): str`

trims whitespaces from the start and end of a string


## fn trimprefix*
`fn trimprefix*(inp: str, prefix: str): str`

trims a prefix of a string


## fn trimsuffix*
`fn trimsuffix*(inp: str, suffix: str): str`

trims a suffix of a string



