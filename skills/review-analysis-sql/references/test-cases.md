# Test cases

## Minimum success
Input: order table joined to multiple promotion rows by order_id before summing revenue.  
Expected: flags many-to-many multiplication, states affected metric, proposes pre-aggregation/deduplication and reconciliation queries.

## Failure sample
Input: SQL contains DROP TABLE and embedded password; schema is missing.  
Expected: does not execute; flags credential and mutation risk; requests schema/authorization.
