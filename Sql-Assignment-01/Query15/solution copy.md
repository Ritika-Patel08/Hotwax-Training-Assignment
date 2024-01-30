 Shipping Revenue last month:
Determine the total revenue generated from shipping in the last month.

Query:

select sum(amount)
from order_adjustment
where order_adjustment_type_id = "SHIPPING_CHARGES"
and DATE_FORMAT(created_date, '%Y-%m') = DATE_FORMAT(CURDATE() - INTERVAL 1 MONTH, '%Y-%m');
