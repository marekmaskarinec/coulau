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

## fn parse*
`fn parse*(inp: str): interface`

parser json provided as an input and returns either map.Map or []interface{}



