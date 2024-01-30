Total number of shipments in January 2022 first quarter:
Determine the total count of shipments made during the first quarter of 2022, specifically in the month of January.

select count(*) from shipment_status
where status_id="SHIPMENT_SHIPPED" AND status_date
between "2022-01-01" AND "2022-03-31";