### Get a id order base on is invoice number
```SQL
SELECT id_order FROM orders WHERE invoice_number (SELECT id_order FROM order_invoice WHERE number = %invoice_number% )
```