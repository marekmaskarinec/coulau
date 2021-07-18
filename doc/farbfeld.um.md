# farbfeld.um

```

                                                                  
 farbfeld.um - public domain farbfeld parser and writer           
 by Marek Maskarinec                                              
 https:github.commarekmaskarineclibs                          
                                                                  
 How to use:                                                      
   get yourself a copy of std.um, change line 21 to import from   
   a correct path and import this file.                           
                                                                  
 TODO:                                                            
   make pixelsplit and merge faster                               
                                                                  
 Return values:                                                   
   parse() returns four values. Data itself,                      
   width of the image, height of the image and                    
   an error code. You can compare them to constants               
   in this file. The data itself is an array of uints32           
   in format of 0xrrggbbaa. Iteration over it is shown            
   in the test.                                                   
                                                                  
 Benchmarks:                                                      
   1 minute and 4 seconds to load 4928x3024 image                 
   1 minute and 4 seconds to load 1024x683 image, convert it      
     to monochromatic and write it to another file.               
                                                                  

```

## fn load*
`fn load*(path: str): ([]uint32, int, int, int)`

loads image at path


## fn pixelsplit*
`fn pixelsplit*(inp: uint32): (uint8, uint8, uint8, uint8)`

splits a pixel into 4 uint8s


## fn pixelmerge*
`fn pixelmerge*(r, g, b, a: uint8): uint32`

merges r, g, b and a values into one


## fn write*
`fn write*(path: str, data: []uint32, w: int): int`

writes a farbfeld file from data. w is width of the image



