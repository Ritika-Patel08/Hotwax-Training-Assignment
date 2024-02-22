## QUERY
    
    Fetch the inventory variances of the products where the reason is ‘VAR_LOST’ or VAR_DAMAGED.

## SOLUTION
```sql
select 
  ii.product_id, 
  iiv.inventory_item_id, 
  iiv.variance_reason_id 
from 
  inventory_item ii 
  join inventory_item_variance iiv on ii.inventory_item_id = iiv.inventory_item_id 
where 
  iiv.variance_reason_id in ("VAR_LOST", "VAR_DAMAGED");

```

## OUTPUT

![Alt text](image-20.png)

#### To show number of rows :

![Alt text](image-21.png)

## QUERY COST 

![Alt text](image-22.png)