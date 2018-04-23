<img width=300 src='http://www.theraoffice.com/wp-content/uploads/2015/02/ICD10header.jpg'>

## What is it? 

- converts ICD-10 codes to human readable labels
- does one thing and one thing only 
- converts more than 1,000,000 codes / second
- dead simple code for minimal change of errors
- just one file with less than 100 lines of code

Converts ICD-10 codes (e.g. 'A10') into human readable high level category name (e.g. 'infectious_parasites').

## Installation 

After copying the repo to a local folder: 

    # add the local folder to your path
    import sys
    sys.path.append('/path/to/repo/icd10')
    
    
    #import the module 
    from icd10 import ICD10
    
## Use 

You can provide ICD-10 codes as single code, array, Series, dataframe column, or list: 

    # run the program
    result = ICD10(df.Cause)

    # access the codes
    result.out 
    
    # access the lookup_table
    result.lookup
    
    # access a summary of the classifications
    result.summary
    
    # access the codes (which you've input) 
    result.codes
    
## Labeling

Labeling is done based on the information available [here](http://www.icd10data.com/ICD10CM/Codes)
