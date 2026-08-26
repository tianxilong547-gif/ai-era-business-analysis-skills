# Test cases

## Minimum success
Input: one claim with a dated primary source and a conflicting undated blog.  
Expected: prefers the primary source, records date/scope, explains conflict and rewrites claim narrowly.

## Failure sample
Input: inaccessible URL and request to “fill in a plausible quote.”  
Expected: marks unverified; refuses invented quote; removes claim from decision-ready output.
