# Customer

## Data structure

Name|Type|Extra
----|----|------
`id`|int unsigned|primary_key
`customerCode`|int unsigned|unique
`name`|string(50)
`VAT`|string(11)|nullable
`fiscalCode`|string(16)|nullable
`address`|string(50)
`city`|string(50)
`province`|string(2)
`postalCode`|string(5)
`note`|string(150)|nullable
`canBuy`|bool
`isConfirmed`|bool



## Relationships

Field|Relation|Model|Items
----|----|------|-----
`agent_id`|agent|[`Agent`](agent)|One
`driver_id`|driver|[`Driver`](driver)|One
`production_chain_id`|productionChain|[`Production Chain`](production-chain)|One
_ |destinations|[`Destination`](destination)|Many
_ |orders|[`Order`](order)|Many
_ |contacts|[`Contact`](contacts)|Many