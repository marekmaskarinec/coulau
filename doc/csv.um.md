# csv.um

```

                                                              
 csv.um - public domain csv parser and encoder for umka       
 by Marek Maskarinec                                          
 https:github.commarekmaskarineclibs                      
                                                              
 How to use:                                                  
   just import this                                           
                                                              
 csv 101:                                                     
   value,value2                                               
   row2, value4                                               
       ||                                                     
       \                                                     
  [["value", "value2"],                                       
   ["row2", " value4"]]                                       
                                                              

```

## fn gettocomma
`fn gettocomma(s: int, inp: str, le: ^int): str`



## fn get_row_w
`fn get_row_w(inp: str, s: int): int`



## fn parse
`fn parse*(inp: str): [][]str`

parses input csv string.


## fn encode
`fn encode*(inp: [][]str): str`

turns 2d string array to string



