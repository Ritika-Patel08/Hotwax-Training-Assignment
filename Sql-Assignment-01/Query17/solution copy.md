BOPIS orders Revenue in the last year:
Calculate the revenue generated from BOPIS orders over the past year.


Query : 

select SUM(oi.quantity*oi.unit_price) as Revenue
from order_item oi
inner join order_item_ship_group ois
on oi.order_id = ois.order_id
where ois.shipment_method_type_id = "STOREPICKUP"
and oi.status_id not in ("ITEM_CANCELLED" , "ITEM_REJECTED");
