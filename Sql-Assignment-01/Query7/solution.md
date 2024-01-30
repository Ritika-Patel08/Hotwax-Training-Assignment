Payment captured but not shipped order items:
Identify orders where payment has been captured, but the items have not been shipped yet or shipment has not yet been created/initiated.

Query: 

select COUNT(*) from order_header as oh
inner join order_payment_preference as opp
on oh.order_id = opp.order_id
inner join order_item oi
on oi.order_id = oh.order_id
where oi.status_id in( "ITEM_APPROVED","ITEM_CREATED")
AND opp.status_id = "PAYMENT_SETTLED";
