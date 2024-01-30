Identify and count the orders and items that were imported in the system during the last week.

Query: 

select count(*),sum(oi.quantity) from order_header oh 
inner join order_item oi on oh.order_id = oi.order_id
where oh.order_date >= CURRENT_DATE - INTERVAL 1 WEEK;
