# filepath.um

```

                                                                    
 filepath.um - public domain, os agnostic filepath utility for umka 
 by Marek Maskarinec                                                
 https:github.commarekmaskarineclibs                            
                                                                    
 How to use:                                                        
   replace std.um with the path to your std.um                      
                                                                    

```

## fn dir*
`fn dir*(inp: str): str`

returns the directory in inp


## fn ext*
`fn ext*(inp: str): str`

returns the extension of file inp. if there is no extension, or it is a diroctory, output is ""


## fn fromslash*
`fn fromslash*(inp: str): str`

converts / to platform specific separator


## fn toslash*
`fn toslash*(inp: str) : str`

converts platform specific separator to /


## fn split*
`fn split*(inp: str): (str, str)`

returns the direcory and file of inp. if inp is a folder, it return "" as a file



