Orders completed hourly:
Analyze and present the distribution of completed orders on an hourly basis.

Query:

select  DATE_FORMAT(ENTRY_DATE, '%Y-%m-%d %H:00:00') AS 
order_completed_hourly,
COUNT(*) AS order_count
from order_header
where status_id="ORDER_COMPLETED"
group by order_completed_hourly;