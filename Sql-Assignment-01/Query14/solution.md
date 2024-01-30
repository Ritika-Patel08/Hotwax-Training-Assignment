Shipping Refund in the last month:
Calculate the refunds issued specifically for shipping charges in the last month.

Query :
select SUM(amount) from return_adjustment
where return_adjustment_type_id = "RET_SHIPPING_ADJ"
and return_type_id = "RTN_REFUND";
