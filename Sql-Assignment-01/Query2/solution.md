Shipment by Tracking number:
View or analyze shipments based on their unique tracking numbers. Each shipment is identified and tracked using a specific tracking number.

Query: 
select sr.tracking_id_number, ss.status_id ,ss.status_date
from shipment_route_segment as sr
inner join shipment_status as ss
on sr.shipment_id = ss.shipment_id where tracking_id_number is not null ;
