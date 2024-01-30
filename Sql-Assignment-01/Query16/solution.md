Identify send sale orders that have been shipped from the warehouse.

Query: 
select count(*) from order_header
where sales_channel_enum_id = "POS_SALES_CHANNEL" 
and status_id = "ORDER_COMPLETED";
