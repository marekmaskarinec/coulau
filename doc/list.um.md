# list.um

```
 list.um - doubly-linked list for umka
 example:
 l := list.List{}
 l.push_front(2)
 l.push_back(4)
 l.insert_after(l.front, 3)
 l.push_front(1)
 printf("%s\n", l.to_str())
```

## struct Any*
```go
type Any* = interface{
}
```



## struct Node*
```go
type Node* = struct {
		value: Any
		next: ^Node
		prev: weak ^Node // cast to ^Node before using
}
```



## struct List*
```go
type List* = struct {
	front: ^Node
	back: ^Node
	length: int
}
```



## fn push_front*
`fn (l: ^List) push_front*(value: Any)`

push value before the first element


## fn push_back*
`fn (l: ^List) push_back*(value: Any)`

add value to the end of the list


## fn insert_after*
`fn (l: ^List) insert_after*(a: ^Node, value: Any)`

insert value after a


## fn from_arr*
`fn from_arr*(s: []Any): List`

creates a list from array s


## fn remove*
`fn (l: ^List) remove*(n: ^Node)`

remove n from the list


## fn to_str*
`fn (l: ^List) to_str*(): str`




