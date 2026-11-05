# Warehouse tools

Small Python utilities for warehouse order and shipping workflows.

Run the tests with `python3 -m unittest discover -s tests -v`.

## Shipping

`shipping_quote(weight_kg, zone, service="standard")` returns a delivery quote.

- **Zones**: `local` and `regional`; weights must be positive.
- **Services**: `standard` (default) or `express`. Express adds a $7.00 surcharge.

```
$ python -m warehouse.cli 5 local
$12.50
$ python -m warehouse.cli 5 local --service express
$19.50
```
