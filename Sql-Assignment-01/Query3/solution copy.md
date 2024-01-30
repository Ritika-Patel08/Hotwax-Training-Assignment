Average number of shipments per month:	
Calculate the average number of shipments made per month by dividing the total number of shipments by the number of months.

Query: 

select count(*)/count(distinct date_format(status_date,"%Y-%m"))
from shipment_status
where status_id="SHIPMENT_SHIPPED";
