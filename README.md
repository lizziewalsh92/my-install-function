# my-install-function

## Installed chgOverTime function that shows percent change, raw change, and whether the value increased or decreased.

<b>Function:</b>

    def chgOverTime(oldValue, newValue):
    '''
        Calculate the raw difference, whether that difference is positive or negative, AND the percent change over time between two values. 

        Params: oldValue is first number, 
        newValue is second/updated number. Values can be any number (dollars, population, etc.) of the same measure. 

        Output: Returns f-string literal "oldValue decreased/increased by X for a percent change of Y". X is int64, Y is float. 
        '''
    
        rawdiff = (newValue - oldValue)
        pct_chg = ((newValue - oldValue) / oldValue * 100)
    
        if rawdiff > 0:
            posneg = "increased"
        else:
            posneg = "decreased"
    
        return f"{oldValue} {posneg} by {abs(rawdiff)}, for a percent change of {pct_chg:.2f}%"

## Returns f-string literal that says: 'oldValue [increased/decreased] by X, for a percent change of -Y%'
