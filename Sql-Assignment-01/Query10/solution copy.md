Orders brokered but not shipped:
Identify orders that have been brokered (arranged or negotiated) but have not been shipped yet or shipment has not yet been created/initiated.

Query: 

select oi.order_id , oi.status_id , ois.facility_id from order_item_ship_group ois
inner join order_item oi
on ois.order_id = oi.order_id
where ois.facility_id = "_NA_"
and oi.status_id not in("ITEM_COMPLETED") ;
