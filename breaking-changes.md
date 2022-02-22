# Breaking changes

## VAT codes
A new table for VAT codes has been introduced, will be used to connect the product with the correct VAT code and to perform some additional computations on prices.

### New table:
Field|Type|Default|Other
-----|----|-------|--------
**id**|`int`|
**code**|`int`|
**description**|`string(191)`
**value**|`float`
**created_at**|`timestamp`||nullable
**updated_at**|`timestamp`||nullable

### New relationship for products

Field|Type|Default|Other
-----|----|-------|--------
...
**vat_code_id**|`int`||foreign

## Prices format changes
All prices have been updated from a two digits decimal to a three digits decimal number.

### Price list
Field|Type|Default|Other
-----|----|-------|--------
...
**fixedPrice**|`decimal(3)`

### Price step
Field|Type|Default|Other
-----|----|-------|--------
...
**price**|`decimal(3)`

### Order line
Field|Type|Default|Other
-----|----|-------|--------
...
**qta**|`float`
**shipped_quantity**|`float`
**unitPrice**|`decimal(3)`
**price_list_price**|`decimal(3)`
**supplier_price**|`decimal(3)`

### Shipment line
Field|Type|Default|Other
-----|----|-------|--------
...
**qta**|`decimal(2)`

### Purchase order line
Field|Type|Default|Other
-----|----|-------|--------
...
**qty**|`decimal(2)`
**shipped_quantity**|`decimal(2)`
**purchasePrice**|`decimal(3)`


