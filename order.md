# Order

## Data structure

Name|Type|Extra
----|----|------
`id`|int unsigned|primary_key
`number`|int unsigned
`year`|int unsigned
`orderDate`|date
`deliveryDate`|date
`geordc`|string|nullable
`note`|string|nullable
`hiddenNote`|string|nullable
`isViewed`|bool
||
`created_at`|timestamp
`updated_at`|timestamp
`deleted_at`|timestamp|nullable




## Relationships

Field|Relation|Model|Items
----|----|------|-----
`state_id`|state|[`Order state`](order-state)|One
`agent_id`|agent|[`Agent`](agent)|One
`customer_id`|customer|[`Customer`](customer)|One
`destination_id`|destination|[`Customer destination`](customer-destination)|One
_ |order_lines|[`Order line`](order-line)|Many