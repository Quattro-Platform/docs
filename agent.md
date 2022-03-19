# Agent

## Data structure

Name|Type|Extra
----|----|------
`id`|int unsigned|primary_key
`name`|string(50)
`email`|string(120)|nullable
`price_book_id`|int unsigned|foreign_key
`created_at`|timestamp|nullable
`updated_at`|timestamp|nullable

## Relationships

Field|Relation|Model|Items
----|----|------|-----
`price_book_id`|priceBook|[`PriceBook`](price-book)|One
_ |products|[`Product`](product)|Many
_ |customers|[`Customer`](customer)|Many