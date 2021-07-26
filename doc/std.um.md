# std.um

```
 Umka standard library
```

## struct File*
```go
type File* = ^struct {}```



## fn fopen*
`fn fopen*    (name: str, mode: str): File`



## fn fclose*
`fn fclose*   (f: File): int`



## fn fread*
`fn fread*(f: File, buf: interface`



## fn fwrite*
`fn fwrite*(f: File, buf: interface`



## fn fseek*
`fn fseek*    (f: File, offset, origin: int): int`



## fn ftell*
`fn ftell*   (f: File): int`



## fn remove*
`fn remove*   (name: str): int`



## fn feof*
`fn feof*    (f: File): bool`



## fn println*
`fn println*(s: str): int`



## fn fprintln*
`fn fprintln*(f: File, s: str): int`



## fn getchar*
`fn getchar*(): char`



## fn atoi*
`fn atoi*(s: str): int`



## fn atof*
`fn atof*(s: str): real`



## fn itoa*
`fn itoa*(x: int): str`



## fn ftoa*
`fn ftoa*(x: real, decimals: int): str`



## fn srand*
`fn srand*(seed: int)`



## fn rand*
`fn rand*(): int`



## fn frand*
`fn frand*(): real`



## fn time*
`fn time*(): int`



## fn clock*
`fn clock*(): real`



## fn argc*
`fn argc*(): int`



## fn argv*
`fn argv*(i: int): str`



## fn getenv*
`fn getenv*(name: str): str`




