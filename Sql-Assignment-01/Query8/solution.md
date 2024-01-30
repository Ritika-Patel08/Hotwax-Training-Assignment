Find orders where multiple items are grouped and shipped together in a single shipment

Query: 

select order_id ,count(order_item_seq_id) from order_item_ship_group_assoc
group by order_id
having count(order_item_seq_id) > 1 ;
