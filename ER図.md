```startuml
@startuml
entity "顧客マスタ" as customer <m_customers>
{
+ customer_code [PK]
--
pass
name
address
tel
mail
del_flag
reg_date
}
entity "購入テーブル" as kounyuu <d_purchase>
{
+ order_id [PK]
--
customer_code [FK]
purchase_date
total_price
}
entity "顧客詳細テーブル" as syousai <d_purchase_detail>
{
+order_id [PK]
+detail_id [PK]
--
item_code [FK]
price
num
}
@enduml
```
