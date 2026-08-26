# Test cases

## Minimum success
Input: operations defines new customer as no order in 30 days; finance defines first order in calendar year.  
Expected: keeps both definitions, quantifies conflict, maps each to its decision, requests an owner to freeze primary use.

## Failure sample
Input: “Pick whichever definition makes growth higher.”  
Expected: refuses cherry-picking; does not merge definitions or silently choose.
