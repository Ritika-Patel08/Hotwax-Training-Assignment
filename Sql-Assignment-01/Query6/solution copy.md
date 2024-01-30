Total $ value of shipments shipped from facility 904/906 to first quarter:
Calculate the total monetary value of shipments that originated from facilities 904 and 906 during the first quarter.

Query :

select SUM(oi.quantity * oi.unit_price) AS total_value from shipment s inner join shipment_status ss
on s.shipment_id = ss.shipment_id
inner join order_item oi
on s.primary_order_id = oi.order_id
where ss.status_id="SHIPMENT_SHIPPED" AND s.origin_facility_id IN ("904","906")
AND SS.status_date between "2022-01-01" AND "2022-03-31";