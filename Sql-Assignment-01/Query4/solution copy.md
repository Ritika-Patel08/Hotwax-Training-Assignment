Shipped units By Location:
Identify the number of units that have been shipped, categorized by different locations	;. Gain insights into the distribution of shipped units across various locations.

Query: 
select s.origin_facility_id,sum(si.quantity)
from shipment s
inner join shipment_item as si
on si.shipment_id = s.shipment_id
inner join shipment_status ss
on ss.shipment_id = s.shipment_id
where ss.status_id="SHIPMENT_SHIPPED"
group by s.origin_facility_id;
