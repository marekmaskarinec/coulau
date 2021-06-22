# std.um

```
 Umka standard library
```

## struct File*
```go
type File* = ^struct {}

const (
    seekBegin* = 0
    seekCur*   = 1
    seekEnd*   = 2
)    

fn rtlfopen  (name: str, mode: str): File;  
fn fopen*    (name: str, mode: str): File {return rtlfopen(name, mode)}

fn rtlfclose (f: File): int
fn fclose*   (f: File): int {return rtlfclose(f)}

fn rtlfread(buf: ^void, size, cnt: int, f: File): int

fn fread*(f: File, buf: interface{}): int {
    if bytes := ^[]uint8(buf); bytes != null {
        return rtlfread(&bytes[0], len(bytes^), 1, f)
    }
    if selfhasptr(buf) {
        error("Cannot read reference types except ^[]uint8")
    }
    return rtlfread(buf.__self, sizeofself(buf), 1, f)
}
```



## fn rtlfopen
`fn rtlfopen  (name: str, mode: str): File;`



## fn fopen
`fn fopen*    (name: str, mode: str): File`



## fn rtlfclose
`fn rtlfclose (f: File): int`



## fn fclose
`fn fclose*   (f: File): int`



## fn rtlfread
`fn rtlfread(buf: ^void, size, cnt: int, f: File): int`



## fn fread
`fn fread*(f: File, buf: interface`



## fn rtlfwrite
`fn rtlfwrite(buf: ^void, size, cnt: int, f: File): int`



## fn fwrite
`fn fwrite*(f: File, buf: interface`



## fn rtlfseek
`fn rtlfseek  (f: File, offset, origin: int): int`



## fn fseek
`fn fseek*    (f: File, offset, origin: int): int`



## fn rtlftell
`fn rtlftell (f: File): int`



## fn ftell
`fn ftell*   (f: File): int`



## fn rtlremove
`fn rtlremove (name: str): int`



## fn remove
`fn remove*   (name: str): int`



## fn rtlfeof
`fn rtlfeof  (f: File): int`



## fn feof
`fn feof*    (f: File): bool`



## fn println
`fn println*(s: str): int`



## fn fprintln
`fn fprintln*(f: File, s: str): int`



## fn getchar
`fn getchar*(): char`



## fn atoi
`fn atoi*(s: str): int`



## fn atof
`fn atof*(s: str): real`



## fn itoa
`fn itoa*(x: int): str`



## fn ftoa
`fn ftoa*(x: real, decimals: int): str`



## fn srand
`fn srand*(seed: int)`



## fn rand
`fn rand*(): int`



## fn frand
`fn frand*(): real`



## fn rtltime
`fn rtltime(): int`



## fn time
`fn time*(): int`



## fn rtlclock
`fn rtlclock(): real`



## fn clock
`fn clock*(): real`



## fn argc
`fn argc*(): int`



## fn argv
`fn argv*(i: int): str`



## fn rtlgetenv
`fn rtlgetenv(name: str): str`



## fn getenv
`fn getenv*(name: str): str`




