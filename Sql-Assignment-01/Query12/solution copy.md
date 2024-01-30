Maximum units fulfilled by location:
Identify the location that has fulfilled the maximum number of units. This provides insights into the efficiency of different fulfillment centers.

Query : 

select facility_id , count(*) as facility_cnt 
from order_item_ship_group 
where facility_id not in ("_NA_")
group by facility_id
order by facility_cnt desc
LIMIT 1;
